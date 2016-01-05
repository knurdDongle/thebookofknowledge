# Code Review.
Просмотр кода это один из важных аспектов проверки качества. На этом этапе есть возможность отследить самые крупные и видимые ошибки, которые могут быть как на уровне логики приложения, так и в самом коде. Так как в ревью всегда присутствуют как минимум два человека: тот кто написал код и тот, кто его проверяет, то рекомендации мы приводятся как для одного так и для другого.

## Общее
* Самое главное — понимать, что в программировании зачастую нет «серебряной пули» для решения задач. Есть только варианты того, как можно сделать, на которые влияет множество факторов. Отсюда следует, что если код не нравится, то в первую очередь стоит обсудить, почему он написан именно так и постараться прийти к решению по тому, что с ним делать.
* В некоторых случаях возможно несоблюдение некоторых стандартов и откладывание рефакторинга на потом (конечно, если при этом код полностью работает) при условии создания Issues на это будущее изменение.
* Задавайте вопросы, не требуйте.
* Если что-то непонятно, попросите прояснить
* Старайтесь быть как можно более точным в своих формулировках.
* Если в ходе проверки возникло слишком много вопросов, лучше обсудить это лично и по факту обсуждения написать комментарий, который суммирует всё, что было написано.
* По возможности стоит избегать обсуждений, которые напрямую не относятся к текущему PR, а если они возникают, то всегда можно обсудить это в общем чате ;)

## Создатель PR
* Ваша самая главная задача в рамках PR — это получить отзывы о том коде, который вы написали для решения задачи.
* При создании PR в комментарии к нему следует указать:
    * Какая именно задача решается данным пулом. В данном случае лучше всё-таки описывать своими словами, но в краткой форме. Также можно привести ссылку на конкретную задачу в issue tracker
    * Что необходимо сделать для того, что бы проверить, что задача решена и всё работает именно так, как и должно работать. Тут можно указать урлы, которыми можно воспользоваться, дополнительные сведения и прочее.
* После этого стоит ещё раз внимательно посмотреть на все свои изменения, возможно уже при этом просмотре будет найденно что-то, что было не видно до этого.
* При получении комментариев к своему реквесту, необходимо по возможности ответить на них все. Понятно, что иногда стоит отстоять свою позицию, иногда стоит согласиться с теми комментариями, которые вам предлагают.

## Проверяющий
* Самая главная ваша задача как проверяющего — помочь довести тому человеку, который писал код, его задачу до логического конца, когда код полностью работает, соответствует стандартам и выполняет ровно то, что требуется по условиям задачи.
* Первым делом проверям код на соответствие [стандартам кодирования принятым в Evercode](https://github.com/EvercodeLab/thebookofknowledge/tree/master/code_style)
* Далее просматриваем код на наличие различных логических ошибок
* Следующим шагом просматриваем выполняет ли код задачу, которая ставилась перед его написанием. Если да, то есть ли возможность улучшить этот код? Есть ли в нём дублирование?
* Если для данного кода можно написать тест, написан ли он? Если написан, то проходит ли он?
* Последним шагом будет проверка кода на работоспособность. Для этого можно выполнить действия указанные в описании PR. Лучше, если при этом будут ещё проверены граничные значения.