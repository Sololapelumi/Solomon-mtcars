# Solomon-mtcars
mtcars and Usarrests
######### Assignment 1 #######
library(datasets)
data("USArrests")
head(USArrests)
nrow(USArrests)
ncol(USArrests)
?USArrests
attach(USArrests)
summary(USArrests)
Murder_Assault <- subset(USArrests, select = c(Murder, Assault))
Murder_Assault
Reg_Anal <- lm(Murder ~ Assault)
summary(Reg_Anal)
Murder_Urbanpop <- subset(USArrests, select = c(Murder, UrbanPop))
Murder_Urbanpop
Reg_Anal2 <- lm(Murder ~ UrbanPop)
summary(Reg_Anal2)

######## INTERPRETATION 1 ##########
######## For the Regression of Murder against Assault, we have that the relationship
######## between Murder and Assault is positive, that is, as the number of assault 
######## increases the number of murder also increases. We can accept the null 
######## hypothesis that there is a significant relationship between Murder and 
######## Assault.

######## INTERPRETATION 2 ##########
######## For the Regression of Murder against Urban Population, we have that the
######## relationship between Murder and Urban Population is positive, that is, 
######## as the number of assault increases, the number of murder also increases 
######## though almost insignificant. We will reject the null hypothesis a significant 
######## relationship between Murder and Urban Population.


######## Assignment 2 ########
data("mtcars")
head(mtcars)
nrow(mtcars)
ncol(mtcars)
?mtcars
attach(mtcars)
summary(mtcars)
am_gear <- subset(mtcars, select = c(am, gear))
am_gear
Reg_Anal3 <- lm(am ~ gear)
summary(Reg_Anal3)
drat_carb <- subset(mtcars, select = c(drat, carb))
drat_carb
Reg_Anal4 <- lm(drat ~ carb)
summary(Reg_Anal4)

######## INTERPRETATION 3 ##########
######## For the Regression of am against gears, we have that the relationship
######## between Murder and Assault is positive, that is, as the number of gears 
######## increases the number of murder also increases. We can accept the null 
######## hypothesis that there is a significant relationship between am and 
######## gears.

######## INTERPRETATION 4 ##########
######## For the Regression of drat against carb, we have that the relationship
######## between drat and carb is negative, that is, as the number of drat 
######## increases the number of carb decreases. We will reject the null 
######## hypothesis that there is a significant relationship between drat and 
######## carb.
