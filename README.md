# Introducción

Node-RED es una plataforma de código abierto basada en Node.js para desarrollar aplicaciones IoT y automatización del hogar. Es una herramienta visual de programación, lo que significa que los desarrolladores pueden crear flujos de trabajo utilizando bloques de construcción en lugar de escribir código. Los bloques se conectan entre sí para crear un flujo de trabajo, y los datos fluyen entre los bloques a medida que se ejecuta el flujo.

Node-RED se utiliza a menudo para integrar diferentes dispositivos y servicios, como sensores, dispositivos IoT, aplicaciones web y servicios en la nube. Los desarrolladores pueden crear flujos de trabajo para recopilar datos de sensores, enviar alertas, controlar dispositivos, y más. También se puede utilizar para automatizar tareas en el hogar, como encender y apagar las luces, regular la temperatura y la humedad, y para recibir alertas de seguridad.

# Material Necesario

- [Instalar NodeJS](https://github.com/RaulToribio/13-Instalar-NodeJS)

# Instrucciones V 1.0

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(1).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(1).png)

Acceder a la página web de [OpenWeatherMap](https://openweathermap.org/).

Clic en “Sign In”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(2).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(2).png)

Ingresar información de acceso o crear una cuenta.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(3).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(3).png)

Clic en “API”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(4).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(4).png)

Clic en “Usuario”.

Clic en “My API Keys”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(5).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(5).png)

Generar “Key”.

Copiar “Key”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(6).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(6).png)

Clic en “API”.

Clic en “API doc” en la sección “Current Weather Data”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(7).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(7).png)

Copiar “API Call”.

`https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&units=metric&appid={API key}`.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(8).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(8).png)

Buscar coordenadas del lugar al que deseemos monitorear.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(9).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(9).png)

Componer la “API Call” con coordenas, API Key y tipo de medición omitiendo las llaves “*{}*”.

`https://api.openweathermap.org/data/2.5/weather?lat=19.4263&lon=-99.1679&units=metric&appid=f7d7dcd811b9febeeae5eb55ddcfdad5`.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(10).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(10).png)

Flujo 05 V 1.0 - Node-RED.

El objetivo de este ejercicio en Node-RED es poder visualizar una gráfica de tipo “Gauge” y tipo “Chart” la temperatura, humedad y el nombre de todas las personas que publiquen el el tema “codigoIoT/G8/mosquitto/flow5”. Los datos se obtendrán de [OpenWeatherMap](https://openweathermap.org/).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(11).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(11).png)

Información obtenida al suscribirse al tema “codigoIoT/G8/mosquitto/flow5”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(12).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(12).png)

Resultado (información obtenida de [OpenWeatherMap](https://openweathermap.org/)).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(13).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(13).png)

Nodo “Inject”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(14).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(14).png)

Nodo “HTTP Request”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(15).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(15).png)

Nodo “JSON”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(16).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(16).png)

Nodo “Function” (Temperatura - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(17).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(17).png)

Nodo “Gauge” (Temperatura - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(18).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(18).png)

Nodo “Function” (Humedad - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(19).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(19).png)

Nodo “Gauge” (Humedad - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(20).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(20).png)

Nodo “MQTT In”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(21).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(21).png)

Nodo “JSON”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(22).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(22).png)

Nodo “Function” (Temperatura - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(23).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(23).png)

Nodo “Chart” (Temperatura - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(24).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(24).png)

Nodo “Function” (Humedad - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(25).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(25).png)

Nodo “Chart” (Humedad - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(26).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(26).png)

Nodo “Inject”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(27).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(27).png)

Nodo “Function” (contiene la información a enviar en formato JSON).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(28).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(28).png)

Nodo “MQTT Out”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(29).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%201.0/Flujo%2005%20V%201%20(29).png)

Configuración del “Broker”.

# Instrucciones V 2.0

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(1).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(1).png)

Clic en “API”.

Clic en “API doc” en la sección “One Call API 3.0”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(2).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(2).png)

Documentación de “One Call API 3.0”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(3).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(3).png)

Copiar “API Call”.

`https://api.openweathermap.org/data/3.0/onecall?lat=33.44&lon=-94.04&exclude=hourly,daily&units=metric&appid={API key}`

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(4).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(4).png)

Buscar coordenadas del lugar al que deseemos monitorear.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(5).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(5).png)

Flujo 05 V 2.0 - Node-RED.

El objetivo de este ejercicio en Node-RED es poder visualizar una gráfica de tipo “Gauge” y tipo “Chart” la temperatura, humedad, nivel UV, calidad del aire y el nombre de todas las personas que publiquen el el tema “codigoIoT/G8/mosquitto/flow5”. Los datos se obtendrán de [OpenWeatherMap](https://openweathermap.org/).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(6).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(6).png)

Información obtenida al suscribirse al tema “codigoIoT/G8/mosquitto/flow5”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(7).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(7).png)

Resultado (información obtenida de [OpenWeatherMap](https://openweathermap.org/)).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(8).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(8).png)

Nodo “Inject”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(9).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(9).png)

Nodo “HTTP Request”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(10).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(10).png)

Nodo “JSON”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(11).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(11).png)

Nodo “Function” (Temperatura - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(12).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(12).png)

Nodo “Gauge” (Temperatura - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(13).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(13).png)

Nodo “Function” (Humedad - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(14).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(14).png)

Nodo “Gauge” (Humedad - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(15).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(15).png)

Nodo “Function” (UV - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(16).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(16).png)

Nodo “Gauge” (UV - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(17).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(17).png)

Nodo “HTTP Request”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(18).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(18).png)

Nodo “JSON”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(19).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(19).png)

Nodo “Function” (Calidad - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(20).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(20).png)

Nodo “Gauge” (Calidad - Local).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(21).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(21).png)

Nodo “MQTT IN”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(22).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(22).png)

Configuración del “Broker”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(23).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(23).png)

Nodo “JSON”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(24).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(24).png)

Nodo “Function” (Temperatura - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(25).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(25).png)

Nodo “Chart” (Temperatura - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(26).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(26).png)

Nodo “Function” (Humedad - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(27).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(27).png)

Nodo “Chart” (Humedad - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(28).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(28).png)

Nodo “Function” (UV - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(29).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(29).png)

Nodo “Chart” (UV - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(30).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(30).png)

Nodo “Function” (Calidad - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(31).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(31).png)

Nodo “Chart” (Calidad - General).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(32).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(32).png)

Nodo “Inject”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(33).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(33).png)

Nodo “Function” (contiene la información a enviar en formato JSON).

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(34).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(34).png)

Nodo “MQTT Out”.

![https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(35).png](https://raw.githubusercontent.com/RaulToribio/22-Flujo-05/main/Im%C3%A1genes/Flujo%2005%20V%202.0/Flujo%2005%20V%202%20(35).png)

Configuración del “Broker”.

# Créditos

> [José Raúl Toribio Gabriel](https://github.com/RaulToribio)
> 

> [Codigo IoT](https://github.com/codigo-iot)
>
