# customer-service
"Cетевой многопоточный сервис для StatusPage".

Сервис собирает, анализирует и представляет данные о работе систем коммуникации: SMS, MMS, VoiceCall, Email, Billing, Support, Incidents.

Для проверки работы используется симулятор исходных данных.

Порядок работы:
1. из каталога "simulator" запустить симулятор  $... \simulator> go run .

или:
$ go run . -mms "http://127.0.0.1:8383/mms" -support "http://127.0.0.1:8383/support" -accendent "http://127.0.0.1:8383/accendent"

По умолчанию исходные данные приходят:
  "MMS" -> http://127.0.0.1:8383/mms
  "Support" -> http://127.0.0.1:8383/support
  "Incidents" -> http://127.0.0.1:8383/accendent
  и частично записываются в файлы этого каталога: billing.data, email.data, sms.data, voice.data

2. запустить сервис $... go run .   или пример с флагом ( $... go run . -addr "http://127.0.0.1:8000")

Результат работы (верифицированные данные) выводятся
  на http://127.0.0.1:8282  или указанный при запуске (http://127.0.0.1:8000)
  
Также можно посмотреть в окне браузера.
   Для этого в проводнике из папки "simulator" запустить файл "status_page.html"

![Результат работы сервиса](https://github.com/CHvvmu/service-cust/assets/96997574/70681c5d-e6bb-4f27-8639-ed114cd92d71)
