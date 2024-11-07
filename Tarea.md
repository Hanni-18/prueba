# Desafios
especies <- data.frame(
     especie = c("Ajolote", "Rana", "Serpiente", "Tortuga"),
     habitat = c("Lago", "Río", "Bosque", "Lago"),
     tamano = c(30, 10, 150, 50),
     peso = c(150, 25, 1000, 500)
 )
especies_fil <- filter(especies, habitat == "Lago")
especies_fil
  especie habitat tamano peso
1 Ajolote    Lago     30  150
2 Tortuga    Lago     50  500
especies_ord <- especies_fil[order(especies_fil$tamano), ]
especies_ord
  especie habitat tamano peso
1 Ajolote    Lago     30  150
2 Tortuga    Lago     50  500
especies_ord2 <- especies[order(especies$tamano), ]
especies_ord2
    especie habitat tamano peso
2      Rana     Río     10   25
1   Ajolote    Lago     30  150
4   Tortuga    Lago     50  500
3 Serpiente  Bosque    150 1000
str(iris)
'data.frame':	150 obs. of  5 variables:
 $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
 $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
 $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
 $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
 $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
library(ggplot2)
library(hrbrthemes)
graf_d<-ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, alpha=Species))+
     geom_point(size=6, color="#69b3a2") +
     ggtitle("Gráfico de dispersión") +
     theme_ipsum()

> especies_ord2 <- especies[order(especies$tamano), ]
> especies_ord2
    especie habitat tamano peso
2      Rana     Río     10   25
1   Ajolote    Lago     30  150
4   Tortuga    Lago     50  500
3 Serpiente  Bosque    150 1000
> str(iris)
'data.frame':	150 obs. of  5 variables:
 $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
 $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
 $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
 $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
 $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
> library(ggplot2)
> library(hrbrthemes)
Error en library(hrbrthemes): no hay paquete llamado ‘hrbrthemes’
> install.packages("hrbrthemes")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
also installing the dependencies ‘fontBitstreamVera’, ‘fontLiberation’, ‘base64enc’, ‘digest’, ‘fastmap’, ‘extrafontdb’, ‘Rttf2pt1’, ‘fontquiver’, ‘htmltools’, ‘systemfonts’, ‘extrafont’, ‘gdtools’


  There is a binary version available but the
  source version is later:
        binary source needs_compilation
gdtools  0.4.0  0.4.1              TRUE

  Binaries will be installed
probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/fontBitstreamVera_0.1.1.zip'
Content type 'application/zip' length 697821 bytes (681 KB)
downloaded 681 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/fontLiberation_0.1.0.zip'
Content type 'application/zip' length 4530297 bytes (4.3 MB)
downloaded 4.3 MB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/base64enc_0.1-3.zip'
Content type 'application/zip' length 33130 bytes (32 KB)
downloaded 32 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/digest_0.6.37.zip'
Content type 'application/zip' length 223346 bytes (218 KB)
downloaded 218 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/fastmap_1.2.0.zip'
Content type 'application/zip' length 135482 bytes (132 KB)
downloaded 132 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/extrafontdb_1.0.zip'
Content type 'application/zip' length 10611 bytes (10 KB)
downloaded 10 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/Rttf2pt1_1.3.12.zip'
Content type 'application/zip' length 152377 bytes (148 KB)
downloaded 148 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/fontquiver_0.2.1.zip'
Content type 'application/zip' length 2279036 bytes (2.2 MB)
downloaded 2.2 MB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/htmltools_0.5.8.1.zip'
Content type 'application/zip' length 363458 bytes (354 KB)
downloaded 354 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/systemfonts_1.1.0.zip'
Content type 'application/zip' length 1337871 bytes (1.3 MB)
downloaded 1.3 MB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/extrafont_0.19.zip'
Content type 'application/zip' length 57152 bytes (55 KB)
downloaded 55 KB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/gdtools_0.4.0.zip'
Content type 'application/zip' length 2207179 bytes (2.1 MB)
downloaded 2.1 MB

probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/hrbrthemes_0.8.7.zip'
Content type 'application/zip' length 898191 bytes (877 KB)
downloaded 877 KB

package ‘fontBitstreamVera’ successfully unpacked and MD5 sums checked
package ‘fontLiberation’ successfully unpacked and MD5 sums checked
package ‘base64enc’ successfully unpacked and MD5 sums checked
package ‘digest’ successfully unpacked and MD5 sums checked
package ‘fastmap’ successfully unpacked and MD5 sums checked
package ‘extrafontdb’ successfully unpacked and MD5 sums checked
package ‘Rttf2pt1’ successfully unpacked and MD5 sums checked
package ‘fontquiver’ successfully unpacked and MD5 sums checked
package ‘htmltools’ successfully unpacked and MD5 sums checked
package ‘systemfonts’ successfully unpacked and MD5 sums checked
package ‘extrafont’ successfully unpacked and MD5 sums checked
package ‘gdtools’ successfully unpacked and MD5 sums checked
package ‘hrbrthemes’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\Alumno\AppData\Local\Temp\RtmpG4u6wW\downloaded_packages
> graf_d<-ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, alpha=Species))+
+     geom_point(size=6, color="#69b3a2") +
+     ggtitle("Gráfico de dispersión") +
+     theme_ipsum()
Error en theme_ipsum(): no se pudo encontrar la función "theme_ipsum"
> install.packages("ggplot2")
Error in install.packages : Updating loaded packages
> install.packages("ggplot2")
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
Warning in install.packages :
  package ‘ggplot2’ is in use and will not be installed
