# Postwork

### **Instrucciones**

Con base en la aplicación que has ido desarrollando a lo largo del módulo crearás imágenes Docker y podrás lograr versionar las mismas, tomando en cuenta las siguientes indicaciones:

- Deberás descargar y manipular imágenes Docker.
- Versionar las imágenes creadas.
- Utilizar línea de comandos para comprender la Infraestructura.
- Desplegar un servidor de aplicaciones basado en Docker.

### Desarrollo

**1.** Utiliza el repo de Apache

[https://hub.docker.com/_/httpd](https://hub.docker.com/_/httpd)

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled.png)

**2.** Ejecuta el comando para descargar la Imagen a tu local:

`docker pull httpd`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%201.png)

**3** Ejecuta el siguiente comando:

`docker images`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%202.png)

**4.** Verás una indicación similar como la siguiente:

`REPOSITORY      TAG       IMAGE ID       CREATED        SIZE ubuntu-update   latest    31889a5b4786   34 hours ago   104MB httpd           latest    ad17c88403e2   4 days ago     143MB ubuntu          latest    ba6acccedd29   5 weeks ago    72.8MB`

**5.** Ahora, levantarás la imagen con lo siguiente:

`docker run -d --name apache-server -p 80:80 httpd`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%203.png)

Con esto, tendrás el servidor de aplicaciones iniciado:

![https://assets.bedu.org/contents/TECM0066DSAG_Desarrollo_Software_agil/TECM0066DSAG_S4_3_1.png](https://assets.bedu.org/contents/TECM0066DSAG_Desarrollo_Software_agil/TECM0066DSAG_S4_3_1.png)

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%204.png)

**6.** Ejecuta lo siguiente:

`docker ps`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%205.png)

**7.** Verás algo similar:

`CONTAINER ID   IMAGE     COMMAND              CREATED       STATUS       PORTS                NAMES 65db7597168c   httpd     "httpd-foreground"   2 hours ago   Up 2 hours   0.0.0.0:80->80/tcp   apache-server`

**8.** Ubica el Container ID y ejecútalo:

`docker exec -it 5ec19c1e3408 bash`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%206.png)

**9.** Una vez dentro de tu contenedor, actualiza:

`apt-get update & apt-get upgrade -y`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%207.png)

**10.** Instala un par de tools (wget, zip)

`apt install wget apt install zip`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%208.png)

**11.** Ubícate en el path:

`cd /usr/local/apache2/htdocs`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%209.png)

**12.** Descarga un zip, con el site a desplegar:

`wget`

[https://github.com/beduExpert/DevOps-Fundamentals-2021/raw/main/Sesion-01/coming-soon-evening-html.zip](https://github.com/beduExpert/DevOps-Fundamentals-2021/raw/main/Sesion-01/coming-soon-evening-html.zip)

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%2010.png)

**13.** Descomprime el zip:

`unzip coming-soon-evening-html.zip`

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%2011.png)

**14.** Actualiza el navegador, donde podrás ver el sitio actualizado como se muestra en la imagen.

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%2012.png)

### **Checklist**

![Untitled](Postwork%204b3310eabc3d48e289c24ee77a13c2ed/Untitled%2013.png)