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
# <a name="event-based-notifications"></a><span data-ttu-id="99c97-108">Notifications de Event-Based</span><span class="sxs-lookup"><span data-stu-id="99c97-108">Event-Based Notifications</span></span>

<span data-ttu-id="99c97-109">Vous pouvez demander au système d’envoyer des messages de manette de jeu à une application chaque fois que la position d’un axe de manette de jeu change d’une valeur supérieure au *seuil de déplacement* de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="99c97-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="99c97-110">Le seuil de déplacement est la distance à laquelle la manette de jeu doit être déplacée avant qu’un message de modification de position de la manette de jeu ne soit envoyé à une fenêtre qui a capturé l’appareil.</span><span class="sxs-lookup"><span data-stu-id="99c97-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="99c97-111">Pour plus d’informations, [**consultez \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)ou [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).</span><span class="sxs-lookup"><span data-stu-id="99c97-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="99c97-112">Le seuil est initialement égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="99c97-112">The threshold is initially zero.</span></span> <span data-ttu-id="99c97-113">Vous pouvez définir le seuil de déplacement à l’aide de la fonction [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) .</span><span class="sxs-lookup"><span data-stu-id="99c97-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="99c97-114">Vous pouvez récupérer la fréquence d’interrogation minimale de la manette de jeu à l’aide de la fonction [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="99c97-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 