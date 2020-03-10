# Курс "Функциональное программирование" на КТ

## Полезные ссылки

* [Страница с материалами курса](https://github.com/jagajaga/FP-Course-ITMO).
* [Табличка с баллами](https://docs.google.com/spreadsheets/d/13JBmxwb_N2yuqRABSsyF5gELZkHX3GCZ_grjttq7AJ0/).
* [Style-guide](code-style.md).
* [Рекомендуемая конфигурация stylish-haskell](.stylish-haskell.yaml).
* [Рекомендации по настройке рабочего окружения](environment-setup.md).

## Домашние задания

* [ДЗ #0](hw0.md)
* [ДЗ #1](hw1.md)

## Как происходит обучение
В течение семестра раз в неделю Вам будут читаться лекции о языке Haskell. Посещение лекций не влияет на возможность получения зачета.

По прошествии нескольких тем Вам будут выдаваться домашние задания на эти темы. Обычно новое домашнее задание выдается после 3-4х лекций и содержит задачи на темы лекций. На решение каждого домашнего задания отводится 3 недели с момента его выдачи.

## Коллоквиумы
В течение курса будет проведено 3 коллоквиума, на которых будет спрашиваться теоретический материал по всем пройденым с прошлого коллоквиума темам.

## Домашние задания

Как уже было сказано, в каждом домашнем задании будет несколько задач. Каждая задача оценивается в несколько баллов.
У некоторых задач будут _advanced_ версии, которые будут представлять усложненную версию задачи  и оцениваться большим количеством баллов. Сумма баллов за все _advanced_ версии задач равна 100 баллам.

### Требования к выполнению
* Домашние задания необходимо выполнять **самостоятельно**. Под *самостоятельно* подразумевается, что студент написал код *сам*, без помощи в написании другим студентом, без копирования кода из Интернета и других источников, которые не были разрешены явно.
* Если окажется, что два или более студента списали друг у друга код, баллы за списанную задачу у них будут аннулированы вне зависимости от того, кто списал, а кто дал списать.
* Имейте в виду, что Ваше решение будет трактоваться как списанное, если Вы и другой студент независимо друг от друга скопировали код из некоторого публичного источника в Интернете (например, туториала и/или публичного github репозитория), и этот источник не был оговорен в задании как разрешенный.
* Если есть подозрения, что Вы списали решение задачи, преподаватель вправе попросить Вас объяснить код. В этом случае для зачета задачи необходимо полностью понимать и уметь объяснять его.

Решения задач, которые будут признаны как списанные, будут помечаться красным в таблице и аннулироваться.

Решения задач, которые подозреваются как списанные, будут помечаться желтым в таблице и аннулироваться до тех пор, пока студент не докажет, что он полностью понимает код.

### Формат сдачи
Ожидается, что каждый студент заведет один приватный репозиторий на github.com для всех домашних заданий, в который добавит как коллаборатов преподавателей курса (github: jagajaga, georgeee, rvem)

Репозиторий должен иметь следующую структуру:
https://github.com/jagajaga/fp-homework-templates-2020

Чтобы сдать домашнее задание, необходимо отправить на почту курса fp.ctd.itmo@serokell.io письмо с ссылкой на коммит в Вашем репозитории, в котором сделано это домашнее задание.
Письмо должно иметь следующий формат:
```
Subject: ДЗX
Body:
https://github.com/jagajaga/fp-homework-templates/commit/aefa5b04cce75323ce89825e3820cdea58841e8a
Иванов Иван, группа 333Y
```
где `X` - это номер домашнего задания (0, 1, 2, ...).
Отправить письмо необходимо до истечения дедлайна по домашнему заданию.

### Проверка домашних заданий
#### Онлайн проверка
После того как дедлайн по домашнему заданию прошел, преподаватели в первую очередь проверяют Ваши решения на предмет списывания.
Те решения, которые окажутся списанными или подозреваются как списанные, аннулируются в таблице с особой пометкой.
Остальные же решения просматриваются преподавателями.

Прежде всего, чтобы Ваше решение было оценено, необходимо чтобы оно собиралось `stack build`.

Баллы за задачу могут снижаться за:
* невыполнение [style-guide](https://github.com/serokell/serokell-core/blob/master/serokell-style.md) - 0.5 балла за каждый тип стилистической ошибки;
* непроходящий тест - 0.5 балла за каждый тест;
* lts в stack.yaml отличающийся от требуемого - 0.5 балла;
* за "некрасивый код", написание велосипедов - 0.5-1 балл;
* за логические ошибки (например, за невыполнение законов тайпклассов для инстансов, и т.д.) - 0.5-1 балл;
* за невыполнения всех требований задачи (например, требуемой асимптотики, использования требуемых функций и т.д.) - от 0.5 до стоимости задачи баллов.

Имейте в виду, что Вы можете получить отрицательное количество баллов за задачу.

Баллы за задачу могут повышаться за:
* "красивый" код: обобщенные типы функций, грамотно спроектированная архитектура, использование функциональности языка, которая не разбиралась на лекциях и т.д.
* перевыполнение требований задачи: задача реализована с лучшей асимптотикой, чем требовалось, написаны тесты и т.д.

По умолчанию будет происходить **только** онлайн-проверка.

#### Офлайн-проверка
Если желающих сдавать домашние задания будет немного, то преподаватели вправе проводить офлайн-проверку: очную сдачу, при которой студент должен будет продемонстрировать код и ответить на возникающие по ходу проверки вопросы. Об офлайн-проверке задания будет сообщено заранее.

Офлайн-проверка предполагает все те же самые требования (решение выполнено самостоятельно, студент полностью понимает и может объяснить код и т.д.) и условия на снижения и повышения баллов.

## Дополнительные возможности заработать баллы (TBD)
Кроме получения баллов за домашние задания, есть дополнительные возможности заработать баллы.

### IDE
Вы можете попробовать улучшить какую-нибудь Haskell IDE, например: Intellij IDEA на языке Scala, Haskell plugin для Emacs и т.д.

Количество баллов, которое Вы можете заработать, зависит от количества сделанного. Перед выполнением лучше согласовать с преподавателями.

### Issues и PRs
Вы можете попробовать улучшить некоторые существующие библиотеки языка Haskell, исправив некоторые issues в github репозиториях или сделав новые улучшения.
Например, Вы можете попробовать улучшить следующие библиотеки:
* https://github.com/serokell/universum
* https://github.com/serokell/xrefcheck
* https://github.com/serokell/nixfmt
* https://github.com/serokell/haskell-utf8

Количество баллов, которое Вы можете заработать, зависит от количества сделанного. Перед выполнением лучше согласовать с преподавателями.

### Slides
За поиск ошибок и опечаток в слайдах нашего курса будут даваться баллы. Вы также можете предлагать более хорошие примеры и прочие улучшения слайдов.

Количество баллов, которое можно получить, зависит от улучшения, но будет лежать в пределах от 0.5 до 3х баллов.

### Отзывы о лекциях
После некоторых лекций студентам будет предложено оставить отзыв о том, насколько им понравилась лекция и какие были недочеты, по их мнению.

Чтобы избежать случаев, когда студент даже не был на лекции, но оставляет отзыв, неанонимные отзывы будут поощряться в 0.5 баллов.

## Как получить зачет?
Есть три способа получить зачет. ~Три стула.~

### Способ 1 (автомат).
Чтобы автоматом получить зачет, необходимо сдать все коллоквиумы и все _advanced_ версии домашних заданий.

### Способ 2 (полуавтомат).
Чтобы получить зачет данным способом, необходимо выполнить следующие условия:
* сдать 2 из 3 коллоквиумов;
* cдать все домашние задания;
* сдать письменный экзамен (теоретический минимум).

### Способ 3 (страдание).
Чтобы получить зачет данным способом, необходимо выполнить следующие условия:
* набрать не менее 60 баллов в течение семестра;
* сдать письменный экзамен (теоретический минимум);
* сдать устный экзамен.

#### Письменный экзамен
Письменный экзамен представляет собой письменную работу, в которой будет 13 вопросов по разным темам, затронутым в лекциях. Обычно для ответа на вопрос необходимо дать короткий ответ или написать некоторый небольшой кусочек кода. Предполагается, что все знания, нужные для ответа на вопрос, были рассказаны Вам на лекциях.

Каждый вопрос оценивается от 0 до 1 баллов (например, Вы можете получить 0.7 баллов за неточный ответ на вопрос).
То есть максимум за письменную работу можно получить 13 баллов. Количество баллов, которое Вам нужно набрать на письменном экзамене, чтобы его сдать, зависит от количества баллов, которые вы получили за семестр. Чем больше у Вас баллов набранно за семестр --- тем меньше нужно набрать на письменном экзамене.
Конкретные условия такие:  
`>= 60` за семестр --- `>= 10` за письменный экзамен  
`>= 70` за семестр --- `>= 9` за письменный экзамен  
`>= 80` за семестр --- `>= 8` за письменный экзамен  
`>= 90` за семестр --- `>= 7` за письменный экзамен 


#### Устный экзамен
Да, предмет зачетный, но устный экзамен все равно придется сдать, чтобы получить зачет.

~Ребят, зря вы сюда поступили... Оно вас сожрет. Бегите отсюда...~

На экзамене Вы тянете билет, номер которого соответствует расказанной Вам лекции [отсюда](https://github.com/jagajaga/FP-Course-ITMO), у Вас есть 10 минут, чтобы воспользоваться своими записями или ноутбуком, после этого Вы можете еще некоторое время готовиться, но уже без каких либо материалов.
