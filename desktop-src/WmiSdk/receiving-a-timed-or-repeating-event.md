---
description: Un événement chronométré ou répété est un événement qui se produit à une date et une heure spécifiques, ou à intervalles réguliers à intervalles réguliers. Par exemple, un événement peut se produire à minuit le 2 décembre, 2015 ou une fois par semaine, le mardi à 2:31 h 00.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Réception d’un événement chronométré ou répété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202181"
---
# <a name="receiving-a-timed-or-repeating-event"></a>Réception d’un événement chronométré ou répété

Un événement chronométré ou répété est un événement qui se produit à une date et une heure spécifiques, ou à intervalles réguliers à intervalles réguliers. Par exemple, un événement peut se produire à minuit le 2 décembre, 2015 ou une fois par semaine, le mardi à 2:31 h 00.

Le tableau suivant répertorie les différentes classes utilisées pour créer un événement chronométré ou répétitif.



| Classe                                                                                            | Description                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | Modèle d’événement Microsoft standard.<br/> Pour plus d’informations, consultez [création d’un événement de minuterie avec Win32 \_ localtime ou Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).<br/> |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                               | Technique héritée.<br/> Pour plus d’informations, consultez [création d’un événement de minuterie avec \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).<br/>                                             |



 

Si vous souhaitez planifier une tâche ou une tâche pour qu’elle se produise à un moment donné ou à plusieurs reprises, utilisez la classe [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) et ses méthodes. Cette classe représente un travail créé à l’aide de la commande AT dans une fenêtre de commande depuis **Démarrer** , puis **exécuter**, ou à partir des **tâches planifiées** dans le **panneau de configuration**.

 

