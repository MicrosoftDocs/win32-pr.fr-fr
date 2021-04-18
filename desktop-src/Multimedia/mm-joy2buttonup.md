---
title: Message MM_JOY2BUTTONUP (mmsystem. h)
description: Le \_ message JOY2BUTTONUP mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 qu’un bouton a été relâché.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- Message MM_JOY2BUTTONUP Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509137"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="98b35-104">MM \_ message JOY2BUTTONUP</span><span class="sxs-lookup"><span data-stu-id="98b35-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="98b35-105">Le **message \_ JOY2BUTTONUP mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 qu’un bouton a été relâché.</span><span class="sxs-lookup"><span data-stu-id="98b35-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="98b35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98b35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98b35-107">**fwButtons**</span><span class="sxs-lookup"><span data-stu-id="98b35-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="98b35-108">Identifie le bouton qui a changé d’État et les boutons qui sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="98b35-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="98b35-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98b35-109">It can be one of the following:</span></span>



| <span data-ttu-id="98b35-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="98b35-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="98b35-111">Signification</span><span class="sxs-lookup"><span data-stu-id="98b35-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="98b35-112"><dt>**JOIE \_ BUTTON1CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="98b35-113">Le premier bouton de la manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="98b35-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="98b35-114"><dt>**JOIE \_ BUTTON2CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="98b35-115">Le deuxième bouton de la manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="98b35-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="98b35-116"><dt>**JOIE \_ BUTTON3CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="98b35-117">Le bouton de la troisième manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="98b35-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="98b35-118"><dt>**JOIE \_ BUTTON4CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="98b35-119">Le bouton de la quatrième manette de la manette a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="98b35-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="98b35-120">et un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="98b35-120">and one or more of the following:</span></span>



| <span data-ttu-id="98b35-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="98b35-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="98b35-122">Signification</span><span class="sxs-lookup"><span data-stu-id="98b35-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="98b35-123"><dt>**JOIE, \_ Button1**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="98b35-124">Le premier bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="98b35-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="98b35-125"><dt>**BONHEUR \_ button2**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="98b35-126">Le second bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="98b35-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="98b35-127"><dt>**BONHEUR \_ BUTTON3**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="98b35-128">Le bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="98b35-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="98b35-129"><dt>**JOIE \_ BUTTON4**</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="98b35-130">Le bouton de la quatrième manette est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="98b35-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b35-131">**xPos**</span><span class="sxs-lookup"><span data-stu-id="98b35-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="98b35-132">Coordonnées x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="98b35-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="98b35-133">**PosY**</span><span class="sxs-lookup"><span data-stu-id="98b35-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="98b35-134">Coordonnée y de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="98b35-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98b35-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98b35-135">Requirements</span></span>



| <span data-ttu-id="98b35-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98b35-136">Requirement</span></span> | <span data-ttu-id="98b35-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="98b35-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b35-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98b35-138">Minimum supported client</span></span><br/> | <span data-ttu-id="98b35-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98b35-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98b35-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98b35-140">Minimum supported server</span></span><br/> | <span data-ttu-id="98b35-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98b35-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98b35-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="98b35-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="98b35-143"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98b35-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b35-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b35-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b35-145">Manette</span><span class="sxs-lookup"><span data-stu-id="98b35-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="98b35-146">Messages de manette de jeu multimédia</span><span class="sxs-lookup"><span data-stu-id="98b35-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





