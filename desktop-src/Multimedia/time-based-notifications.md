---
title: Notifications de Time-Based
description: Notifications de Time-Based
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- manettes de jeu, notifications
- manettes, messages
- manettes de jeu, notifications temporelles
- notifications de manette de jeu basées sur le temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229811"
---
# <a name="time-based-notifications"></a>Notifications de Time-Based

Vous pouvez notifier le système d’exploitation d’envoyer des messages de la manette de jeu à une application à intervalles réguliers en définissant le paramètre *fChanged* de [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) sur **false** et en spécifiant la longueur de l’intervalle entre les messages successifs. Pour ce faire, affectez au paramètre *uPeriod* une valeur comprise entre les fréquences d’interrogation minimale et maximale de la manette de jeu. Vous pouvez déterminer cette plage à l’aide de la fonction [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , qui remplit les membres **wPeriodMin** et **wPeriodMax** dans la structure [**JoyCaps**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) . Si la valeur *uPeriod* est en dehors de la plage de fréquences d’interrogation valides pour la manette de jeu, le pilote de manette de jeu utilise la fréquence d’interrogation minimale ou maximale, selon la valeur la plus proche de la valeur de *uPeriod* .

> [!Note]  
> Windows configure un événement de minuterie avec chaque appel à **joySetCapture**.

 

 

 