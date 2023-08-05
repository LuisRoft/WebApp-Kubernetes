# Mi Aplicación en Kubernetes

Este es un proyecto de ejemplo que muestra cómo implementar una aplicación web simple en un clúster de Kubernetes y subir el código a GitHub. La aplicación utiliza Node.js y Docker para crear un contenedor que se despliega en el clúster, y se expone a través de un servicio para que pueda ser accedida desde Internet.

## Requisitos

Antes de comenzar, asegúrate de tener instalados los siguientes componentes:

- Docker: Para construir la imagen del contenedor de la aplicación.
- Kubernetes: Para desplegar la aplicación en un clúster.

## Despliegue de la Aplicación

Siga estos pasos para desplegar la aplicación en Kubernetes:

1. Clona este repositorio en tu máquina local:

```
git clone https://github.com/LuisRoft/WebApp-Kubernetes
cd tu-repositorio
```

2. Construye la imagen del contenedor usando Docker:

```
docker build -t tu-repositorio-de-docker/mi-aplicacion:latest .
```

3. Asegúrate de estar conectado al clúster de Kubernetes donde deseas desplegar la aplicación:

```
kubectl config use-context tu-contexto
```

4. Implementa la aplicación en el clúster:

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Esto creará las réplicas de la aplicación y expondrá el servicio para que sea accesible desde Internet.

5. Verifica el estado de la implementación:

```
kubectl get pods
kubectl get services
```

## Acceder a la Aplicación

Una vez que la implementación se haya completado, puedes acceder a la aplicación en tu navegador web a través de la dirección IP pública del servicio. Puedes obtener la dirección IP utilizando el siguiente comando:

```
kubectl get services
```




