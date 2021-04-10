---
title: Position de la manette de jeu
description: Position de la manette de jeu
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- joysticks, position
- manettes, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104199135"
---
# <a name="joystick-position"></a>Position de la manette de jeu

Vous pouvez interroger une manette de jeu pour obtenir des informations sur la position et le bouton à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Par exemple, une application peut interroger la manette de jeu à la recherche de valeurs de position de ligne de base. La feuille de propriétés du panneau de configuration de la manette de jeu utilise cette technique lors de l’étalonnage du joystick.

Vous pouvez également interroger une manette de jeu ou un autre appareil disposant de fonctionnalités étendues à l’aide de la fonction [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 