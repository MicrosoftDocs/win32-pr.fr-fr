---
description: Se produit lorsque l’utilisateur déplace la souris alors que la souris se trouve sur le contrôle InkEdit.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: InkEdit. MouseMove, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0d3e98827a1f0ebcdc80f5d44765ebe768f65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534599"
---
# <a name="inkeditmousemove-event"></a><span data-ttu-id="0cae7-103">InkEdit. MouseMove, événement</span><span class="sxs-lookup"><span data-stu-id="0cae7-103">InkEdit.MouseMove event</span></span>

<span data-ttu-id="0cae7-104">Se produit lorsque l’utilisateur déplace la souris alors que la souris se trouve sur le contrôle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0cae7-104">Occurs when the user moves the mouse while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cae7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cae7-105">Syntax</span></span>


```C++
HRESULT MouseMove(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="0cae7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cae7-107">*Button*</span><span class="sxs-lookup"><span data-stu-id="0cae7-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="0cae7-108">Membre de l’énumération [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) qui indique les boutons de la souris qui sont enfoncés.</span><span class="sxs-lookup"><span data-stu-id="0cae7-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons are depressed.</span></span>



| <span data-ttu-id="0cae7-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cae7-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="0cae7-110">Signification</span><span class="sxs-lookup"><span data-stu-id="0cae7-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="0cae7-111"><dt>**Non \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="0cae7-112">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="0cae7-112">Default.</span></span> <span data-ttu-id="0cae7-113">Aucun bouton de la souris n'a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="0cae7-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="0cae7-114"><dt>À **gauche \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="0cae7-115">Le bouton gauche de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="0cae7-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="0cae7-116"><dt>À **droite \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="0cae7-117">Le bouton droit de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="0cae7-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="0cae7-118"><dt>**Au milieu \_ BOUTON**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="0cae7-119">Le bouton central de la souris a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="0cae7-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="0cae7-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="0cae7-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="0cae7-121">Membre de l’énumération [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) qui indique quelles touches de modification sont enfoncées au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="0cae7-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="0cae7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cae7-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="0cae7-123">Signification</span><span class="sxs-lookup"><span data-stu-id="0cae7-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="0cae7-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="0cae7-125">Spécifie que la touche Maj a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="0cae7-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="0cae7-126"><dt>**IKM \_ Contrôle**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="0cae7-127">Spécifie que la touche CTRL a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="0cae7-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="0cae7-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="0cae7-129">Spécifie que la touche ALT a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="0cae7-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="0cae7-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="0cae7-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="0cae7-131">Coordonnée x actuelle, en pixels, du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="0cae7-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="0cae7-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="0cae7-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="0cae7-133">Coordonnée y actuelle, en pixels, du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="0cae7-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cae7-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cae7-134">Return value</span></span>

<span data-ttu-id="0cae7-135">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0cae7-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cae7-136">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cae7-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cae7-137">Notes</span><span class="sxs-lookup"><span data-stu-id="0cae7-137">Remarks</span></span>

<span data-ttu-id="0cae7-138">Si un bouton de la souris est enfoncé alors que le pointeur est sur un contrôle [InkEdit](inkedit-control-reference.md) , ce contrôle capture la souris et reçoit tous les événements de la souris jusqu’au dernier événement [**MouseUp**](inkedit-mouseup.md) , y compris celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0cae7-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="0cae7-139">Cela implique que les coordonnées du pointeur de la souris (x, y) retournées par un événement de souris ne se trouvent pas toujours dans la zone interne de l’objet qui les reçoit.</span><span class="sxs-lookup"><span data-stu-id="0cae7-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="0cae7-140">Si les boutons de la souris sont appuyés successivement, l’objet qui capture la souris après la première pression reçoit tous les événements de la souris jusqu’à ce que tous les boutons soient libérés.</span><span class="sxs-lookup"><span data-stu-id="0cae7-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="0cae7-141">L’événement **MouseMove** est généré continuellement lorsque le pointeur de la souris se déplace entre les objets.</span><span class="sxs-lookup"><span data-stu-id="0cae7-141">The **MouseMove** event is generated continually as the mouse pointer moves across objects.</span></span> <span data-ttu-id="0cae7-142">À moins qu’un autre objet n’ait capturé la souris, un contrôle [InkEdit](inkedit-control-reference.md) reconnaît un événement **MouseMove** lorsque la position de la souris se trouve dans ses limites.</span><span class="sxs-lookup"><span data-stu-id="0cae7-142">Unless another object has captured the mouse, an [InkEdit](inkedit-control-reference.md) control recognizes a **MouseMove** event whenever the mouse position is within its borders.</span></span>

<span data-ttu-id="0cae7-143">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="0cae7-143">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="0cae7-144">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeMouseMove.</span><span class="sxs-lookup"><span data-stu-id="0cae7-144">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cae7-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cae7-145">Requirements</span></span>



| <span data-ttu-id="0cae7-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cae7-146">Requirement</span></span> | <span data-ttu-id="0cae7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cae7-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cae7-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cae7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0cae7-149">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cae7-149">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0cae7-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cae7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0cae7-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cae7-151">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0cae7-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cae7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cae7-153"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-153"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0cae7-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0cae7-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cae7-155"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cae7-155"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0cae7-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cae7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cae7-157">InkEdit</span><span class="sxs-lookup"><span data-stu-id="0cae7-157">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0cae7-158">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="0cae7-158">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="0cae7-159">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="0cae7-159">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="0cae7-160">[**Événement MouseDown, \[ contrôle InkEdit\]**](inkedit-mousedown.md)</span><span class="sxs-lookup"><span data-stu-id="0cae7-160">[**MouseDown Event \[InkEdit Control\]**](inkedit-mousedown.md)</span></span>
</dt> <dt>

<span data-ttu-id="0cae7-161">[**Contrôle InkEdit de l’événement MouseUp \[\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="0cae7-161">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