> library(ggplot2)
> graf_d<-ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, alpha=Species))+
+     geom_point(size=6, color="#69b3a2") +
+     ggtitle("Gráfico de dispersión") +
+     theme_ipsum()
Error en theme_ipsum(): no se pudo encontrar la función "theme_ipsum"
> install.packages("gcookbook") 
WARNING: Rtools is required to build R packages but is not currently installed. Please download and install the appropriate version of Rtools before proceeding:

https://cran.rstudio.com/bin/windows/Rtools/
probando la URL 'https://cran.rstudio.com/bin/windows/contrib/4.4/gcookbook_2.0.zip'
Content type 'application/zip' length 3897968 bytes (3.7 MB)
downloaded 3.7 MB

package ‘gcookbook’ successfully unpacked and MD5 sums checked

The downloaded binary packages are in
	C:\Users\Alumno\AppData\Local\Temp\RtmpG4u6wW\downloaded_packages
> library(gcookbook)
> graf_d<-ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, alpha=Species))+
+     geom_point(size=6, color="#69b3a2") +
+     ggtitle("Gráfico de dispersión") +
+     theme_ipsum()
Error en theme_ipsum(): no se pudo encontrar la función "theme_ipsum"
> graf_d<-ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, alpha=Species))+
+     geom_point(size=6, color="#69b3a2") +
+     ggtitle("Gráfico de dispersión") 
> graf_d
Aviso:
Using alpha for a discrete variable is not advised. 
> calificaciones <- data.frame(
+     estudiante = c("Ana", "Carlos", "Lucía", "Jorge", "Ana", "Carlos", "Lucía", "Jorge"),
+     asignatura = c("Matemáticas", "Matemáticas", "Matemáticas", "Matemáticas", "Historia", "Historia", "Historia", "Historia"),
+     calificacion = c(95, 85, 92, 88, 78, 82, 85, 90)
+ )
> promedio_calificaciones <- calificaciones %>%
+     group_by(estudiante) %>%
+     summarise(promedio = mean(calificacion))
> promedio_calificaciones
# A tibble: 4 × 2
  estudiante promedio
  <chr>         <dbl>
1 Ana            86.5
2 Carlos         83.5
3 Jorge          89  
4 Lucía          88.5
> alturas <- alturas %>%
+     mutate(altura_m = altura_cm / 100)
Error: objeto 'alturas' no encontrado
> alturas <- data.frame(
+     nombre = c("Laura", "Pedro", "Sara", "Miguel"),
+     altura_cm = c(160, 175, 150, 180)
+ )
> alturas <- alturas %>%
+     mutate(altura_m = altura_cm / 100)
> alturas
  nombre altura_cm altura_m
1  Laura       160     1.60
2  Pedro       175     1.75
3   Sara       150     1.50
4 Miguel       180     1.80
> ventas <- data.frame(
+     mes = c("Enero", "Febrero", "Marzo", "Abril", "Mayo", "Junio"),
+     ventas = c(12000, 15000, 13000, 16000, 17500, 14000)
+ )
> ggplot(ventas, aes(x = mes, y = ventas, fill = mes)) +
+     geom_bar(stat = "identity") +
+     labs(title = "Ventas Mensuales",
+          x = "Mes",
+          y = "Ventas") +
+     theme_minimal() +
+     scale_fill_brewer(palette = "Set3")
> productos <- data.frame(
+     producto = c("A", "B", "C", "D"),
+     precio = c(20, 35, 50, 10),
+     cantidad_vendida = c(100, 200, 150, 250)
+ )
> 
> productos <- productos %>%
+     mutate(ingreso_total = precio * cantidad_vendida)
> productos
  producto precio cantidad_vendida ingreso_total
1        A     20              100          2000
2        B     35              200          7000
3        C     50              150          7500
4        D     10              250          2500
ggplot(mtcars, aes(x = factor(cyl), y = mpg, fill = factor(cyl))) +
+     geom_boxplot() +
+     labs(title = "Distribución de MPG según el Número de Cilindros",
+          x = "Número de Cilindros",
+          y = "Millas por Galón (MPG)") +
+     scale_fill_manual(values = c("4" = "white", "6" = "pink", "8" = "coral")) + 
+     theme_dark()
