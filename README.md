# 18.marzo.2016
descomponer o separar series de tiempo (parte1)

### 18 de marzo de 2016 ###
## descomponer osepara una serie de tiempo ##

tdesoc <-sample(3:8,60,replace=T)
tdesoc <- ts (dato1, start = c(2005,1), frequency = 12)
tdesoc.de <- decompose(tdesoc) 
names(tdesoc.de)
plot(tdesoc.de)
plot(decompose(tdesoc)) ## grafica
trend <- tdesoc.de$trend ## tendencia
season <- tdesoc.de$seasonal ## error
tdesoc.dom <- decompose(tdesoc, type = "mult") ## para separar la serie de tiempo con el modelo multiplicativo
## tambien podemos obtener la tendencia y el error (trend y seasonal) pero seria del modelo multiplicativo

