---
title: Messages de notification de la manette de jeu
description: Messages de notification de la manette de jeu
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- manettes de jeu, notifications
- manettes, messages
- joysticks, position
- manettes, boutons
- Messages MM_JOY1
- Messages MM_JOY2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195231"
---
# <a name="joystick-notification-messages"></a>Messages de notification de la manette de jeu

Les messages de la manette de jeu informent votre application qu’une manette de jeu a changé de position ou que l’un de ses boutons a changé d’État. Les messages commençant par MM \_ JOY1 sont envoyés à la fonction si votre application demande une entrée à partir de la manette de jeu à l’aide de l’identificateur JOYSTICKID1, et que des \_ messages JOY2 mm sont envoyés si votre application demande une entrée de la manette de jeu à l’aide de l’identificateur JOYSTICKID2.

Les messages figurant dans le tableau suivant identifient l’état des boutons de la manette de jeu :



| Message                                         | Description                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**\_JOY1BUTTONDOWN mm**](mm-joy1buttondown.md) | Un bouton sur la manette de jeu JOYSTICKID1 a été enfoncé.              |
| [**\_JOY1BUTTONUP mm**](mm-joy1buttonup.md)     | Un bouton sur la manette de jeu JOYSTICKID1 a été relâché.             |
| [**\_JOY1MOVE mm**](mm-joy1move.md)             | La manette de jeu JOYSTICKID1 a changé de position dans l’axe x ou y. |
| [**\_JOY1ZMOVE mm**](mm-joy1zmove.md)           | La manette de jeu JOYSTICKID1 a changé de position dans l’axe z.       |
| [**\_JOY2BUTTONDOWN mm**](mm-joy2buttondown.md) | Un bouton sur la manette de jeu JOYSTICKID2 a été enfoncé.              |
| [**\_JOY2BUTTONUP mm**](mm-joy2buttonup.md)     | Un bouton sur la manette de jeu JOYSTICKID2 a été relâché.             |
| [**\_JOY2MOVE mm**](mm-joy2move.md)             | La manette JOYSTICKID2 a changé de position dans l’axe x ou y  |
| [**\_JOY2ZMOVE mm**](mm-joy2zmove.md)           | La manette de jeu JOYSTICKID2 a changé de position dans l’axe z.       |



 

Tous les messages signalent des boutons inexistants comme étant libérés.

 

 




