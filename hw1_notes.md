Основное

<span style="color:green"> &#x2611; </span> Классические операции matmul и matvec

<span style="color:green"> &#x2611; </span> Статическая линковка

<span style="color:green"> &#x2611; </span> Флаги -g и -O3

<span style="color:green"> &#x2611; </span> Вызов из python

Дополнительное:

<span style="color:green"> &#x2611; </span> BLAS

<span style="color:green"> &#x2611; </span> LINPACK

<span style="color:red"> &#x2612; </span> Штрассен

Заметки:

1. Порядок линковки иногда приводит к ошибкам компиляции (видимо зависит от операционной системы, у меня на Linux нужно было сначала линковать ``-lmatrix`` и только потом ``-lopenblas``, иначе вылезала ошибка).

2. Тип ``clock_t`` может работать cpu time, а не wall time. Он еще и по разному себя ведет на Windows и на Linux. Наверное есть какой-то вариант, который точно возвращает wall time и причем кроссплатформенный.

Ссылки: [linking order](https://stackoverflow.com/questions/45135/why-does-the-order-in-which-libraries-are-linked-sometimes-cause-errors-in-gcc), [wall/cpu time](https://stackoverflow.com/questions/17432502/how-can-i-measure-cpu-time-and-wall-clock-time-on-both-linux-windows)
