## 📦 Required Packages
Assuming that `Python` (version 3) is installed in the targeted machine, to install the required packages:
```
pip install docopt scipy numpy csv graphviz
```
or
```
python -m pip install docopt scipy numpy csv graphviz
```

## ⚙️ Usage
### Task generator:
The options of the taskset generator are as follows (`python ./task_generator.py -h`):
```
Usage:
    task_generator                [options]

Options:
    --round, -r                round the numbers [default: False]
    --utilization=N, -u N      system utilization in percent  [default: 50]
    --generator=N, -g N        task generation algorithm (0: WATERS 1: UUniFast 2: Emberson 3:WATERS (fixed-sum))  [default: 1]
    --mapping=N, -m N          the mapping algorithm of taskset (0: No mapping 1: Worst-fit 2: First-fit) [default: 0]
    --ntask=N, -n N            number of tasks in one taskset  [default: 15]
    --nset=N, -s N             number of tasksets to generate  [default: 1]
    --npe=N, -p N              number of processing elements  [default: 4]
    --version, -v              show version and exit
    --help, -h                 show this message
```
To test the tool and run the taskset generator with the default options:
```
$ python ./task_generator.py
```

### Jobset generator:
In order to generate a jobset with specific job-level fixed priority policy from a taskset, you can use the `./priority_generator.py`. The options of the jobset generator are as follows (`./priority_generator.py -h`):
```
Usage:
    priority_generator               [-t FILE] [options]

Options:
    --taskset FILE, -t FILE          taskset csv file [default: taskset-0.csv]
    --method=N, -m N                 priority assigning method (0: Rate-monotonic,1: Deadline-monotonic,2: Earliest deadline first (EDF)) [default: 0]
    --sag, -s                        generate with SAG format
    --version, -v                    show version and exit
    --help, -h                       show this message
```
 

### Group generator:
In order to generate a group of tasksets and their jobsets, you can use the `./group_generator` bash script. The options of the group taskset generator are as follows (`./group_generator -h`):
```
Usage:
      group_generator.sh  [-argument value]...

Options:
    -s N      number of tasksets to generate  [default: 1]
    -n N      number of tasks in each taskset  [default: 10]
    -u N      system utilization in percent  [default: 50]
    -g N      task generation algorithm (0: WATERS 1: UUniFast 2: Emberson 3: WATERS (fixed-sum))  [default: 1]
    -p N      priority assigning method (0: Rate-monotonic 1: Deadline-monotonic 2: Earliest deadline first (EDF)) [default: 0]
    -c N      number of cores [default: 4]
    -v        show version and exit
    -h        show this message

```

## 🔧 Features
  * "[UUnifast](https://dl.acm.org/doi/abs/10.1007/s11241-005-0507-9)" taskset generator<sup>[1](#note1)</sup>
  * "[Real world automotive benchmark for free](https://www.ecrts.org/forum/viewtopic.php?f=20&t=23)" taskset generator with subset sum algorithm<sup>[1](#note1)</sup>
  * "[Emberson et al.](https://www.ecrts.org/archives/fileadmin/WebsitesArchiv/Workshops/WATERS/Proceedings/WATERS-2010-Proceedings.pdf#page=6)" taskset generator
  * "[Real world automotive benchmark for free](https://www.ecrts.org/forum/viewtopic.php?f=20&t=23)" taskset generator with RandFixedSum algorithm
  * Random multi-rate DAG generator<sup>[2](#note2)</sup>

## 🚧 Limitations 
- For now, the generators just support the discrete-time model and all the numbers are integer.

Newer and more advanced versions of this tool is available [here](https://github.com/porya-gohary/real-time-task-generator-framework). 
