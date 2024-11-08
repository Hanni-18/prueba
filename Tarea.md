# Desafios
## Primer desafío: Filtrar y manipular data frames
```ruby
#install.packages("dplyr")
library(dplyr)
especies <- data.frame(
     especie = c("Ajolote", "Rana", "Serpiente", "Tortuga"),
     habitat = c("Lago", "Río", "Bosque", "Lago"),
     tamano = c(30, 10, 150, 50),
     peso = c(150, 25, 1000, 500)
)
```
![especies 1](https://github.com/user-attachments/assets/b6d1bd85-2959-421d-97df-38d71912581d)
```ruby
especies_fil <- filter(especies, habitat == "Lago")
especies_fil
```
![especies 2](https://github.com/user-attachments/assets/9c1b2ea0-702f-469b-ba91-5c73954c1be4)
```ruby
especies_ord <- especies_fil[order(especies_fil$tamano), ]
especies_ord
```
![especies 3](https://github.com/user-attachments/assets/9844c4a1-fb93-46e7-a8fa-3878dda6dbf9)
```ruby
especies_ord2 <- especies[order(especies$tamano), ]
especies_ord2
```
![especies 4](https://github.com/user-attachments/assets/596bbb68-ecc2-4092-86ce-1f39bba54e94)

## Segundo desafío: Generación de gráficos
```ruby
#install.packages("ggplot2")
library(ggplot2)
# install.packages("hrbrthemes")
library(hrbrthemes)
#install.packages("gcookbook")
library(gcookbook)
str(iris)
'data.frame':	150 obs. of  5 variables:
 $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
 $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
 $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
 $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
 $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
graf_d<-ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, alpha=Species))+
     geom_point(size=6, color="#69b3a2") +
     ggtitle("Gráfico de dispersión") +
     theme_ipsum()




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
