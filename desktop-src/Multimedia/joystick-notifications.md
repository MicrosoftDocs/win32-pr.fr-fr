---
title: Notifications de manette de jeu
description: Notifications de manette de jeu
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- manettes de jeu, notifications
- manettes, messages
- joysticks capturés
- joysticks débranchés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031200"
---
# <a name="joystick-notifications"></a><span data-ttu-id="9271a-107">Notifications de manette de jeu</span><span class="sxs-lookup"><span data-stu-id="9271a-107">Joystick Notifications</span></span>

<span data-ttu-id="9271a-108">Vous pouvez capturer des messages de manette de jeu directs à envoyer à une fonction à l’aide de la fonction [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) .</span><span class="sxs-lookup"><span data-stu-id="9271a-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="9271a-109">Une seule application à la fois peut capturer des messages à partir d’une manette de jeu, mais vous pouvez interroger la manette de jeu à partir d’une autre application à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) ou [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="9271a-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="9271a-110">Un message de manette de jeu peut ne pas parvenir à atteindre l’application qui a capturé la manette de jeu si une deuxième application utilise **joyGetPos** ou **joyGetPosEx** pour interroger la manette à peu près au même moment que le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="9271a-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="9271a-111">Dans ce cas, la deuxième application peut intercepter le message.</span><span class="sxs-lookup"><span data-stu-id="9271a-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="9271a-112">Si vous souhaitez capturer des messages à partir de deux manettes associées au système, utilisez [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) à deux reprises, une fois pour chaque manette de jeu.</span><span class="sxs-lookup"><span data-stu-id="9271a-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="9271a-113">Votre fenêtre reçoit des messages distincts et distincts pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="9271a-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="9271a-114">Vous pouvez libérer une manette capturée à l’aide de la fonction [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) .</span><span class="sxs-lookup"><span data-stu-id="9271a-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="9271a-115">Si une application ne libère pas la manette de jeu avant de se terminer, la manette de jeu est automatiquement libérée peu après la destruction de la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="9271a-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="9271a-116">Vous ne pouvez pas capturer une manette débranchée.</span><span class="sxs-lookup"><span data-stu-id="9271a-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="9271a-117">La fonction **joySetCapture** retourne JOYERR \_ débranché si l’appareil spécifié est débranché.</span><span class="sxs-lookup"><span data-stu-id="9271a-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 