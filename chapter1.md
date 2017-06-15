---
title       : Самая первая глава
description : Она очень важна
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise lang:r xp:100 skills:1 key:1a09e3a5db
## О пользе графиков

В этом упражнении Винни-Пух построит гистограмму


*** =instructions
- С помощью функции `qplot` из заранее подргуженного Пятачком пакета `ggplot2` Винни-Пуху предстоит построить гистограмму вектора из 100 нормальных случайных величин.

*** =hint
- Создать вектор можно командой `rnorm(...)`, указав в скобках количество.

*** =pre_exercise_code
```{r}
# кириллица в комменте
library(ggplot2)

```

*** =sample_code
```{r}
set.seed(42)
# Кодь туточки

```

*** =solution
```{r}
set.seed(42)
qplot(rnorm(100))

```

*** =sct
```{r}
bad_arg_message <- "У функции qplot должен быть подходящий аргумент"
no_arg_message <- "У функции qplot должен быть аргумент"
no_fun_message <- "Функцию qplot использовал?"
test_function("qplot", args = "x",
              not_called_msg = no_fun_message,
              incorrect_msg = bad_arg_message)
test_function("rnorm", args = "n",
              not_called_msg = "Функцию rnorm неплохо бы позвать",
              incorrect_msg = "А ещё у функции rnorm нужно указать правильный аргумент")
success_msg("Ты крутой перец!!!")
```
