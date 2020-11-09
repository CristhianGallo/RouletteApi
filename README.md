# RouletteApi
Project designed for appliying to back end software developer on masivian
How to run

Proyecto creado con Spring Boot, por lo cual puede ser ejecutado usando el IDE de Spring tools

1 - Crear ruleta: localhost:8080/create

2 - Abrir ruleta:  localhost:8080/open?id=43 
      Donde "id" es el identificador de la ruleta previamente creada

3 - Apostar:       http://localhost:8080/bet     
     Como headers se deben enviar:
     A:  Content-Type  --> Valor: "application/json"
     B:  user_id --> Valor: "Cualquier cadena de texto o numero"
     Ejemplos del body que se debe enviar:
 Ejemplo 1:
    {
        "color": "negro",
        "rouletteId": "40",
        "betMoneyAmount": 5000
    }
Ejemplo 2:
   {
        "number": 16,,
        "rouletteId": 40,
        "betMoneyAmount": 5000
   }

3 - Ejecutar ruleta:     localhost:8080/executeRulette?id=11
          Donde "id" es el identificador de la ruleta que debe estar en estado "Abierta"

4 - Obtener todas las ruletas:   localhost:8080/getAllRouletes
   
NOTA: La base de datos que se utiliza, es una base de datos MySQL en la nube, usando la herramienta gratuita "https://remotemysql.com", por lo cual no hay necesidad de configuraciones adicionales para ejecutar el proyecto.
