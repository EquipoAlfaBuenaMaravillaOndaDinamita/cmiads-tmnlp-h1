
# Instrucciones para instalar

## Crear ambiente virtual

```bash
python3 -m venv venv

# windows
./venv/Scripts/activate

# instalar librerias
pip install -r requirements.txt
``` 

## Ejecutar crawler
```bash
scrapy crawl pagination
```

# Descripción
Se hizo un scrapper de reviews de hoteles de tripadvisor. Se tomó como base los hoteles de cierta URL base. En este caso se tomaron hoteles de Antigua Guatemala (https://www.tripadvisor.com/Hotels-g295366-Antigua_Sacatepequez_Department-Hotels.html).

El programa itera sobre H hoteles y de cada hotel extrae R reviews (se consideró el pagineo para extraer los hoteles y reviews necesarios). En código se dejó configurado para iterar con H=50 hoteles y R=500 reviews/hotel  

# Resultado
Se utilizó un formato JSON para guardar el resultado. Se guarda en el archivo *result.json*. El JSON tiene los siguientes campos:
- **url**: link del hotel evaluado
- **hotel_name**: nombre del hotel evaluado
- **rating_value**: valor entre 0 y 50 con la calificación
- **rating**: clasificación del rating_value (Excelent, Very Good, Average, Poor, Terrible)
- **reviewer**: nombre del evaluador
- **title**: título del review
- **review**: texto completo del review

# Contribuciones
Grupo 3 en canvas
- Kevin García: repositorio, crawler base con parse de reviews
- Martín Guzmán: parse por hotel y cálculo de rating