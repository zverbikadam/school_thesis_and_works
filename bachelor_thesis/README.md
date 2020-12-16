# Názov práce

Klientská aplikácia pre zobrazenie dát ako súčasť senzorického informačného systému

## Thesis

Client application for data visualization as a part of sensory information system

## Abstrakt

Zverbík, Adam: Klientská aplikácia pre zobrazenie dát ako súčasť senzorického infor-mačného systému. [Bakalárska práca]. – Slovenská technická univerzita. Materiálovo-technologická fakulta; Ústav aplikovanej informatiky automatizácie a mechatroniky. –Vedúci práce: Ing. Juraj Ďuďák, PhD. – MTF STU, 2020, 57s.

Cieľom záverečnej práce je vyvinúť a implementovať multiplatformnú desktopovúaplikáciu a web aplikáciu. Výsledkom tejto práce je funkčná klientská aplikácia prezobrazenie dát a spravovanie senzorického informačného systému Sensorical. V prvejkapitole je opísaný systém Sensorical, jeho dátový model a komunikácia so serverom.Druhá kapitola sa venuje analýze požiadaviek a štruktúre aplikácie. V tretej kapitole súpopísané nástroje, ktoré boli použité pri vývoji aplikácie. Štvrtá kapitola pojednáva oimplementácií a piata kapitola je venovaná buildovaniu aplikácie.

## Abstract

Zverbík, Adam: Client application for data visualization as a part of sensory informationsystem. [Bachelor thesis]. – Slovak University of Technology. Faculty of Materials Scienceand Technology; Institute of Applied Informatics, Automation and Mechatronics. –Thesis supervisor: Ing. Juraj Ďuďák, PhD. – MTF STU, 2020, 57p.

The aim of the bachelor thesis is to develop and implement multiplatform desktopapplication and web application. The result of this thesis is functional client application,which shows and manages data of the sensoric information system Sensorical. Datamodel of sensorical system and communication with server is described in the firstchaper. The second chapter is dedicated to analyze requirements and structure of theapplication. The tools used in development process are described in the third chapter.The fourth chapter is about implementation and the fifth chapter describes building ofthe final application.

### kľúčové slová (keywords)

desktopová aplikácia, web aplikácia, React, Electron, senzorický informačný systém 

(desktop application, web application, React, Electron, sensory information system)


# Preview of React application developed within practical part


## Description

This app is developed using combination of 2 JavaScript frameworks, React.js and Electron.js. It is not done yet, there are still functionalities missing at backand side as well as in client side. 

Application communicates with 2 APIs. Models of both APIs are in `API_models` folder. Backend is developed by my supervisor. 

Firstly, app communicates with authorization API to authorize users.

Auth API
- http://login.nsoric.com/nsoric/auth/

After successful authorization users can choose application (information system) to connect to and view data.

Manage API
- http://{app}.nsoric.com/{endpoint}/manage/


Administrators can manage both APIs.

After successful login to information system, users can view measured sensoric data, such as temperature, humidity...

They can view charts from 1 day, 1 week or 1 month. Data are measured and sent to server every 5 minutes (when there is no problem).

## Screenshot with comments

### Login screen

Login screen is the first screen after application launch.

<img src="./obrazky/app_demo/AppDemo/01-HomeUI.png" width=600 alt="Login screen">

Fig.1: Login 

### Applist screen

After successful login, users see companies and company applications. They see only those applications, they have access to.

<img src="./obrazky/app_demo/AppDemo/02-ApplistUI.png" width=600 alt="Applist screen">

Fig. 2: Companies and their applications

### AuthAdmin screen

Auth API administrators can manage this API too.

<img src="./obrazky/app_demo/AppDemo/03-AuthAdminUI.png" width=600 alt="AuthAdmin screen">

Fig. 3: Auth API administration

### Sectors screen - last measured value

When user choose company's application, they see last measured value from sensors in area's sector. They can switch between sectors and areas and view data from sensors in different location.

<img src="./obrazky/app_demo/AppDemo/04-SectorsUI.png" width=600 alt="Sectors screen - last measured value">

Fig. 4: last measured values from sensors

### Sectors screen - values rendered in chart

Users can display line chart, that contains values that were measured during 1 day, 1 week or 1 month. `Recharts` library was used to render charts.

<img src="./obrazky/app_demo/AppDemo/05-SensorGraphs.png" width=600 alt="## Sectors screen - values rendered in chart">

Fig. 5: Data from 1 month displayed in line chart

### ManageAdmin screen

Administrators of current application can manage that database as well.

<img src="./obrazky/app_demo/AppDemo/06-ManageAdminUI.png" width=600 alt="ManageAdmin screen">

Fig. 6: Manage API administration

### Building

To build react side of the application was used reacts
```
$ npm run build
```

<img src="./obrazky/app_demo/Building/reactBuild.png" alt="React build" width=600>

To build electron side of the application was used `electron-packager` library and custom scripts.

<img src="./obrazky/app_demo/Building/electronBuild.png" alt="Electron build" width=600>

