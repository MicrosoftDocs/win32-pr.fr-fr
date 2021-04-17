---
description: Se produit lorsque l’utilisateur relâche une touche alors que le contrôle InkEdit a le focus.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Événement InkEdit. KeyUp (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530045"
---
# <a name="inkeditkeyup-event"></a><span data-ttu-id="22a1c-103">InkEdit. KeyUp, événement</span><span class="sxs-lookup"><span data-stu-id="22a1c-103">InkEdit.KeyUp event</span></span>

<span data-ttu-id="22a1c-104">Se produit lorsque l’utilisateur relâche une touche alors que le contrôle [InkEdit](inkedit-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="22a1c-104">Occurs when the user releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a1c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22a1c-105">Syntax</span></span>


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="22a1c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22a1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a1c-107">*A-la*</span><span class="sxs-lookup"><span data-stu-id="22a1c-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="22a1c-108">Code de la touche virtuelle de la touche enfoncée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22a1c-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="22a1c-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="22a1c-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="22a1c-110">Membre de l’énumération [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) qui indique quelles touches de modification sont enfoncées au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="22a1c-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="22a1c-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="22a1c-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="22a1c-112">Signification</span><span class="sxs-lookup"><span data-stu-id="22a1c-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="22a1c-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="22a1c-114">Spécifie que la touche Maj a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="22a1c-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="22a1c-115"><dt>**IKM \_ Contrôle**</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="22a1c-116">Spécifie que la touche CTRL a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="22a1c-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="22a1c-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="22a1c-118">Spécifie que la touche ALT a été utilisée comme modificateur.</span><span class="sxs-lookup"><span data-stu-id="22a1c-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a1c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22a1c-119">Return value</span></span>

<span data-ttu-id="22a1c-120">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22a1c-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22a1c-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22a1c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a1c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="22a1c-122">Remarks</span></span>

<span data-ttu-id="22a1c-123">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="22a1c-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="22a1c-124">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeKeyUp.</span><span class="sxs-lookup"><span data-stu-id="22a1c-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a1c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22a1c-125">Requirements</span></span>



| <span data-ttu-id="22a1c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22a1c-126">Requirement</span></span> | <span data-ttu-id="22a1c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="22a1c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a1c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22a1c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22a1c-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22a1c-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="22a1c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22a1c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22a1c-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="22a1c-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="22a1c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="22a1c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="22a1c-133"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="22a1c-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22a1c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="22a1c-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22a1c-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="22a1c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22a1c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a1c-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="22a1c-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="22a1c-138">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="22a1c-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="22a1c-139">[**KeyOut, événement \[ InkEdit, contrôle\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="22a1c-139">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="22a1c-140">[**Événement KeyPress \[ InkEdit, contrôle\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="22a1c-140">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> </dl>

 

