---
title: Message BM_SETCHECK (winuser. h)
description: Définit l’état d’activation d’une case d’option ou d’une case à cocher. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro Button SetCheck.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032440"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="00179-105">\_Message SETCHECK BM</span><span class="sxs-lookup"><span data-stu-id="00179-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="00179-106">Définit l’état d’activation d’une case d’option ou d’une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="00179-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="00179-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**Button \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .</span><span class="sxs-lookup"><span data-stu-id="00179-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="00179-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00179-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00179-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00179-110">État d’activation.</span><span class="sxs-lookup"><span data-stu-id="00179-110">The check state.</span></span> <span data-ttu-id="00179-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="00179-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="00179-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="00179-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="00179-113">Signification</span><span class="sxs-lookup"><span data-stu-id="00179-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="00179-114"><dt>**BST \_ vérifié**</dt></span><span class="sxs-lookup"><span data-stu-id="00179-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="00179-115">Définit l’état du bouton sur activé.</span><span class="sxs-lookup"><span data-stu-id="00179-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="00179-116"><dt>**BST \_ indéterminé**</dt></span><span class="sxs-lookup"><span data-stu-id="00179-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="00179-117">Définit l’état du bouton sur grisé, ce qui indique un état indéterminé.</span><span class="sxs-lookup"><span data-stu-id="00179-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="00179-118">Utilisez cette valeur uniquement si le bouton a le style [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="00179-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="00179-119"><dt>**BST \_ désactivé**</dt></span><span class="sxs-lookup"><span data-stu-id="00179-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="00179-120">Définit l’état du bouton sur effacé.</span><span class="sxs-lookup"><span data-stu-id="00179-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="00179-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00179-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00179-122">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="00179-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00179-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00179-123">Return value</span></span>

<span data-ttu-id="00179-124">Ce message retourne toujours la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="00179-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="00179-125">Notes</span><span class="sxs-lookup"><span data-stu-id="00179-125">Remarks</span></span>

<span data-ttu-id="00179-126">Le **message \_ SETCHECK BM** n’a aucun effet sur les boutons de commande.</span><span class="sxs-lookup"><span data-stu-id="00179-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="00179-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00179-127">Requirements</span></span>



| <span data-ttu-id="00179-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00179-128">Requirement</span></span> | <span data-ttu-id="00179-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="00179-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00179-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00179-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00179-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00179-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00179-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00179-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00179-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00179-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00179-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="00179-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="00179-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00179-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00179-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00179-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="00179-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="00179-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="00179-138">**\_GETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="00179-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="00179-139">**\_GETSTATE BM**</span><span class="sxs-lookup"><span data-stu-id="00179-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="00179-140">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="00179-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





