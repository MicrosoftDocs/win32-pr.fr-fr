---
title: Message MM_JOY1BUTTONUP (mmsystem. h)
description: Le \_ message JOY1BUTTONUP mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été relâché.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- Message MM_JOY1BUTTONUP Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106525"
---
# <a name="mm_joy1buttonup-message"></a><span data-ttu-id="d8cb0-104">MM \_ message JOY1BUTTONUP</span><span class="sxs-lookup"><span data-stu-id="d8cb0-104">MM\_JOY1BUTTONUP message</span></span>

<span data-ttu-id="d8cb0-105">Le **message \_ JOY1BUTTONUP mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 qu’un bouton a été relâché.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-105">The **MM\_JOY1BUTTONUP** message notifies the window that has captured joystick JOYSTICKID1 that a button has been released.</span></span>


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="d8cb0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8cb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8cb0-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="d8cb0-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-108">Identifie le bouton qui a changé d’État et les boutons qui sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="d8cb0-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8cb0-109">It can be one of the following:</span></span>



| <span data-ttu-id="d8cb0-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8cb0-110">Requirement</span></span> | <span data-ttu-id="d8cb0-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8cb0-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="d8cb0-112">JOIE \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="d8cb0-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="d8cb0-113">Le premier bouton de la manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="d8cb0-114">JOIE \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="d8cb0-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="d8cb0-115">Le deuxième bouton de la manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="d8cb0-116">JOIE \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="d8cb0-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="d8cb0-117">Le bouton de la troisième manette de jeu a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="d8cb0-118">JOIE \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="d8cb0-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="d8cb0-119">Le bouton de la quatrième manette de la manette a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="d8cb0-120">et un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8cb0-120">and one or more of the following:</span></span>



| <span data-ttu-id="d8cb0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8cb0-121">Requirement</span></span> | <span data-ttu-id="d8cb0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8cb0-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="d8cb0-123">JOIE, \_ Button1</span><span class="sxs-lookup"><span data-stu-id="d8cb0-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="d8cb0-124">Le premier bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="d8cb0-125">BONHEUR \_ button2</span><span class="sxs-lookup"><span data-stu-id="d8cb0-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="d8cb0-126">Le second bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="d8cb0-127">BONHEUR \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="d8cb0-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="d8cb0-128">Le bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="d8cb0-129">JOIE \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="d8cb0-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="d8cb0-130">Le bouton de la quatrième manette est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d8cb0-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="d8cb0-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-132">Coordonnées x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d8cb0-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*</span><span class="sxs-lookup"><span data-stu-id="d8cb0-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="d8cb0-134">Coordonnée y de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8cb0-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8cb0-135">Requirements</span></span>



| <span data-ttu-id="d8cb0-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8cb0-136">Requirement</span></span> | <span data-ttu-id="d8cb0-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8cb0-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8cb0-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8cb0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d8cb0-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8cb0-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8cb0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d8cb0-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8cb0-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8cb0-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8cb0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8cb0-143"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8cb0-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8cb0-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8cb0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8cb0-145">Manette</span><span class="sxs-lookup"><span data-stu-id="d8cb0-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="d8cb0-146">Messages de manette de jeu multimédia</span><span class="sxs-lookup"><span data-stu-id="d8cb0-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





