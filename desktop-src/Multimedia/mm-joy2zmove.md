---
title: Message MM_JOY2ZMOVE (mmsystem. h)
description: Le \_ message JOY2ZMOVE mm notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 que la position de la manette de jeu sur l’axe z a changé.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- Message MM_JOY2ZMOVE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517337"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="e8e7f-104">MM \_ message JOY2ZMOVE</span><span class="sxs-lookup"><span data-stu-id="e8e7f-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="e8e7f-105">Le **message \_ JOY2ZMOVE mm** notifie la fenêtre qui a capturé la manette de jeu JOYSTICKID2 que la position de la manette de jeu sur l’axe z a changé.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="e8e7f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8e7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e7f-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="e8e7f-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="e8e7f-108">Identifie les boutons qui sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="e8e7f-109">Il peut s’agir d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="e8e7f-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8e7f-110">Requirement</span></span> | <span data-ttu-id="e8e7f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8e7f-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="e8e7f-112">JOIE, \_ Button1</span><span class="sxs-lookup"><span data-stu-id="e8e7f-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="e8e7f-113">Le premier bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="e8e7f-114">BONHEUR \_ button2</span><span class="sxs-lookup"><span data-stu-id="e8e7f-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="e8e7f-115">Le second bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="e8e7f-116">BONHEUR \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="e8e7f-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="e8e7f-117">Le bouton de la manette de jeu est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="e8e7f-118">JOIE \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="e8e7f-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="e8e7f-119">Le bouton de la quatrième manette est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e8e7f-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="e8e7f-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="e8e7f-121">Coordonnée z de la manette de jeu.</span><span class="sxs-lookup"><span data-stu-id="e8e7f-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8e7f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8e7f-122">Requirements</span></span>



| <span data-ttu-id="e8e7f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8e7f-123">Requirement</span></span> | <span data-ttu-id="e8e7f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8e7f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e7f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8e7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e7f-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8e7f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e8e7f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8e7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e7f-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8e7f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8e7f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8e7f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e7f-130"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e7f-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e7f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8e7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e7f-132">Manette</span><span class="sxs-lookup"><span data-stu-id="e8e7f-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="e8e7f-133">Messages de manette de jeu multimédia</span><span class="sxs-lookup"><span data-stu-id="e8e7f-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





