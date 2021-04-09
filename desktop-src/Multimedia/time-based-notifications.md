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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940848"
---
# <a name="time-based-notifications"></a><span data-ttu-id="ee11e-107">Notifications de Time-Based</span><span class="sxs-lookup"><span data-stu-id="ee11e-107">Time-Based Notifications</span></span>

<span data-ttu-id="ee11e-108">Vous pouvez notifier le système d’exploitation d’envoyer des messages de la manette de jeu à une application à intervalles réguliers en définissant le paramètre *fChanged* de [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) sur **false** et en spécifiant la longueur de l’intervalle entre les messages successifs.</span><span class="sxs-lookup"><span data-stu-id="ee11e-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="ee11e-109">Pour ce faire, affectez au paramètre *uPeriod* une valeur comprise entre les fréquences d’interrogation minimale et maximale de la manette de jeu.</span><span class="sxs-lookup"><span data-stu-id="ee11e-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="ee11e-110">Vous pouvez déterminer cette plage à l’aide de la fonction [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , qui remplit les membres **wPeriodMin** et **wPeriodMax** dans la structure [**JoyCaps**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) .</span><span class="sxs-lookup"><span data-stu-id="ee11e-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="ee11e-111">Si la valeur *uPeriod* est en dehors de la plage de fréquences d’interrogation valides pour la manette de jeu, le pilote de manette de jeu utilise la fréquence d’interrogation minimale ou maximale, selon la valeur la plus proche de la valeur de *uPeriod* .</span><span class="sxs-lookup"><span data-stu-id="ee11e-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="ee11e-112">Windows configure un événement de minuteur avec chaque appel à **joySetCapture**.</span><span class="sxs-lookup"><span data-stu-id="ee11e-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 