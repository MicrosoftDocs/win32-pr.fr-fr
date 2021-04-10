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
# <a name="joystick-position"></a><span data-ttu-id="caf9a-105">Position de la manette de jeu</span><span class="sxs-lookup"><span data-stu-id="caf9a-105">Joystick Position</span></span>

<span data-ttu-id="caf9a-106">Vous pouvez interroger une manette de jeu pour obtenir des informations sur la position et le bouton à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="caf9a-106">You can query a joystick for position and button information by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="caf9a-107">Par exemple, une application peut interroger la manette de jeu à la recherche de valeurs de position de ligne de base.</span><span class="sxs-lookup"><span data-stu-id="caf9a-107">For example, an application can query the joystick for baseline position values.</span></span> <span data-ttu-id="caf9a-108">La feuille de propriétés du panneau de configuration de la manette de jeu utilise cette technique lors de l’étalonnage du joystick.</span><span class="sxs-lookup"><span data-stu-id="caf9a-108">The Joystick Control Panel property sheet uses this technique when calibrating the joystick.</span></span>

<span data-ttu-id="caf9a-109">Vous pouvez également interroger une manette de jeu ou un autre appareil disposant de fonctionnalités étendues à l’aide de la fonction [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="caf9a-109">You can also query a joystick or other device that has extended capabilities by using the [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

 

 