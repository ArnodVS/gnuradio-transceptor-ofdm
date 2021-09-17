# gnuradio-transceptor-ofdm

### Resumen
Este proyecto fue compialdo en GNU Radio Companion 3.7.11 con el interprete de Python2, y ejecutado con la distribución Ubuntu 18.04 LTS.
El diagrama de flujos trx-ofdm.grc contiene el procesamiento que lleva acabo un transceptor OFDM con un mapa QPSK para la carga útil y BPSK para sus encabezados.

### Introducción
El algoritmo trx-ofdm.py proporciona símbolos OFDM con 54 subportadoras, de las cuales 4 son portadoras piloto y 48 son portadoras con carga útil. Las 54 portadoras son moduladas por el bloque ifft con una longitud de ventana de 64 para procesar todas las portadoras.

### Dependencias
- GNU Radio Companion 3.7.11

### Instrucciones de Uso
1. Clonar el repositorio.
2. Abrir Terminal desde el directorio con el repositorio descargado.
3. Ejecutar el archivo compilado trx-ofdm.py
4. Adicionalmente se puede modificar el diagrama de flujos trx-ofdm.grc o directamente en el código trx-ofdm.py.

### Redacción Futura
Este algoritmo OFDM puede ser modificado desde su diagrama de flujos para integrar el control de hardware SDR, basta con separar el Tx y el RX e integrar un bloque de control SDR (como los bloques UHD:USRP) en cada diagrama de flujos separado. Esto con la intención de generar un enlace RF con simbolos OFDM  en bandas de Wi-Fi.
