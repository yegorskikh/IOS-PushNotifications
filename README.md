# IOS-PushNotifications

## Chapter 1: Introduction
### Key points
- Push-уведомления позволяют вам взаимодействовать с вашими пользователями вне обычного потока вашего приложения.
- Уведомление может быть запланировано локально в зависимости от условий или из удаленной службы и отправлено на ваше устройство.
- Удаленные уведомления являются наиболее распространенным типом, и они используют облачный сервис, чтобы определить, что уведомление должно быть создано и отправлено на устройство.
- Уведомляющие сообщения остаются безопасными, поскольку APN использует криптографическую проверку и аутентификацию.
- Локальное уведомление создается и планируется на устройстве, а не отправляется на устройство удаленным провайдером.

## Chapter 3: Remote Notification Payload
### Key points
- Предпочитайте использовать словарь вместо строки для ключа предупреждения.
Подумайте, как вы собираетесь решать проблемы локализации: на стороне сервера или на стороне клиента.
- Используйте поле HTTP-заголовка apns-collapse-id, когда «переопределение» или «обновление» вашего уведомления более уместно, чем отправка дополнительного уведомления.
- Поместите все свои пользовательские данные за пределы ключа APS, чтобы ваши пользовательские ключи были надежными в будущем.
- Подумайте, имеет ли смысл группировать и / или сворачивать ваши уведомления.
- Убедитесь, что вы указываете значение для нового HTTP-заголовка apns-push-type.

## Chapter 4: Xcode Project Setup
### Key points
- Вы должны сообщить Xcode, что push-уведомления будут частью вашего проекта; выполните действия, описанные в этой главе, чтобы Xcode мог выполнить регистрацию за вас.
- Вы должны добавить требуемый код, чтобы подготовить приложение к получению push-уведомлений.
- Push-уведомления являются дополнительной функцией, поэтому вы должны запросить разрешения у пользователя, чтобы включить их.
- Чтобы избежать резких уведомлений при первом открытии приложения пользователем, используйте временную авторизацию, чтобы уведомления доставлялись в Центр уведомлений пользователя в автоматическом режиме без запроса разрешения.
- Для критических предупреждений, которые отменяют отклонение предупреждений пользователя, вы должны подать заявку на получение специального разрешения от Apple, чтобы включить их из-за их разрушительного характера.
- После того, как вы успешно зарегистрируете свое приложение для получения уведомлений, iOS вызовет метод делегата, предоставив вашему приложению токен устройства.
- Никогда не делайте предположений о длине вашего токена и не пытайтесь связать токен с конкретным пользователем.
- Укажите в своей реализации структуры приложения, что вы используете делегата приложения.
- [example](https://github.com/egorskikh/IOS-PushNotifications/tree/main/Chapter%204/PushNotifications)

## Chapter 5: Sending Your First Push Notification
### Key points
- Чтобы ваше приложение получало push-уведомления, у вас должен быть токен аутентификации, используемый серверами Apple, чтобы доверять вашему приложению.
- Токен аутентификации проверяет ваш сервер и гарантирует, что между вашим сервером и APN всегда есть безопасное соединение.
- Создание токена аутентификации - это простой процесс, который вам нужно сделать только один раз; следуйте инструкциям в главе, чтобы создать свой.
- Чтобы настроить push и отправить его вручную, на GitHub есть много бесплатных проектов с открытым исходным кодом, которые предоставляют эту функцию - просто убедитесь, что все, что вы используете, поддерживает ключи аутентификации.
- Если вы отправляете push-уведомление в симулятор, убедитесь, что файл имеет расширение apns и включает идентификатор вашего пакета.
- [example](https://github.com/egorskikh/IOS-PushNotifications/tree/main/Chapter%205/PushNotifications)

## Chapter 6: Server-Side Pushes
### Key points
- Вам понадобится SQL-сервер для хранения токенов устройств.
- Для хранения и удаления токенов вам понадобится API, доступный для вашего приложения iOS.
- Не используйте собственные сетевые команды Foundation для отправки push-уведомлений. Apple будет рассматривать это как атаку отказа в обслуживании из-за повторяющегося открытия и закрытия соединений.
- Есть много вариантов построения вашего push-сервера. Выберите те, которые лучше всего подходят для вашего набора навыков.
- [example](https://github.com/egorskikh/IOS-PushNotifications/tree/main/Chapter%206)

## Chapter 7: 
### Key points

## Chapter 8: 
### Key points

## Chapter 9: 
### Key points

## Chapter 10: 
### Key points

## Chapter 11: 
### Key points

## Chapter 12: 
### Key points

## Chapter 13: Local Notifications
### Key points
- Хотя большинство push-уведомлений, отображаемых на вашем устройстве, являются удаленными уведомлениями, также можно отображать уведомления, исходящие с устройства пользователя, локально.
- Локальные уведомления используются реже, но они все же заслуживают вашего понимания. Могут быть случаи, когда пользователю требуется уведомление (например, напоминание) без каких-либо предпринятых действий.
- Уведомления календаря происходят в определенную дату или время.
- Уведомления об интервале появляются через определенное время.
- Уведомления о местоположении появляются при входе в определенную область.
- Несмотря на то, что уведомление создается и доставляется локально на устройство пользователя, вы все равно должны получить разрешение на отображение уведомлений.
- [example]( - )
