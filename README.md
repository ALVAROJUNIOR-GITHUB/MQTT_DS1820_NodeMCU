# MQTT_DS1820_NodeMCU
Projeto testado com as placas NodeMCU modelo AMICA e NodeMCU modelo LOLIN. Todas ESP8266.

Sistema mede a temperatua ambiente/líquidos, por intermédio de um Sensor DS1820, e faz um PUBLISH MQTT nos BROKER's abaixo:

 - test.mosquitto.org
 - iot.eclipse.org


Para testar abra o Terminal LINUX e instale primeiro o BROKER mosquitto. Para isso digite: 

 - sudo apt-get install mosquitto
 - sudo apt-get install mosquitto-clients


Depois da instalação digite o código abaixo e de enter, assim que o NODEMCU começar a publicar, as temperaturas serão mostradas.

NÃO ESQUECER DE MUDAR NO CODIGO DO NODEMCU PARA SUA REDE WIFI(SSID) E PARA SUA SENHA(PASSWORD) !!!

- mosquitto_sub -h iot.eclipse.org -t teste/temp  


Para temperatura Máxima digite:
 - mosquitto_sub -h iot.eclipse.org -t teste/temp_MAX


Para temperatura Mínima digite:
- mosquitto_sub -h iot.eclipse.org -t teste/temp_MIN
