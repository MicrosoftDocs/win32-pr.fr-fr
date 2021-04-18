---
title: Message MM_JOY1BUTTONDOWN (mmsystem. h)
description: Le \_ message JOY1BUTTONDOWN mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été enfoncé.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- Message MM_JOY1BUTTONDOWN Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464499"
---
# <a name="mm_joy1buttondown-message"></a><span data-ttu-id="c3123-104">MM \_ message JOY1BUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="c3123-104">MM\_JOY1BUTTONDOWN message</span></span>

<span data-ttu-id="c3123-105">Le **message \_ JOY1BUTTONDOWN mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c3123-105">The **MM\_JOY1BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID1 that a button has been pressed.</span></span>


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="c3123-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3123-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="c3123-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="c3123-108">Identifie le bouton qui a changé d’État et les boutons qui sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="c3123-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="c3123-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3123-109">It can be one of the following:</span></span>



| <span data-ttu-id="c3123-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3123-110">Requirement</span></span> | <span data-ttu-id="c3123-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3123-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="c3123-112">JOIE \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="c3123-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="c3123-113">Le premier bouton de la manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="c3123-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="c3123-114">JOIE \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="c3123-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="c3123-115">Le deuxième bouton de la manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="c3123-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="c3123-116">JOIE \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="c3123-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="c3123-117">Le bouton de la troisième manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="c3123-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="c3123-118">JOIE \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="c3123-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="c3123-119">Le bouton de la quatrième manette de la manette a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="c3123-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="c3123-120">et un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c3123-120">and one or more of the following:</span></span>



| <span data-ttu-id="c3123-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3123-121">Requirement</span></span> | <span data-ttu-id="c3123-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3123-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="c3123-123">JOIE, \_ Button1</span><span class="sxs-lookup"><span data-stu-id="c3123-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="c3123-124">Le premier bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c3123-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="c3123-125">BONHEUR \_ button2</span><span class="sxs-lookup"><span data-stu-id="c3123-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="c3123-126">Le second bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c3123-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="c3123-127">BONHEUR \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="c3123-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="c3123-128">Le bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c3123-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="c3123-129">JOIE \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="c3123-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="c3123-130">Le bouton de la quatrième manette est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c3123-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c3123-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="c3123-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="c3123-132">Coordonnée x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="c3123-132">The x-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="c3123-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*</span><span class="sxs-lookup"><span data-stu-id="c3123-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="c3123-134">Coordonnée y de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="c3123-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3123-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3123-135">Requirements</span></span>



| <span data-ttu-id="c3123-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3123-136">Requirement</span></span> | <span data-ttu-id="c3123-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3123-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3123-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3123-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c3123-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3123-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c3123-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3123-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c3123-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3123-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3123-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3123-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3123-143"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3123-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3123-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3123-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3123-145">Manette</span><span class="sxs-lookup"><span data-stu-id="c3123-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="c3123-146">Messages de manette de jeu multimédia</span><span class="sxs-lookup"><span data-stu-id="c3123-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





