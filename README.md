# Animated-Chats-using-ggplot2-R-package
https://github.com/sujitkadam91/Animated-Chats-using-ggplot2-R-package.git


## Animated charts R codes 


#### Import some libraries

library(gapminder)

head(gapminder)

library(ggplot2)

library(plotly)

p1 <- ggplot(gapminder,aes(x=continent,y=gdpPercap,fill=continent))+
  geom_boxplot(aes(frame=year))
  
  
p1


ggplotly(p1)




## Animated Scatter plot



p2 <- ggplot(gapminder,aes(x=lifeExp,y=gdpPercap,fill=continent,size=pop))+
      geom_point(aes(frame=year,id= country))
      
      
p2

ggplotly(p2)
