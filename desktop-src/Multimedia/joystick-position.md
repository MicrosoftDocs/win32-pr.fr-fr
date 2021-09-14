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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195228"
---
# <a name="joystick-position"></a>Position de la manette de jeu

Vous pouvez interroger une manette de jeu pour obtenir des informations sur la position et le bouton à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Par exemple, une application peut interroger la manette de jeu à la recherche de valeurs de position de ligne de base. La feuille de propriétés du panneau de configuration de la manette de jeu utilise cette technique lors de l’étalonnage du joystick.

Vous pouvez également interroger une manette de jeu ou un autre appareil disposant de fonctionnalités étendues à l’aide de la fonction [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 