---
description: Cette rubrique traite des minuteries. Un minuteur est une routine interne qui mesure à plusieurs reprises un intervalle spécifié, en millisecondes.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Minuteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364455"
---
# <a name="timers"></a>Minuteurs

Un minuteur est une routine interne qui mesure à plusieurs reprises un intervalle spécifié, en millisecondes.

### <a name="in-this-section"></a>Dans cette section



| Nom                                   | Description                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [À propos des minuteries](about-timers.md)       | Décrit comment créer, identifier, définir et supprimer des minuteries.<br/>                                                     |
| [Utilisation de minuteurs](using-timers.md)       | Explique comment créer et détruire des minuteries, et comment utiliser un minuteur pour intercepter l’entrée de la souris à des intervalles spécifiés.<br/> |
| [Référence du minuteur](timer-reference.md) | Contient la référence de l’API.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Fonctions de minuterie



| Nom                           | Description                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Détruit la minuterie spécifiée. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Crée un minuteur avec la valeur de délai d’attente spécifiée.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Fonction de rappel définie par l’application qui traite les messages [**\_ du minuteur WM**](wm-timer.md) . Le type **TIMERPROC** définit un pointeur vers cette fonction de rappel. [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) est un espace réservé pour le nom de la fonction définie par l’application. <br/> |



 

### <a name="timer-notifications"></a>Notifications du minuteur



| Nom                          | Description                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_minuteur WM**](wm-timer.md) | Publié dans la file d’attente de messages du thread d’installation lors de l’expiration d’un minuteur. Le message est publié par la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . <br/> |



 

 

 
