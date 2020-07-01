# Configuration
LED_GREEN, PA_5

GPIO_InitTypeDef gpio;  // obiekt gpio będący konfiguracją portów GPIO
 
GPIO_StructInit(&gpio);  // domyślna konfiguracja
gpio.GPIO_Pin = GPIO_Pin_5;  // konfigurujemy pin 5
gpio.GPIO_Mode = GPIO_Mode_Out_PP;  // jako wyjście
GPIO_Init(GPIOA, &gpio);  // inicjalizacja modułu GPIOA


USER_BUTTON, PC_13

gpio.GPIO_Pin = GPIO_Pin_13; // konfigurujemy pin 13
gpio.GPIO_Mode = GPIO_Mode_IPU; // jako wejście z rezystorem pull-up
GPIO_Init(GPIOC, &gpio); 


Prriperials:
RCC (Reset and Clock Control)
    High Speed Clock (HSE) : Cristal/Ceramic Resonator

SYS (System):
    Debug: Serial Wire

USB:  Enable Device FS

MiddleWares:
USB_DEVICE: Communication Device Class (Virtual Port Com)


USBSerialTest.cfg
 #Use hardware reset
reset+config srat+only

Application:
CDC_Transmit_FS()

CDC_Receive_FS()

# To push an existing repository from the command line

git remote add origin git@github.com:TechNotes-pl/HelloSTM32F103.git
git push -u origin master