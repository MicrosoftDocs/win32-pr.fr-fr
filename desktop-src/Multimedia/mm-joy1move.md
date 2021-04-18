---
title: Message MM_JOY1MOVE (mmsystem. h)
description: Le \_ message JOY1MOVE mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 que la position de la manette de jeu a changé.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- Message MM_JOY1MOVE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78753bd55f6682b3ac3f1514356d93cb455d162
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512781"
---
# <a name="mm_joy1move-message"></a><span data-ttu-id="66a19-104">MM \_ message JOY1MOVE</span><span class="sxs-lookup"><span data-stu-id="66a19-104">MM\_JOY1MOVE message</span></span>

<span data-ttu-id="66a19-105">Le **message \_ JOY1MOVE mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID1 que la position de la manette de jeu a changé.</span><span class="sxs-lookup"><span data-stu-id="66a19-105">The **MM\_JOY1MOVE** message notifies the window that has captured joystick JOYSTICKID1 that the joystick position has changed.</span></span>


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="66a19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a19-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="66a19-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="66a19-108">Identifie les boutons qui sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="66a19-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="66a19-109">Il peut s’agir d’une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="66a19-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="66a19-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66a19-110">Requirement</span></span> | <span data-ttu-id="66a19-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="66a19-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="66a19-112">JOIE, \_ Button1</span><span class="sxs-lookup"><span data-stu-id="66a19-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="66a19-113">Le premier bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="66a19-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="66a19-114">BONHEUR \_ button2</span><span class="sxs-lookup"><span data-stu-id="66a19-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="66a19-115">Le second bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="66a19-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="66a19-116">BONHEUR \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="66a19-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="66a19-117">Le bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="66a19-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="66a19-118">JOIE \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="66a19-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="66a19-119">Le bouton de la quatrième manette est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="66a19-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="66a19-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="66a19-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="66a19-121">Coordonnées x de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="66a19-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="66a19-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*</span><span class="sxs-lookup"><span data-stu-id="66a19-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="66a19-123">Coordonnée y de la manette de jeu par rapport au coin supérieur gauche de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="66a19-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66a19-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66a19-124">Requirements</span></span>



| <span data-ttu-id="66a19-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66a19-125">Requirement</span></span> | <span data-ttu-id="66a19-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="66a19-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a19-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66a19-127">Minimum supported client</span></span><br/> | <span data-ttu-id="66a19-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66a19-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66a19-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66a19-129">Minimum supported server</span></span><br/> | <span data-ttu-id="66a19-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66a19-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="66a19-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="66a19-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a19-132"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66a19-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a19-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66a19-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a19-134">Manette</span><span class="sxs-lookup"><span data-stu-id="66a19-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="66a19-135">Messages de manette de jeu multimédia</span><span class="sxs-lookup"><span data-stu-id="66a19-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





