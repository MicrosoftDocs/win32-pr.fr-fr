---
title: Notifications de Event-Based
description: Notifications de Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- manettes de jeu, notifications
- manettes, messages
- manettes de jeu, notifications basées sur les événements
- joysticks, seuil de déplacement
- notifications de manette de jeu basées sur les événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725132"
---
# <a name="event-based-notifications"></a>Notifications de Event-Based

Vous pouvez demander au système d’envoyer des messages de manette de jeu à une application chaque fois que la position d’un axe de manette de jeu change d’une valeur supérieure au *seuil de déplacement* de l’appareil. Le seuil de déplacement est la distance à laquelle la manette de jeu doit être déplacée avant qu’un message de modification de position de la manette de jeu ne soit envoyé à une fenêtre qui a capturé l’appareil. Pour plus d’informations, [**consultez \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)ou [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).

Le seuil est initialement égal à zéro. Vous pouvez définir le seuil de déplacement à l’aide de la fonction [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) . Vous pouvez récupérer la fréquence d’interrogation minimale de la manette de jeu à l’aide de la fonction [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .

 

 