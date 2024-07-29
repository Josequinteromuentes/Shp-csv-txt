# Shp-csv-txt
Convertir archivos SHP a CSV y TXT en R

# Instalar los paquetes necesarios si no lo has hecho ya

install.packages("sf")
install.packages("readr")

# Cargar los paquetes

library(sf)
library(readr)

# Ruta al archivo SHP de entrada

input_shp <- "ruta/al/archivo.shp"

# Leer el archivo SHP

shp_data <- st_read(input_shp)

# Ruta para el archivo CSV de salida

output_csv <- "ruta/al/archivo_salida.csv"

# Exportar a formato CSV

write_csv(shp_data, output_csv)

# Ruta para el archivo TXT de salida

output_txt <- "ruta/al/archivo_salida.txt"

# Exportar a formato TXT (usando tabulaciones como separador)

write_delim(shp_data, output_txt, delim = "\t")

