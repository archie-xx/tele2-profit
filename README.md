# Tele2 Profit [![Release 1.3.0](https://img.shields.io/github/v/release/raritetmolodoy/tele2-profit?color=black&label=%20)](https://github.com/raritetmolodoy/tele2-profit/releases)

Console application that allows you to quickly sell your Tele2 data on their **Market**



## Disclaimer
**!!!!!!!!!!!!!!!!!!!!ВАЖНАЯ ИНФОРМАЦИЯ!!!!!!!!!!!!!!!!!!!!!!!!!   
Перевыставление лотов больше не работает.  
Выставить лоты теперь можно только один раз.  
Данный скрипт больше не имеет смысла.   
Поддерживать скрипт я больше не буду, пока не вернут перевыставление.  
ВСЕМ СПАСИБО ЗА ИСПОЛЬЗОВАНИЕ И ПОЖЕРТВОВАНИЯ!)**

_От автора:_  
Я не несу ответственности за ваши номера (если они улетят в бан или еще чего по-хуже).  
Скрипт не делает ничего запрещенного, а лишь "нажимает кнопочки, которые вы могли
бы нажать в их приложении, потратив в 10 (да-да) раз больше времени".  

Скрипт не ворует данные и не каким образом не взаимодействует ни с чем-либо кроме
оффициального (но не публичного) API Tele2.
Простое консольное прилоджение сделано лишь для того, чтобы у пользователя не 
возникало сомнений в честности действий, выполняемых скриптом. 
Вы можете посмотреть исходники и подредактировать код, если в том есть неоходимость.
Подобные приложения с веб-интерфейсом и т.п вынуждены хранить ваши авторизационные токены на своих серверах,
что может привести с потере доступа к аккаунту.
Т.к существует возможность бесконечного продления токена без необходимости 
повторного ввода СМС-кода, ввели смс в типичное мошенническое веб-приложение
1 раз и злоумышленник получит доступ к вашему аккаунту НАВСЕГДА (да).
 

Если возникли какие-либо проблемы в работе - откройте обсуждение на вкладке Issues и,
если, нашли решение, приложите свои комментарии. Так как скрипт очень
чувствителен к региону, из которого он запускается, могут возникнуть проблемы в работе, и не факт,
что конкретно ваша проблема решаема (например, старый тариф без поддержки
Маркета и т.п). 

Спасибо за понимание)


## Features
* Quick market listing of your Tele2 data
* Bumping up lots that haven't been sold
* Asynchronous queries to _Tele2 API_ allow to perform multiple actions simultaneously
* Lots auto re-listing after some user-provided interval
* **[v2.0+] Token auto-refreshing without extra SMS inputs**


## Demo (v2.0.0 on Windows 10 Terminal)
![imgur demo gif](https://i.imgur.com/Ciy2tp3.gif)


## Installation (basic - *Windows x64 only*)
#### Steps:
1. Go to [latest release](https://github.com/raritetmolodoy/tele2-profit/releases/latest)
and download **zip**-archive (tele2-profit@\<version\>.zip)
2. Unarchive wherever you want and run **exe**-files.
3. You are good to go!


## Source installation (advanced - _Any OS_)
#### Steps:
1. Clone repository
2. Setup virtual environment (optional)  
    2.1. Create **venv** with `python -m venv venv`  
    2.2. Activate by running this command (just paste it after previous and hit enter) `venv\Scripts\activate`
3. Install dependencies with `pip install -r requirements.txt`
4. You are also good to go!

#### Command list (Windows):
* `git clone https://github.com/raritetmolodoy/tele2-profit.git`
* `cd tele2-profit`
* `python -m venv venv`
* `venv\Scripts\activate`
* `pip install -r requirements.txt`

#### Command list (Unix - bash):
* `git clone https://github.com/raritetmolodoy/tele2-profit.git`
* `cd tele2-profit`
* `python3 -m venv venv`
* `source venv/bin/activate`
* `pip3 install -r requirements.txt`


## Usage
Run `python main.py` (or main.exe if built version), login, and select action.

**note: Access-token saves on your PC _only_, in `./config.json` file** 

### FYI: Current Tele2 market lot requirements

#### Gigabytes
* Minimum GB amount - **1 GB**
* Minimum GB price - **15 rub/GB**, maximum - **50 rub/GB**

#### Minutes
* Minimum minute amount - **50 min**
* Minimum minute price - **0.8 rub/min**, maximum - **2 rub/min**

### Listing lots
**Preparing lots is done with this syntax: `<lot amount> <lot price>`**  
For example: `60 80` - 60 minutes (or gb) will be listed for 80 rub.  

**Standard syntax can be shortened to just `<lot amount>`**   
For example: `68` -  68 minutes (or gb) will be listed with **minimum** possible price *(in this case - 55 rub if minutes, 1020 rub if gb)*.  
When done leave input field empty (just hit enter) and you will jump to the next part.

## Donations
Huge thanks to my donors:
* Кирилл - 100 rub
* Alex - 300 rub
* Никита - 300 rub
* Михаил - 200 rub  

If you want to support my work - *79044979272* (qiwi, sber, tinkoff)
