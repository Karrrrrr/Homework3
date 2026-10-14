Пользовательские роли:
	- пользователь

Пользовательские сценарии:
	- обзор подписок
	- создание подписки
	- редактирование подписки
	- удаление подписки
	- просмотр статистики
	- получение уведомлений о предстоящих списаниях
	- импорт подписок из стороннего приложения/сервиса
	- изменение категорий подписок

Must have User Stories:
	- Как пользователь я хочу просматривать список своих подписок, чтобы видеть, какие подписки у меня есть
	Критерий приёмки: Given user created subscriptions When user opens app Then list of subscriptions is shown
	- Как пользователь я хочу создавать новые подписки, они появились в списке моих подписок
	Критерий приёмки: Given user opened app When user creates new subscription Then subscription appears on main page
	- Как пользователь я хочу редактировать свои подписки, чтобы вносить изменения в информацию о подписках
	Критерий приёмки: Given user created subscriptions When user edits subscription Then updated information about subscription is shown
	- Как пользователь я хочу удалять подписки, чтобы больше не отслеживать те подписки, которые мне не нужны
	Критерий приёмки: Given user created subscription When user deletes subscription Then subscription disappears from main page

Should have User Stories:
	- Как пользователь я хочу просматривать статистику, чтобы получать информацию о списаниях в разрезе месяца/года
	Критерий приёмки: Given user used app for month/year When user opens statistics page Then statistics for month/year calculate
	- Как пользователь я хочу получать уведомления о предстоящих списаниях, чтобы знать, сколько денег, когда и на что спишется с моего счёта
	Критерий приёмки: Given user has subscriptions When it's withdrawal for one of the subscription is tomorrow Then push notification is shown to user

Nice to have User Stories:
	- Как пользователь я хочу импортировать подписки из стороннего приложения/сервиса, чтобы быстро получить список всех своих подписок без необходимости создавать их вручную
	Критерий приёмки: Given user has subscriptions connected to other app/service When user imports his subscriptions from other app/service Then all imported subscriptions appear on main page
	- Как пользователь я хочу изменять категории подписок, чтобы подстроить их под себя и группировать подписки так, как мне это нужно
	Критерий приёмки: Given user has other categories of his subscriptions When user changes categories Then categories changed on main page, on subscription create and edit pages, on statistics page

Негативные сценарии:
	- у пользователя нет подписок: отобразить экран с текстом о том, что подписок ещё нет
	- пользователь создаёт подписку без названия: отображается всплывающая подсказка о том, что название сервиса обязательно для создания подписки
	- пользователь ещё не использовал приложение достаточно времени, чтобы отобразить статистику: на экране статистики отображается текст о том, что недостаточно данных для сбора статистики
	- пользователь создаёт подписку со стоимостью 0 рублей: отображается сообщение о том, точно ли пользователь хочет создать подписку со стоимостью 0 рублей
	- ошибка при импорте подписок из стороннего приложения/сервиса: отображается сообщение об ошибке импорта