---
description: Se produit lorsque l’utilisateur appuie sur le bouton de la souris pendant que la souris se trouve sur le contrôle InkEdit.
ms.assetid: 8985fee5-7b63-46ab-b229-046e2f0ee004
title: InkEdit. MouseDown, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78e684fe2d75e5eaaf2b0064e8c7c78cbfe281a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868297"
---
# <a name="inkeditmousedown-event"></a><span data-ttu-id="39306-103">InkEdit. MouseDown, événement</span><span class="sxs-lookup"><span data-stu-id="39306-103">InkEdit.MouseDown event</span></span>

<span data-ttu-id="39306-104">Se produit lorsque l’utilisateur appuie sur le bouton de la souris pendant que la souris se trouve sur le contrôle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="39306-104">Occurs when the user presses a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="39306-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39306-105">Syntax</span></span>


```C++
HRESULT MouseDown(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="39306-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39306-107">*Button*</span><span class="sxs-lookup"><span data-stu-id="39306-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="39306-108">Membre de l’énumération [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) qui indique les boutons de la souris qui ont été enfoncés.</span><span class="sxs-lookup"><span data-stu-id="39306-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were pressed.</span></span>



| <span data-ttu-id="39306-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="39306-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="39306-110">Signification</span><span class="sxs-lookup"><span data-stu-id="39306-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="39306-111"><dt>**Non \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="39306-112">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="39306-112">Default.</span></span> <span data-ttu-id="39306-113">Aucun bouton de la souris n'a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="39306-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="39306-114"><dt>À **gauche \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="39306-115">Le bouton gauche de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="39306-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="39306-116"><dt>À **droite \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="39306-117">Le bouton droit de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="39306-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="39306-118"><dt>**Au milieu \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="39306-119">Le bouton central de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="39306-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="39306-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="39306-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="39306-121">Membre de l’énumération [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) qui indique quelles touches de modification sont enfoncées au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="39306-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="39306-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="39306-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="39306-123">Signification</span><span class="sxs-lookup"><span data-stu-id="39306-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="39306-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="39306-125">Spécifie que la touche Maj a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="39306-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="39306-126"><dt>**IKM \_ Contrôle**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="39306-127">Spécifie que la touche CTRL a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="39306-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="39306-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="39306-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="39306-129">Spécifie que la touche ALT a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="39306-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="39306-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="39306-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="39306-131">Coordonnée x actuelle, en pixels, du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="39306-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="39306-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="39306-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="39306-133">Coordonnée y actuelle, en pixels, du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="39306-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39306-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39306-134">Return value</span></span>

<span data-ttu-id="39306-135">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="39306-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39306-136">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39306-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39306-137">Notes</span><span class="sxs-lookup"><span data-stu-id="39306-137">Remarks</span></span>

<span data-ttu-id="39306-138">Si un bouton de la souris est enfoncé alors que le pointeur est sur un contrôle [InkEdit](inkedit-control-reference.md) , ce contrôle capture la souris et reçoit tous les événements de la souris jusqu’au dernier événement [**MouseUp**](inkedit-mouseup.md) , y compris celui-ci.</span><span class="sxs-lookup"><span data-stu-id="39306-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="39306-139">Cela implique que les coordonnées du pointeur de la souris (x, y) retournées par un événement de souris ne se trouvent pas toujours dans la zone interne de l’objet qui les reçoit.</span><span class="sxs-lookup"><span data-stu-id="39306-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="39306-140">Si les boutons de la souris sont appuyés successivement, l’objet qui capture la souris après la première pression reçoit tous les événements de la souris jusqu’à ce que tous les boutons soient libérés.</span><span class="sxs-lookup"><span data-stu-id="39306-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="39306-141">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="39306-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="39306-142">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeMouseDown.</span><span class="sxs-lookup"><span data-stu-id="39306-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="39306-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39306-143">Requirements</span></span>



| <span data-ttu-id="39306-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39306-144">Requirement</span></span> | <span data-ttu-id="39306-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="39306-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39306-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39306-146">Minimum supported client</span></span><br/> | <span data-ttu-id="39306-147">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39306-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="39306-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39306-148">Minimum supported server</span></span><br/> | <span data-ttu-id="39306-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="39306-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="39306-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="39306-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="39306-151"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="39306-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="39306-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39306-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="39306-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39306-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="39306-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39306-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39306-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="39306-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="39306-156">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="39306-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="39306-157">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="39306-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="39306-158">[**MouseMove, événement \[ InkEdit, contrôle\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="39306-158">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> <dt>

<span data-ttu-id="39306-159">[**Contrôle InkEdit de l’événement MouseUp \[\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="39306-159">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

