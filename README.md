# customer-service
"Cетевой многопоточный сервис для StatusPage".

Сервис собирает, анализирует и представляет данные о работе систем коммуникации: SMS, MMS, VoiceCall, Email, Billing, Support, Incidents.

Для проверки работы используется симулятор исходных данных.

Порядок работы:
1. из каталога "simulator" запустить симулятор  $... \simulator> go run .
2. запустить сервис $... go run .   или пример с флагом ( $... go run . -addr "http://127.0.0.1:8000")
3. результат работы (верифицированные данные) выводятся на http://127.0.0.1:8282/test  (http://127.0.0.1:8000)

Для пулучения из других источников выполнить запуск с флагом:

пример:

$ go run . -mms "http://127.0.0.1:8383/mms" -support "http://127.0.0.1:8383/support" -accendent "http://127.0.0.1:8383/accendent"
