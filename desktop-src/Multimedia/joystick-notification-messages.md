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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509187"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="3e7b7-109">Messages de notification de la manette de jeu</span><span class="sxs-lookup"><span data-stu-id="3e7b7-109">Joystick Notification Messages</span></span>

<span data-ttu-id="3e7b7-110">Les messages de la manette de jeu informent votre application qu’une manette de jeu a changé de position ou que l’un de ses boutons a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="3e7b7-111">Les messages commençant par MM \_ JOY1 sont envoyés à la fonction si votre application demande une entrée à partir de la manette de jeu à l’aide de l’identificateur JOYSTICKID1, et que des \_ messages JOY2 mm sont envoyés si votre application demande une entrée de la manette de jeu à l’aide de l’identificateur JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="3e7b7-112">Les messages figurant dans le tableau suivant identifient l’état des boutons de la manette de jeu :</span><span class="sxs-lookup"><span data-stu-id="3e7b7-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="3e7b7-113">Message</span><span class="sxs-lookup"><span data-stu-id="3e7b7-113">Message</span></span>                                         | <span data-ttu-id="3e7b7-114">Description</span><span class="sxs-lookup"><span data-stu-id="3e7b7-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="3e7b7-115">**\_JOY1BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="3e7b7-116">Un bouton sur la manette de jeu JOYSTICKID1 a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="3e7b7-117">**\_JOY1BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="3e7b7-118">Un bouton sur la manette de jeu JOYSTICKID1 a été relâché.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="3e7b7-119">**\_JOY1MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="3e7b7-120">La manette de jeu JOYSTICKID1 a changé de position dans l’axe x ou y.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="3e7b7-121">**\_JOY1ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="3e7b7-122">La manette de jeu JOYSTICKID1 a changé de position dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="3e7b7-123">**\_JOY2BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="3e7b7-124">Un bouton sur la manette de jeu JOYSTICKID2 a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="3e7b7-125">**\_JOY2BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="3e7b7-126">Un bouton sur la manette de jeu JOYSTICKID2 a été relâché.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="3e7b7-127">**\_JOY2MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="3e7b7-128">La manette JOYSTICKID2 a changé de position dans l’axe x ou y</span><span class="sxs-lookup"><span data-stu-id="3e7b7-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="3e7b7-129">**\_JOY2ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="3e7b7-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="3e7b7-130">La manette de jeu JOYSTICKID2 a changé de position dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="3e7b7-131">Tous les messages signalent des boutons inexistants comme étant libérés.</span><span class="sxs-lookup"><span data-stu-id="3e7b7-131">All messages report nonexistent buttons as released.</span></span>

 

 




