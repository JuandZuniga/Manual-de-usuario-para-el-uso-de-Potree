# Documentación para le uso de Potree.
Para el uso de la herramienta de Potree se requiere realizar pasos adicionales.
## Herramienta de XAMPP
Para este caso se usara XAMPP como un servidor que alojara de manera local nuestor sitio web.
1. Descargar en el sitio oficial [XAMPP](https://www.apachefriends.org/es/index.html)
    - XAMPP ofrece varias versiones de descarga para este proyecto se utilizo la version 8.2.12 para un OS de Windows. XAMPP presenta diferentes versiones para sistemas Linux o OS X
2. Una vez descargada XAMPP proceda a realizar la instalación del paquete en su dispositivo.
    - Si presenta problemas para la instalación puede dirigirse al siguiente enlace [Problemas con instalación de XAMPP](https://www.youtube.com/watch?v=Uyq3KbVwz3k&t=577s)
    **Nota:** Este enlace solo es para problemas en sistemas Windows.
3. Al realizar la instalación ingrese a la aplicación de XAMPP y se abrira el siguiente panel.

    <img alt="Panel de control XAMPP" src="image\PanelControlXampp.png" />

4. En el panel de control de XAMPP se presentaran diferentes herramientas como Apache, MySQL, FileZilla, Mercury, Tomcat. 
Para este proyecto solo uso la herramienta de Apache. El cual es un servidor local en el alojara el sitio web de Potree.
    - Para activar este servidor presione en **Start** y espera que el modulo de Apache este en color verde como se muestra en la siguiente imagen
    <img alt="Panel de control XAMPP" src="image\PanelControlXamppVerde.png" />

## PotreeConvert
Una vez Instalado XAMPP y activado el servidor Apache en su dispositivo local, proceda a descargar PotreeConvert.
1. Descargar en el sitio oficial de [PotreeConvert](https://github.com/potree/PotreeConverter/releases)
    - Al ingresar al sitio web procesada a descargar PotreeConvert correspondiente a su sistema operativo. Para este proyecto se utilizo OS Windows

    <img alt="Panel de control XAMPP" src="image\PotreeConvertDesa.png" />  
2. Al descargar esta herramienta el archivo que se descarga es un .zip por lo cual debe de extraer esos archivo de la carpeta.
    - Una vez realizada la extracción se presentaran los siguiente archivos extraidos. El arhivo extraido que se utilizo fue `PotreeConvert.exe`

    <img alt="Panel de control XAMPP" src="image\IndexPotreeCon.png" />

### Convertir y Generar pagina web
Para realizar la conversión y generar la pagina web para visualizar la nube de puntos realiza lo siguientes paso

1. Ingrese a su herramientas de comandos. Para este proyecto se uso el CMD de Windows.
    - Una vez ingrese al CMD dirigase en donde guardo el `PotreeConvert.exe`. En este proyecto la aplicación de guardo en una carpta llamada potree
    ```
    C:\potree
    ```
    - Luego de ingresar a la carpeta donde guardo el aplicativo procesa a realizar el siguiente comando
    ```
    ./PotreeConverter.exe C:/pointcloud.las -o C:/xampp/htdocs/potree --generate-page pageName
    ```
    Explicaión del comando
    ```
    ./PotreeConverter.exe --> Comando para usar PotreeConvert.
    C:/pointcloud.las --> Ubicación de la nube de puntos.
    -o --> Comando para guardar el proyecto
    C:/xampp/htdocs/potree --> Ubicación en donde guardar el proyecto.
    --generate-page pageName --> Comando para generar la pagina web y asignación del nombre.
    ```
2. Al final de la conversión, PotreeConvert arrojara lo siguiente archivo

<img alt="" src = "image\LibsPotree.png">

## Visualización de Resultados
Una vez realizado los comandos anteriores puede ingresar a un web browser. En este caso se uso Microsoft Edge, en el buscador ingrese el siguiente URL `http://localhost/output/prove.html`

<img alt = "" src= "image\ResultPotree.png">

## Referencias
1. Si desea conocer más de esta herramienta puede dirigirse al reposiotrio de Github [Potree](https://github.com/potree/potree)
2. Para obtener más información sobre la herramienta de conversión [PotreeConvert](https://github.com/potree/PotreeConverter)

# Bibtex
    ```
    @article{SCHUETZ-2020-MPC,
	title =      "Fast Out-of-Core Octree Generation for Massive Point Clouds",
	author =     "Markus Schütz and Stefan Ohrhallinger and Michael Wimmer",
	year =       "2020",
	month =      nov,
	journal =    "Computer Graphics Forum",
	volume =     "39",
	number =     "7",
	doi =        "10.1111/cgf.14134",
	pages =      "13",
	publisher =  "John Wiley & Sons, Inc.",
	pages =      "1--13",
	keywords =   "point clouds, point-based rendering, level of detail",
}
    ```