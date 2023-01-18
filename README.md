<h1> Vulnerabilidad a la COVID-19 </h1>
  <p>Este repositorio contiene los enlaces donde se logró acceder a los 
    datos abiertos implementados para este proyecto, así como la guía de 
    cómo estan divididas las carpetas y archivos.
  </p>
 
  <ol>
    <h2>Recolección de datos (Modelo Inicial)</h2>
    <li> <a
      href="http://microdatos.dane.gov.co/index.php/catalog/643/data_dictionary#page=F9&tab=data-dictionary"> 
      Censo Nacional de Población y Vivienda 2018</a>: </li>
    <ul>
      Los datos fueron recolectados por el DANE y tienen información sociodemográfica dividida en 5 datasets 
      de los cuales, a partir de las variables seleccionadas se consideraron 4 que proveían información 
      relevante; los datasets usados fueron: vivienda, hogares, fallecidos y personas.
    </ul>
    <li> <a
      href="https://geoportal.dane.gov.co/visor-vulnerabilidad/"> 
      Indice de vulnerabilidad del DANE</a>: </li> 
    <ul>
      Los datos de vulnerabilidad fueron recolectados del geo-portal de vulnerabilidad realizado por el DANE
      el cual permite descargar los archivos en formato Shapefile. Este es un formato que permite almacenar 
      la información geométrica y la información de atributos de las entidades geográficas. Estos datos son 
      estáticos y se encuentran para la mayoría de municipios en Colombia.
    </ul>
    <h2>Distribución de los archivos (Modelo Inicial)</h2>
    <ul>
    <li> <a
      href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/tree/main/Initial%20Index"> 
      Initial Index</a>: </li>
      En esta carpeta se encuentra el diccionario de datos para cada uno de los datasets que se obtuvieron 
      como resultado de los datasets publicados por el DANE. Esta carpeta cuenta con 9 archivos en formato
      .ipynb
      <ul>
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Preproces_Deptos.ipynb"> 
          Preproces_Deptos.ipynb</a>: </li>
          Este archivo hace el llamado del .csv de cada departamento teniendo en cuenta si es de vivienda, 
          personas, hogares o fallecidos; creando un nuevo csv con las variables seleccionadas para cada uno.
          Finalmente, une los csv en cuatro categorías: viviendas, personas, hogares o fallecidos; los cuales 
          contienen información de todos los departamentos.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Prom_Ciudades_Viviendas.ipynb"> 
          Prom_Ciudades_Viviendas.ipynb</a>: </li>
          Este archivo utiliza el csv creado por Preproces_Deptos.ipynb para viviendas, realiza el 
          preprocesamiento de cada una de las variables y exporta un archivo csv.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Prom_Ciudades_Personas_2.ipynb"> 
          Prom_Ciudades_Personas.ipynb</a>: </li>
          Este archivo utiliza el csv creado por Preproces_Deptos.ipynb para personas, realiza el 
          preprocesamiento de cada una de las variables y exporta un archivo csv.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Prom_Ciudades_Hogares.ipynb"> 
          Prom_Ciudades_Hogares.ipynb</a>: </li>
          Este archivo utiliza el csv creado por Preproces_Deptos.ipynb para hogares, realiza el 
          preprocesamiento de cada una de las variables y exporta un archivo csv. 
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Prom_Ciudades_Fallecidos.ipynb"> 
          Prom_Ciudades_Fallecidos.ipynb</a>: </li>
          Este archivo utiliza el csv creado por Preproces_Deptos.ipynb para fallecidos, realiza el 
          preprocesamiento de cada una de las variables y exporta un archivo csv.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Union_Dataset_Personas.ipynb"> 
          Union_Dataset_Personas.ipynb</a>: </li>
          Este archivo utiliza cada csv creado por Prom_Ciudades_Personas_2.ipynb, los une en un 
          único archivo, y se exporta como un archivo csv.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Union_datasets_final.ipynb"> 
          Union_datasets_final.ipynb</a>: </li>
          Este archivo utiliza los csv creados por Prom_Ciudades_Fallecidos.ipynb, 
          Prom_Ciudades_Hogares.ipynb, Prom_Ciudades_Viviendas.ipynb y Union_Dataset_Personas.ipynb, 
          unificándolos, generando así un archivo csv con toda la informacion del CNPV preprocesada.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Dataset_Inicial_Final.ipynb"> 
          Dataset_Inicial_Final.ipynb</a>: </li>
          Este archivo utiliza el csv creado por Union_datasets_final.ipynb y el archivo generado para 
          obtener la vulnerabilidad. se unifican para generar el dataset definitivo con todas la variables 
          relevantes del CNPV y la vulnerabilidad presentada por el DANE. Este dataset fue cargado en 
          <a href="https://www.kaggle.com/datasets/sebastianrgonzalez/initial-dane-covid19-dataset"> 
          Kaggle</a>.
        <li><a
          href="https://github.com/Sebas-Realpe/Indice_vul_COVID19/blob/main/Initial%20Index/Evaluacion_Modelo_Inicial_Clasificacion.ipynb"> 
          Evaluacion_Modelo_Inicial_Clasificacion.ipynb</a>: </li>
          Este archivo utiliza el csv creado por Dataset_Inicial_Final.ipynb para analizar los datos 
          y realizar una evaluación aplicando diferente algorítmos de Machine Learning (ML).
      </ul>