---
title: Message EM_GETIMESTATUS (winuser. h)
description: Obtient un jeu d’indicateurs d’État qui indiquent comment le contrôle d’édition interagit avec l’éditeur de méthode d’entrée (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105121"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="d6a83-104">\_Message GETIMESTATUS em</span><span class="sxs-lookup"><span data-stu-id="d6a83-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="d6a83-105">Obtient un jeu d’indicateurs d’État qui indiquent comment le contrôle d’édition interagit avec l’éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="d6a83-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="d6a83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6a83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a83-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6a83-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a83-108">Type d’État à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d6a83-108">The type of status to retrieve.</span></span> <span data-ttu-id="d6a83-109">Ce paramètre peut avoir la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="d6a83-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="d6a83-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6a83-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="d6a83-111">Signification</span><span class="sxs-lookup"><span data-stu-id="d6a83-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="d6a83-112"><dt>**EMSIS \_ COMPOSITIONSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a83-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="d6a83-113">Définit le comportement de gestion de la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="d6a83-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d6a83-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6a83-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6a83-115">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d6a83-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a83-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6a83-116">Return value</span></span>

<span data-ttu-id="d6a83-117">Données spécifiques au type d’État à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d6a83-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="d6a83-118">Avec la valeur de **\_ COMPOSITIONSTRING EMSIS** pour l' *État*, cette valeur de retour est une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6a83-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="d6a83-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d6a83-119">Return code</span></span>                                                                                                    | <span data-ttu-id="d6a83-120">Description</span><span class="sxs-lookup"><span data-stu-id="d6a83-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6a83-121"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a83-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="d6a83-122">Si cet indicateur est défini, le contrôle d’édition intercepte le message de composition de l' [**\_ \_ IME WM**](/windows/desktop/Intl/wm-ime-composition) avec *fFlags* défini sur GC \_ RESULTSTR et retourne la chaîne de résultat immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d6a83-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="d6a83-123">Si cet indicateur n’est pas défini, le contrôle d’édition passe le message de **\_ \_ composition de l’IME WM** à la procédure de fenêtre par défaut et traite la chaîne de résultat à partir du message [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; il s’agit du comportement par défaut du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="d6a83-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="d6a83-124"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a83-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="d6a83-125">Si cet indicateur est défini, le contrôle d’édition annule la chaîne de composition lorsqu’il reçoit le message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="d6a83-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="d6a83-126">Si cet indicateur n’est pas défini, le contrôle d’édition n’annule pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="d6a83-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="d6a83-127"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a83-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="d6a83-128">Si cet indicateur est défini, le contrôle d’édition termine la chaîne de composition lors de la réception du message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="d6a83-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="d6a83-129">Si cet indicateur n’est pas défini, le contrôle d’édition ne termine pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="d6a83-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d6a83-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d6a83-130">Remarks</span></span>

<span data-ttu-id="d6a83-131">**Modification riche :** Le **message \_ GETIMESTATUS em** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d6a83-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a83-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6a83-132">Requirements</span></span>



| <span data-ttu-id="d6a83-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6a83-133">Requirement</span></span> | <span data-ttu-id="d6a83-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6a83-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a83-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6a83-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a83-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6a83-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6a83-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6a83-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a83-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6a83-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6a83-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6a83-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a83-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6a83-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a83-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6a83-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a83-142">**\_SETIMESTATUS em**</span><span class="sxs-lookup"><span data-stu-id="d6a83-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

