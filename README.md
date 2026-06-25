# Clasificación Industrial Internacional Uniforme (CIIU) - Colombia

Este repositorio contiene un archivo [`ciiu.json`](./ciiu.json) con la estructura jerárquica completa de la **Clasificación Industrial Internacional Uniforme de todas las actividades económicas, Revisión 4 Adaptada para Colombia (CIIU Rev. 4 A.C.)**, basada en la normativa vigente del DANE.

## ¿Qué es la CIIU?

La **Clasificación Industrial Internacional Uniforme (CIIU)** es una clasificación de actividades económicas por procesos productivos. Su propósito principal es:

> *"ofrecer un conjunto de categorías de actividades que se pueda utilizar para la reunión, análisis y presentación de estadísticas de acuerdo con esas actividades."* [Fuente: DANE](https://www.dane.gov.co/index.php/sistema-estadistico-nacional-sen/normas-y-estandares/nomenclaturas-y-clasificaciones/clasificaciones/clasificacion-industrial-internacional-uniforme-de-todas-las-actividades-economicas-ciiu)

En Colombia, el DANE es la entidad encargada de adaptar y mantener esta clasificación. La versión aquí representada corresponde a la **CIIU Rev. 4 A.C.**, actualizada mediante la [Resolución 2306 de 2022](https://www.dane.gov.co/files/acerca/Normatividad/resoluciones/2022/Resolucion-2306-de-2022.pdf).

## Estructura del Archivo JSON

El archivo `ciiu.json` organiza la clasificación en cuatro niveles jerárquicos:

* **Sección**: identificada con una letra (ej. `"A"`, `"B"`, `"C"`).
* **División**: código de dos dígitos (ej. `"01"`, `"02"`).
* **Grupo**: código de tres dígitos (ej. `"011"`, `"012"`).
* **Clase**: código de cuatro dígitos (ej. `"0111"`, `"0112"`).

Cada nivel incluye su código y descripción correspondiente.

### Ejemplo de la estructura:

```json
{
  "secciones": [
    {
      "codigo": "A",
      "descripcion": "AGRICULTURA, GANADERÍA, CAZA, SILVICULTURA Y PESCA",
      "divisiones": [
        {
          "codigo": "01",
          "descripcion": "Agricultura, ganadería, caza y actividades de servicios conexas",
          "grupos": [
            {
              "codigo": "011",
              "descripcion": "Cultivos agrícolas transitorios",
              "clases": [
                {
                  "codigo": "0111",
                  "descripcion": "Cultivo de cereales (excepto arroz), legumbres y semillas oleaginosas"
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}