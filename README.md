# nfsiostat-grapher
Modified version of [http://git.linux-nfs.org/?p=steved/nfs-utils.git;a=blob;f=tools/nfs-iostat/nfs-iostat.py;h=61d15a540e4f1c2c9d250d1f1956520e52af3213;hb=1df82a36df74a59f55eea99d08612564fa22cbef nfsiostat] to generate graphics. It also prints output in YAML format.

Generate report with metrics each second:
```
nfsiostat-grapher 1 -H output.html
```
To generate report stop the execution with Control+C (SIGINT).

We can also generate the report without stopping the program: ``kill -10 PID``




Generate report with 10 metrics, one each second:
```
nfsiostat-grapher 1 10 -H output.html
```

Generate JSON file with metrics each second:
```
nfsiostat-grapher 1 -J example_data.json
```

Generate report from a previosly collected JSON file:
```
nfsiostat-grapher -L example_data.json -H example_output.html
```

8 hours of capture each 2" with 3 NFS units weight: 69MB


To generate data we need these libs:
```
bokeh==0.10.0
```
