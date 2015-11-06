# nfsiostat-grapher
Modified version of nfsiostat to generate graphics

Generar reporte con metricas cada segundo:
```
nfsiostat-grapher 1 -H output.html
```
Para generar el reporte deberemos parar la ejecucción con Control+C (SIGINT).

También podemos mandarle un ``kill -10 PID`` para forzarle a que genere los datos sin para la ejecucción.



Generar reporte con diez metricas, una cada segundo:
```
nfsiostat-grapher 1 10 -H output.html
```

Generar fichero JSON con metricas cada segundo:
```
nfsiostat-grapher 1 -J example_data.json
```

Generar reporte a partir de un fichero JSON:
```
nfsiostat-grapher -L example_data.json -H example_output.html
```


Para generar gráficas necesita:
```
bokeh==0.10.0
```


8 horas de captura cada 2", con 3 unidades NFS montadas, ocupan: 69MB
