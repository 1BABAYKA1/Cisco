Чтобы включить функцию DHCP Snooping нужно для начала задать доверенные и не доверенные порты. 
Все порты, к которому подключены конечные пользователи считаются не доверенными.

### AccSwitch(config)#int ra ***
### AccSwitch(config-if-range)#ip dhcp snooping limit rate ***
### AccSwitch(config-if-range)#ip arp inspection limit rate ***

Тут мы задаем количество пакетов, которые должны проходить через не доверенный интерфейс. 
Обычно такого числа пакетов хватает для получения и обновления IP адреса. Далее настраиваем доверенные интерфейсы:

### AccSwitch(config)#int ra ***
### AccSwitch(config-if-range)#ip dhcp snooping trust
### AccSwitch(config-if-range)#ip arp inspection trust

После этого глобально включаем DHCP Snooping, но НЕ ARP Inspection:

### AccSwitch(config)#ip dhcp snooping
### AccSwitch(config)#ip dhcp snooping vlan ***
### AccSwitch(config)#no ip dhcp snooping information option
