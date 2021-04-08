---
description: Envoyé à une fenêtre que l’utilisateur redimensionne. En traitant ce message, une application peut surveiller la taille et la position du rectangle de glissement et, si nécessaire, modifier sa taille ou sa position.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Message WM_SIZING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756633"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="7697b-104">\_Message de dimensionnement WM</span><span class="sxs-lookup"><span data-stu-id="7697b-104">WM\_SIZING message</span></span>

<span data-ttu-id="7697b-105">Envoyé à une fenêtre que l’utilisateur redimensionne.</span><span class="sxs-lookup"><span data-stu-id="7697b-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="7697b-106">En traitant ce message, une application peut surveiller la taille et la position du rectangle de glissement et, si nécessaire, modifier sa taille ou sa position.</span><span class="sxs-lookup"><span data-stu-id="7697b-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="7697b-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7697b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="7697b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7697b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7697b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7697b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7697b-110">Bord de la fenêtre en cours de dimensionnement.</span><span class="sxs-lookup"><span data-stu-id="7697b-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="7697b-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7697b-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7697b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7697b-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="7697b-113">Signification</span><span class="sxs-lookup"><span data-stu-id="7697b-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="7697b-114"><dt>**WMSZ \_**</dt> <dt>6</dt> derniers</span><span class="sxs-lookup"><span data-stu-id="7697b-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="7697b-115">Bord inférieur</span><span class="sxs-lookup"><span data-stu-id="7697b-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="7697b-116"><dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="7697b-117">Angle inférieur gauche</span><span class="sxs-lookup"><span data-stu-id="7697b-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="7697b-118"><dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="7697b-119">Coin inférieur droit</span><span class="sxs-lookup"><span data-stu-id="7697b-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="7697b-120"><dt>**WMSZ \_ GAUCHE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="7697b-121">Bord gauche</span><span class="sxs-lookup"><span data-stu-id="7697b-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="7697b-122"><dt>**WMSZ \_ DROIT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="7697b-123">Bord droit</span><span class="sxs-lookup"><span data-stu-id="7697b-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="7697b-124"><dt>**WMSZ \_**</dt> <dt>3</dt> premiers</span><span class="sxs-lookup"><span data-stu-id="7697b-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="7697b-125">Bord supérieur</span><span class="sxs-lookup"><span data-stu-id="7697b-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="7697b-126"><dt>**WMSZ \_ GAUCHE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="7697b-127">Coin supérieur gauche</span><span class="sxs-lookup"><span data-stu-id="7697b-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="7697b-128"><dt>**WMSZ \_ À droite**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="7697b-129">Coin supérieur droit</span><span class="sxs-lookup"><span data-stu-id="7697b-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="7697b-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7697b-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7697b-131">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec les coordonnées d’écran du rectangle de glissement.</span><span class="sxs-lookup"><span data-stu-id="7697b-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="7697b-132">Pour modifier la taille ou la position du rectangle de glissement, une application doit modifier les membres de cette structure.</span><span class="sxs-lookup"><span data-stu-id="7697b-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7697b-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7697b-133">Return value</span></span>

<span data-ttu-id="7697b-134">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7697b-134">Type: **LRESULT**</span></span>

<span data-ttu-id="7697b-135">Une application doit retourner la **valeur true** si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="7697b-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7697b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7697b-136">Requirements</span></span>



| <span data-ttu-id="7697b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7697b-137">Requirement</span></span> | <span data-ttu-id="7697b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="7697b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7697b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7697b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7697b-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7697b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7697b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7697b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7697b-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7697b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7697b-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="7697b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7697b-144"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7697b-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7697b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7697b-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="7697b-146">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7697b-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7697b-147">**dédéplacement de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7697b-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="7697b-148">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="7697b-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="7697b-149">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7697b-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7697b-150">Windows</span><span class="sxs-lookup"><span data-stu-id="7697b-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="7697b-151">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="7697b-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7697b-152">[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7697b-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
