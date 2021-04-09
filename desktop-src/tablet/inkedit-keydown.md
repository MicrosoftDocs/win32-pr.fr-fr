---
description: Se produit lorsque l’utilisateur appuie sur une touche alors que le contrôle InkEdit a le focus.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Événement InkEdit. KEYpoint (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952920"
---
# <a name="inkeditkeydown-event"></a><span data-ttu-id="3df1a-103">InkEdit. KeyOut, événement</span><span class="sxs-lookup"><span data-stu-id="3df1a-103">InkEdit.KeyDown event</span></span>

<span data-ttu-id="3df1a-104">Se produit lorsque l’utilisateur appuie sur une touche alors que le contrôle [InkEdit](inkedit-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="3df1a-104">Occurs when the user presses a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3df1a-105">Syntax</span></span>


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="3df1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3df1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df1a-107">*A-la*</span><span class="sxs-lookup"><span data-stu-id="3df1a-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="3df1a-108">Code de la touche virtuelle de la touche enfoncée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3df1a-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="3df1a-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="3df1a-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="3df1a-110">Membre de l’énumération [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , qui indique quelles touches de modification sont enfoncées au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="3df1a-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration, that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="3df1a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3df1a-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="3df1a-112">Signification</span><span class="sxs-lookup"><span data-stu-id="3df1a-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="3df1a-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="3df1a-114">Spécifie que la touche Maj a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="3df1a-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="3df1a-115"><dt>**IKM \_ Contrôle**</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="3df1a-116">Spécifie que la touche CTRL a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="3df1a-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="3df1a-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="3df1a-118">Spécifie que la touche ALT a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="3df1a-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df1a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3df1a-119">Return value</span></span>

<span data-ttu-id="3df1a-120">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3df1a-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3df1a-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3df1a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3df1a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3df1a-122">Remarks</span></span>

<span data-ttu-id="3df1a-123">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="3df1a-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="3df1a-124">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeKeyDown.</span><span class="sxs-lookup"><span data-stu-id="3df1a-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df1a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3df1a-125">Requirements</span></span>



| <span data-ttu-id="3df1a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3df1a-126">Requirement</span></span> | <span data-ttu-id="3df1a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3df1a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df1a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3df1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3df1a-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3df1a-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3df1a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3df1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3df1a-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3df1a-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3df1a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3df1a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df1a-133"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3df1a-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3df1a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="3df1a-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df1a-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3df1a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3df1a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df1a-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="3df1a-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3df1a-138">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="3df1a-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="3df1a-139">[**Événement KeyPress \[ InkEdit, contrôle\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="3df1a-139">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> <dt>

<span data-ttu-id="3df1a-140">[**Événement KeyUp \[ contrôle InkEdit\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="3df1a-140">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

