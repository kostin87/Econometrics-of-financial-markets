---
title       : Test 1
description : Тестирование по эконометрии
attachments :


--- type:NormalExercise lang:r xp:100 skills:5 key:98360b49d2
## Вычисление обычой доходности



*** =instructions 
- У вас есть цены актива spy.
- Вычислите обычную доходность для этого актива и запишите ее в переменную R.

*** =hint

*** =pre_exercise_code
```{r}
n=round(runif(1, min = 1, max = 30))
load(url("http://s3.amazonaws.com/assets.datacamp.com/production/course_2233/datasets/SPY.RData"))
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

--- type:NormalExercise lang:r xp:100 skills:5 key:61f0a215c8
## Вычисление логарифмической доходности



*** =instructions 
- У вас есть цены актива spy.
- Вычислите логарифмическую доходность для этого актива и запишите ее в переменную r.

*** =hint

*** =pre_exercise_code
```{r}
n=round(runif(1, min = 1, max = 30))
load(url("http://s3.amazonaws.com/assets.datacamp.com/production/course_2233/datasets/SPY.RData"))
spy=SPY[[1]][((n-1)*390+1):(n*390),2]
```

*** =sample_code
```{r}
r<-

```

*** =solution
```{r}
r<-diff(log(spy))
```

*** =sct
```{r}
test_object("r")
```