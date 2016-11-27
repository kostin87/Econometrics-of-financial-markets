---
title       : Test 1
description : Тестирование по эконометрии
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise lang:r xp:100 skills:1 key:192e338017
## Выберите номер вашего варианта



*** =instructions
- Создайте переменную n и запишите туда номер вашего варианта.

*** =hint
- Use `n<- ваш вариант` 

*** =sample_code
```{r}


```

*** =solution
```{r}
n=1
```

*** =sct
```{r}
test_object("n", eval = FALSE)
```

--- type:NormalExercise lang:r xp:100 skills:1 key:98360b49d2
## Вычисление обычой доходности



*** =instructions 
- У вас есть цены актива spy.
- Вычислите обычную доходность для этого актива и запишите ее в переменную R.

*** =hint

*** =pre_exercise_code
```{r}
load(url("https://github.com/kostin87/Econometrics-of-financial-markets/raw/master/SPY.RData"))
spy=SPY[[1]][((n-1)*390+1):(n*390),2]
```

*** =sample_code
```{r}
R<-

```

*** =solution
```{r}
R<-diff(spy)/spy[-NROW(spy)]
```

*** =sct
```{r}
test_object("R")
```
