# Se crea un pod multicontenedor de acuerdo a lo esperado

### Se muestra la información del Pod se vea que contiene dos contenedores

![image](https://user-images.githubusercontent.com/67799058/198738471-ee652d03-eac2-41f5-b9a7-c7d4f2e5d3e6.png)

### Se muestra el contenido del archivo index.html en el primer contenedor, ejecutando:

```
kubectl exec pod-multicontenedor -c contenedor1 -- /bin/cat /usr/share/nginx/html/index.html
```

![image](https://user-images.githubusercontent.com/67799058/198738536-79e3fb14-d74e-4aea-9e1b-ad9145fb61ab.png)


### Se muestra el contenido del archivo index.html en el segundo contenedor, ejecutando:

```
kubectl exec pod-multicontenedor -c contenedor2 -- /bin/cat /html/index.html
```

![image](https://user-images.githubusercontent.com/67799058/198738735-b7b3bd7a-6e7c-43d8-b1ca-c06d6dd0fa0d.png)

### Se ejecuta un "port forward" para acceder al Pod en el puerto 8081 de localhost

![image](https://user-images.githubusercontent.com/67799058/198738831-b1e34c28-54a2-4be4-ac6b-ef4c8a1ac472.png)

### Motivado a que el pod fue montado en vagrant usamos lynx para verificar la pagina web 

```
 lynx http://127.0.0.1:8081
```
![image](https://user-images.githubusercontent.com/67799058/198738943-5c34ad64-97dc-4d80-9eae-5809098eb763.png)
