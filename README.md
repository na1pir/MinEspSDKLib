# MinEspSDK
Minimalist SDK on ESP8266ex v1.2.0
---

A complete set of Wi-Fi and LwIP functions.<br>
Имеет полный набор функций работы с WiFi и UDP/TCP (LwIP ver1.4.0).<br>
Данная сборка не содержит espconn и SSL.<br>
Проектируется для работы с датчиками и будет содержать расширения для быстрого<br> 
старта после deep-sleep с возможностями управления дальнейшей загрузки SDK или<br> 
опроса датчиков и нового перехода в режим deep-sleep.<br>
В целях экономии питания, время от просыпания после deep-sleep до старта опроса<br> 
датчиков и для принятия решения повторного засыпания или загрузки полного SDK<br>
для коммуникации и передачи накопленных данных будет составлять 30..40 мс.<br>  
В текщей версии, при стандартных настройках по умолчанию, после события подачи<br>
питания, reset или deep-sleep соединение по TCP при фиксированном ip модуля в<br> 
режиме STATION к модулю в режиме SOFTAP устанавливается примерно не более чем<br> 
через 540 мс. Основное время занимает инициализации SDK в части WiFi.<br>
Далее полудуплексный трафик TCP составляет более 1-го Мегабайта в секунду.<br>    

From Espressif SDK ver 1.2.0 used only:<br> 
libpp.a, libwpa.a, libnet80211.a, parts libphy.a, user_interface.o<br>
Из Espressif SDK ver 1.2.0 используются только описанные части.<br>
Остальные части даны с исходными кодами.<br>

Supported options 48 kbytes IRAM.<br>
Supported 'Rapid Loader' and Flash 512 кbytes - 16 Mbytes.<br>
Поддержка расширенной памяти IRAM в 48 килобайт,<br>
Flash от 512 килобайт до 16 Мегабайт и ускоряющего загрузку SDK 'лоадера'.<br>

Free IRAM : 29 kbytes<br>
Free Heap : 51 kbytes<br>
Total Free RAM : 80 kbytes<br>

Options programming Flash:<br> 

SPI_SPEED: 40MHz or 80MHz.<br>
SPI_MODE: QIO only.<br>
FLASH_SIZE: Always set the size to 512 KB flash.<br>
			Automatic determination of the real size of the flash.<br>
При заливке прошивки в модуль всегда устанавливайте размер Flash в 512 килобайт.<br> 
Реальный размер Flash определяется автоматически во время старта SDK.<br> 

Для компиляции SDK используется UDK:   
[Unofficial Developer Kit](http://esp8266.ru/forum/forums/devkit/)<br>

Создать отдельную библиотеку libsdk120.a можно<br> 
с помощью lib/libsdk.bat после компиляции.<br>
Для полного комплекта выйдет: libsdk120.a + libmgcc.a + libmicroc.a и include<br>

libmicroc.a - https://github.com/anakod/esp_microc  
      

