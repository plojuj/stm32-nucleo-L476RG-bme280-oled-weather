# STM32 Weather Station (BME280 + OLED)

Kompaktowa stacja pogodowa oparta na mikrokontrolerze **STM32L476RG**. Urządzenie odczytuje temperaturę, wilgotność oraz ciśnienie z czujnika środowiskowego BME280 i na bieżąco wyświetla sformatowane dane na ekranie OLED.

## Funkcjonalność
* Odczyt danych środowiskowych z czujnika Bosch BME280.
* Wyświetlanie wyników na wyświetlaczu OLED (sterownik SSD1306/SH1106).
* Komunikacja z obydwoma modułami po magistrali I2C.
* **Współdzielona linia I2C:** Zarówno ekran, jak i czujnik są podłączone do tych samych pinów mikrokontrolera (I2C1), wykorzystując różne adresy sprzętowe.

## Podłączenie sprzętu (Hardware)

| Moduł | Pin STM32 | Funkcja | Uwagi |
| :--- | :--- | :--- | :--- |
| **I2C (Wspólne)** | **PB8** | SCL | Sygnał zegarowy (podłączone do BME280 i OLED) |
| | **PB9** | SDA | Linia danych (podłączone do BME280 i OLED) |
| **Zasilanie** | 3.3V | VCC / VIN | Zasilanie obu modułów |
| | GND | GND | Wspólna masa |

## Wykorzystane biblioteki (Credits)
W projekcie wykorzystano świetne biblioteki open-source. Pełne prawa autorskie należą do ich twórców:
* **Biblioteka BME280 dla STM32:** [https://github.com/controllerstech/STM32-HAL/tree/master/BME280/I2C]
* **Biblioteka OLED SSD1306 dla STM32:**[https://github.com/afiskon/stm32-ssd1306]

*Wielkie podziękowania dla autorów za udostępnienie kodu!*