---
title: Sélecteur de date et heure
description: Cette section contient des informations sur les éléments d’API utilisés avec les contrôles de sélecteur de date et d’heure.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4e91b325b798ff465d8048cac2f0a9a72e5774
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842810"
---
# <a name="date-and-time-picker"></a>Sélecteur de date et heure

Cette section contient des informations sur les éléments d’API utilisés avec les contrôles de sélecteur de date et d’heure.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                                    | Contenu                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des contrôles de sélecteur de date et d’heure](date-and-time-picker-controls.md) | Un *contrôle de sélecteur de date et d’heure (PAO)* fournit une interface simple et intuitive par le biais de laquelle échanger des informations de date et d’heure avec un utilisateur.<br/> |
| [Utilisation des contrôles de sélecteur de date et heure](using-date-and-time-picker.md)    | Cette section fournit des informations et des exemples de code pour implémenter les contrôles de sélecteur de date et d’heure. <br/>                                                |



 

### <a name="macros"></a>Macros



| Rubrique                                                                     | Contenu                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Ferme le contrôle de sélecteur de date et d’heure (PAO). Utilisez cette macro ou envoyez le [**message \_ CLOSEMONTHCAL DTM**](dtm-closemonthcal.md) de manière explicite.<br/>                                                                                                                     |
| [**DateTime \_ GetDateTimePickerInfo**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Obtient des informations pour un contrôle de sélecteur de date et d’heure (PAO) spécifié.<br/>                                                                                                                                                                                              |
| [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Obtient la taille nécessaire pour afficher le contrôle sans découpage. Utilisez cette macro ou envoyez le [**message \_ GETIDEALSIZE DTM**](dtm-getidealsize.md) de manière explicite.<br/>                                                                                                        |
| [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Obtient le handle vers le contrôle de calendrier mensuel de l’enfant du sélecteur de dates et d’heures (PAO). Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETMONTHCAL DTM**](dtm-getmonthcal.md) de manière explicite. <br/>                                                                               |
| [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Obtient la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETMCCOLOR DTM**](dtm-getmccolor.md) de manière explicite. <br/>                                                           |
| [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez utiliser cette macro ou envoyer le [**message \_ GETMCFONT DTM**](dtm-getmcfont.md) de manière explicite. <br/>                                                      |
| [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Obtient le style d’un contrôle PAO spécifié. Utilisez cette macro ou envoyez le [**message \_ GETMCSTYLE DTM**](dtm-getmcstyle.md) de manière explicite.<br/>                                                                                                                               |
| [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Obtient l’heure système actuelle minimale et maximale autorisée pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez utiliser cette macro ou envoyer le message [**\_ GETRANGE DTM**](dtm-getrange.md) de manière explicite. <br/>                                                              |
| [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) spécifiée. Vous pouvez utiliser cette macro ou envoyer le message [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md) de manière explicite. <br/> |
| [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Définit l’affichage d’un contrôle de sélecteur de date et heure (PAO) basé sur une chaîne de format donnée. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETFORMAT DTM**](dtm-setformat.md) de manière explicite. <br/>                                                                          |
| [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Définit la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETMCCOLOR DTM**](dtm-setmccolor.md) de manière explicite. <br/>                                                           |
| [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez utiliser cette macro ou envoyer explicitement le message [**DTM \_ SETMCFONT**](dtm-setmcfont.md) . <br/>                                                                |
| [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Définit le style d’un contrôle PAO spécifié. Utilisez cette macro ou envoyez le [**message \_ SETMCSTYLE DTM**](dtm-setmcstyle.md) de manière explicite.<br/>                                                                                                                              |
| [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Définit les heures système minimale et maximale autorisées pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez utiliser cette macro ou envoyer le message [**DTM \_ SetRange**](dtm-setrange.md) explicitement. <br/>                                                                       |
| [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Définit un contrôle de sélecteur de date et heure (PAO) à une date et une heure données. Vous pouvez utiliser cette macro ou envoyer le [**message \_ SETSYSTEMTIME DTM**](dtm-setsystemtime.md) de manière explicite. <br/>                                                                                       |



 

### <a name="messages"></a>Messages



| Rubrique                                                           | Contenu                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md)                 | Ferme un contrôle PAO. Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .<br/>                                                                                                                                        |
| [**DTM \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | Obtient des informations sur un contrôle de sélecteur de dates et d’heures (PAO).<br/>                                                                                                                                                                                                                  |
| [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | Obtient la taille nécessaire pour afficher le contrôle sans découpage. Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .<br/>                                                                                                  |
| [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md)                       | Obtient la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) . <br/>                                              |
| [**DTM \_ GETMCFONT**](dtm-getmcfont.md)                         | Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) . <br/>                                         |
| [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | Obtient le style d’un contrôle PAO. Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .<br/>                                                                                                                       |
| [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | Obtient le handle vers le contrôle de calendrier mensuel de l’enfant du sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) . <br/>                                                                              |
| [**DTM \_ GETRANGE**](dtm-getrange.md)                           | Obtient l’heure système actuelle minimale et maximale autorisée pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) . <br/>                                                              |
| [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md)                 | Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) spécifiée. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) . <br/> |
| [**DTM \_ SETFORMAT**](dtm-setformat.md)                         | Définit l’affichage d’un contrôle de sélecteur de date et heure (PAO) basé sur une chaîne de format donnée. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) . <br/>                                                                         |
| [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md)                       | Définit la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) . <br/>                                              |
| [**DTM \_ SETMCFONT**](dtm-setmcfont.md)                         | Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .<br/>                                                    |
| [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md)                       | Définit le style d’un contrôle PAO. Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .<br/>                                                                                                                       |
| [**DTM \_ SEtrange**](dtm-setrange.md)                           | Définit les heures système minimale et maximale autorisées pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message explicitement ou utiliser la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) . <br/>                                                                      |
| [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | Définit l’heure dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) . <br/>                                                                                                   |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                   | Contenu                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ gros plan](dtn-closeup.md)                         | Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur ferme le calendrier du mois déroulant. Le calendrier du mois est fermé lorsque l’utilisateur choisit une date dans le calendrier du mois ou clique sur la flèche déroulante pendant que le calendrier est ouvert. <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | Envoyé par un contrôle de sélecteur de date et heure (PAO) chaque fois qu’une modification se produit. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                                                                  |
| [\_liste déroulante DTN](dtn-dropdown.md)                       | Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur active le calendrier du mois de la liste déroulante. <br/>                                                                                                                                                                                                                                               |
| [\_format DTN](dtn-format.md)                           | Envoyé par un contrôle de sélecteur de date et heure (PAO) pour demander du texte à afficher dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | Envoyé par un contrôle de sélecteur de date et heure (PAO) pour récupérer la taille maximale autorisée de la chaîne qui s’affichera dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsqu’un utilisateur termine la modification d’une chaîne dans le contrôle. Ce code de notification est uniquement envoyé par les contrôles de PAO définis sur le style [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . Ce message est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)                     | Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur tape dans un champ de rappel. Ce message est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (date/heure)](nm-killfocus-date-time.md) | Avertit une fenêtre parente d’un contrôle de sélecteur de date et d’heure que le contrôle a perdu le focus d’entrée. [**Nm \_ KILLFOCUS (date heure)**](nm-killfocus-date-time.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                 |
| [NM \_ SetFocus (date/heure)](nm-setfocus-date-time-.md)  | Avertit une fenêtre parente d’un contrôle de sélecteur de date et d’heure que le contrôle a reçu le focus d’entrée. [Nm \_ SETFOCUS (date heure)](nm-setfocus-date-time-.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                  |



 

### <a name="structures"></a>Structures



| Rubrique                                                  | Contenu                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Contient des informations sur un contrôle de PAO. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Contient des informations sur une modification qui a été effectuée dans un contrôle de sélecteur de dates et d’heures (PAO). Cette structure est utilisée avec le code de notification [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) . <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Contient des informations sur une partie de la chaîne de format qui définit un champ de rappel dans un contrôle de sélecteur de date et d’heure (PAO). Elle transporte la sous-chaîne qui définit le champ de rappel et contient une mémoire tampon pour recevoir la chaîne qui s’affichera dans le champ de rappel. Cette structure est utilisée avec le code de notification de [ \_ format DTN](dtn-format.md) . <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Contient des informations sur un champ de rappel du contrôle de la date et de l’heure (PAO). Elle contient une sous-chaîne (extraite de la chaîne de format du contrôle) qui définit un champ de rappel. La structure reçoit la taille maximale autorisée du texte qui s’affichera dans le champ de rappel. Cette structure est utilisée avec le code de notification [DTN \_ FORMATQUERY](dtn-formatquery.md) . <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Contient des informations spécifiques à une opération de modification qui a eu lieu dans un contrôle de sélecteur de dates et d’heures (PAO). Ce message est utilisé avec le code de notification [DTN \_ USERSTRING](dtn-userstring.md) . <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Contient les informations utilisées pour décrire et gérer un code de notification [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Constantes



| Rubrique                                                                          | Contenu                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Styles de contrôle de sélecteur de date et d’heure](date-and-time-picker-control-styles.md) | Les styles de fenêtre répertoriés ici sont spécifiques aux contrôles de sélecteur de date et d’heure.<br/> |



 

 

