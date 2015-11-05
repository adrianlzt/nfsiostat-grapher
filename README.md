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
nfsiostat-grapher 1 -J datos.json
```

Generar reporte a partir de un fichero JSON:
```
nfsiostat-grapher -L datos.json -H output.html
```


Para generar gráficas necesita:
```
bokeh==0.10.0
```
