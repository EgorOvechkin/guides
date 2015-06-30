# Требования к оформлению PR

Что сделать, чтобы ваш PR был принят быстро и с первого раза:
- В описании к PR должна содержаться ссылка на задачу JIRA, если такая задача есть
- Перед тем как оформить PR проверьте стилистическое оформление кода
  - Лишние пробелы
  - Форматирование многострочных конструкций
  - Форматирование сложных конструкций
- Декомпозируйте, декомпозируйте и еще раз декомпозируйте
  - Еще раз взгляните на куски кода - видите, что сложно выглядит - первый сигнал к декомпозиции
  - Не можете протестировать метод – значит, он написан плохо - декомпозируйте
  - Проблемы в личной жизни - декомпозируйте код
- Называйте переменные и методы так, чтобы через день, вспомнить, что они значат
  - Именование стоит делать не как быстрее, а как понятнее, даже если это набросок (нет ничего более постоянного, чем временное)
  - Непонятные имена методов только усложняют разработку, тебе самому
- Используйте только I18n. Это упростит жизнь в будущем
  - При переносе кода в плагин, вам придется это сделать, потому что у вас в проекте это платья, а где-то это трубы
  - Интернационализация должна использоваться везде, от контроллеров и моделей, до вьюшек
- Если вы изменяли хранимки в БД, обязательно положите их под гит, сначала положите, потом измените (отдельными коммитами)
  - Это упростит конфликты при изменении двумя людьми одной и той же хранимки
  - Это внесет ясность, при сложных обновлениях, пришедших с других проектов
- Всегда пишите тесты на свой код
- Проверяйте недочеты по всем файла из PR
  - Если вам в каком-то файле отметили недочет - обязательно проверьте все файлы PR на этот недочет, скорее всего - он не один такой
  - Очень полезно смотреть на свой PR глобально, лучше всего подходит GH
- Комментируйте проделанную работу
  - На данный момент нужно использовать TomDoc
  - Начните с описания того, что делает тот или иной модуль, класс, метод

# Требования к принятию PR
- PR обязательно должен быть просмотрен хотя бы одним разработчиком проекта, отличным от автора
- Проверяющий должен оставить подтверждение проверки в виде комментария к PR
- Должны пройти тесты
- Должны быть исправлены или согласованы все комментарии по оформлению кода (Hound)
- Все изменения которые производит автор после начала процесса ревью, должны быть сделаны в виде отдельных коммитов.
- После завершения процесса ревью и согласования, проверающий дает команду на rebase.
- Разработчик делает rebase, обновляет реквест, дает сигнл принимающему.
- Отвественный за репозиторий, принимает реквест.


Требования распространяются на любые PR в проект. PR не может быть принят в случае несоответствия требованиям к принятию PR. Ответственность за принятие PR несоответствующего требованиям несет человек, принявший PR.


В большинстве вопросов мы принимаем правила описанные в гайде: https://github.com/thoughtbot/guides/tree/master/code-review