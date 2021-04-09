---
title: Message EM_SETIMESTATUS (winuser. h)
description: Définit les indicateurs d’État qui déterminent le mode d’interaction d’un contrôle d’édition avec l’éditeur de méthode d’entrée (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742012"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="9491d-104">\_Message SETIMESTATUS em</span><span class="sxs-lookup"><span data-stu-id="9491d-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="9491d-105">Définit les indicateurs d’État qui déterminent le mode d’interaction d’un contrôle d’édition avec l’éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="9491d-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="9491d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9491d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9491d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9491d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9491d-108">Type d’État à définir.</span><span class="sxs-lookup"><span data-stu-id="9491d-108">The type of status to set.</span></span> <span data-ttu-id="9491d-109">Ce paramètre peut avoir la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="9491d-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="9491d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9491d-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="9491d-111">Signification</span><span class="sxs-lookup"><span data-stu-id="9491d-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="9491d-112"><dt>**EMSIS \_ COMPOSITIONSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="9491d-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="9491d-113">Définit le comportement de la chaîne de composition de gestion.</span><span class="sxs-lookup"><span data-stu-id="9491d-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9491d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9491d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9491d-115">Données spécifiques au type d’État.</span><span class="sxs-lookup"><span data-stu-id="9491d-115">Data specific to the status type.</span></span> <span data-ttu-id="9491d-116">Si *wParam* est **EMSIS \_ COMPOSITIONSTRING**, ce paramètre peut avoir une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9491d-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="9491d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9491d-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="9491d-118">Signification</span><span class="sxs-lookup"><span data-stu-id="9491d-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="9491d-119"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="9491d-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="9491d-120">Si cet indicateur est défini, le contrôle d’édition intercepte le message de composition de l' [**\_ IME \_ WM**](/windows/desktop/Intl/wm-ime-composition) avec *lParam* défini sur GC \_ RESULTSTR et retourne la chaîne de résultat immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9491d-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="9491d-121">Si cet indicateur n’est pas défini, le contrôle d’édition passe le message de **\_ \_ composition de l’IME WM** à la procédure de fenêtre par défaut et gère la chaîne de résultat à partir du message [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; il s’agit du comportement par défaut du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="9491d-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="9491d-122"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="9491d-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="9491d-123">Si cet indicateur est défini, le contrôle d’édition annule la chaîne de composition lorsqu’il reçoit le message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="9491d-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="9491d-124">Si cet indicateur n’est pas défini, le contrôle d’édition n’annule pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="9491d-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="9491d-125"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="9491d-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="9491d-126">Si cet indicateur est défini, le contrôle d’édition termine la chaîne de composition lors de la réception du message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="9491d-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="9491d-127">Si cet indicateur n’est pas défini, le contrôle d’édition ne termine pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="9491d-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9491d-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9491d-128">Return value</span></span>

<span data-ttu-id="9491d-129">Retourne la valeur précédente du paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9491d-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="9491d-130">Notes</span><span class="sxs-lookup"><span data-stu-id="9491d-130">Remarks</span></span>

<span data-ttu-id="9491d-131">**Modification riche :** Le **message \_ SETIMESTATUS em** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9491d-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9491d-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9491d-132">Requirements</span></span>



| <span data-ttu-id="9491d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9491d-133">Requirement</span></span> | <span data-ttu-id="9491d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9491d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9491d-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9491d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9491d-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9491d-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9491d-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9491d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9491d-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9491d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9491d-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="9491d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9491d-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9491d-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9491d-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9491d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9491d-142">**\_GETIMESTATUS em**</span><span class="sxs-lookup"><span data-stu-id="9491d-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

