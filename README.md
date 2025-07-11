# Análisis Dataset CDRs #
![Python >=3.11](https://img.shields.io/badge/python-%3E%3D3.11-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

## Descripción
**¿Qué son los CDRs de datos móviles?**

Los Registros de Detalles de Llamadas (CDRs, por sus siglas en inglés) de datos móviles son registros generados por los operadores de redes móviles cada vez que un usuario utiliza datos móviles para navegar por internet, usar aplicaciones, enviar correos electrónicos, etc. Estos registros contienen metadatos que describen el uso de los datos móviles, sin incluir el contenido de las actividades realizadas. Los CDRs de datos móviles incluyen información como:

- **Número de teléfono**: El número asociado al dispositivo móvil que utiliza los datos.
- **Fecha y hora**: Cuándo comenzó y terminó la sesión de datos.
- **Duración de la sesión**: Cuánto tiempo duró la sesión de datos.
- **Volumen de datos**: La cantidad de datos transmitidos durante la sesión, generalmente medida en megabytes (MB) o gigabytes (GB).
- **Tipo de servicio**: La naturaleza del servicio utilizado, como navegación web, transmisión de video, o uso de aplicaciones.
- **Ubicación**: La torre celular a través de la cual se realizó la conexión de datos, lo que permite aproximar la ubicación del usuario.

Estos registros son cruciales para que los operadores de telecomunicaciones puedan facturar a los usuarios según su consumo de datos. Además, los CDRs de datos móviles permiten a los operadores monitorear el uso de la red, optimizar su rendimiento, y detectar posibles fraudes o usos indebidos​​.

Los CDRs de datos también tienen aplicaciones más amplias, como el diseño de planes de datos personalizados, y la mejora de los servicios ofrecidos por los operadores. En el campo de la ciencia de datos, estos registros pueden ser analizados para obtener insights valiosos sobre el comportamiento de los usuarios y la eficiencia de la red​.

![image](https://github.com/user-attachments/assets/09e64de8-85bb-4dca-8b27-6899d5a6f88c)

A partir de un dataset en bruto se realiza el curado del mismo. Luego se continúa con el análisis en pos de encontrar patrones comúnes entre algunos usuarios.

**Necesidad de Negocio:** Una posible necesidad es configurar cada APN de manera de minimizar la cantidad de registros generados por el trafico de los dispositivos conectados al mismo. Para ello es necesario establecer una configuración técnica para cada APN. Lo mejor es agrupar los distintos tipos de comportamiento de tráfico en cada APN. Luego será necesario agrupar APNs con comportamientos similares para aplicarles la misma configuración por grupo. De esa forma se minimiza la cantidad de distintas configuraciones a gestionar.

## Data Set ##
Se presenta el dataset con su diversidad de campos ya listo para los pasos siguientes.

| **Campo**     | **Tipo** | **Descripción**                                |
|---------------|----------|------------------------------------------------|
| **IdTD**      | Numeric  | Identificador de detalle del tráfico de datos  |
| **ICCID**     | Text     | ICCID                                          |
| **MSISDN**    | Numeric  | MSISDN                                         |
| **IMSI**      | Numeric  | IMSI                                           |
| **NAccount**  | Numeric  | Número de cuenta                               |
| **Chargeable?** | Boolean | Etiqueta Cobrable                            |
| **FactCicle** | Numeric  | Ciclo de facturación                           |
| **SIMStatus** | Numeric  | Estado de SIM                                  |
| **Tserv**     | Text     | Tipo de servicio                               |
| **IdRP**      | Numeric  | Número de plan de precios asignado             |
| **IdRZ**      | Numeric  | Identificador de la zona de precios asignada   |
| **UsoNoPico** | Boolean  | Etiqueta de uso en no pico                     |
| **DReg**      | Time     | Fecha de recepción del registro                |
| **Tdata**     | Numeric  | Uso de datos - Total sin procesar              |
| **Udata**     | Numeric  | Uso de datos - Subida sin procesar             |
| **Ddata**     | Numeric  | Uso de datos - Bajada sin procesar             |
| **RoundData** | Numeric  | Uso de datos - Redondeado                      |
| **APN**       | Text     | APN                                            |
| **IPv4**      | Text     | Dirección IPv4                                 |
| **Network**   | Numeric  | Red del operador                               |
| **DIni**      | Time     | Hora de inicio del registro                    |
| **Duration**  | Numeric  | Duración de la sesión                          |
| **Nsec**      | Numeric  | Número de secuencia del registro               |
| **IdCharge**  | Numeric  | Número de cargo                                |
| **CloseCod**  | Numeric  | Cerrar causa de sesión                         |
| **TAP**       | Text     | Código de TAP                                  |
| **IdAccountOp** | Numeric | ID de cuenta del operador                    |
| **IdRPVersion** | Numeric | Identificador de la versión de plan de precios|
| **IdFlow**    | Numeric  | Identificador de flujo                         |
| **SGSN**      | Text     | SGSN en servicio                               |
| **CallTech**  | Numeric  | Tipo de tecnología de llamada                  |

## Instalación de Dependencias
Se provee archivo con los requerimientos:
```bash
conda install --file requirements.txt
```

## Resultados
> Puede ver una presentación resumida sobre el análisis realizado en formato .pdf en el siguiente archivo:
> [📄 Ver informe en PDF](./Análisis%20de%20CDRs.pdf)

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

💡 For commercial inquiries or specific licensing questions, feel free to contact me.
