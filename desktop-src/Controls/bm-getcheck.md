---
title: Message BM_GETCHECK (winuser. h)
description: Obtient l’état d’activation d’une case d’option ou d’une case à cocher. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetCheck macro.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105769"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="0e01d-105">\_Message GETCHECK BM</span><span class="sxs-lookup"><span data-stu-id="0e01d-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="0e01d-106">Obtient l’état d’activation d’une case d’option ou d’une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="0e01d-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="0e01d-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span><span class="sxs-lookup"><span data-stu-id="0e01d-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e01d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e01d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e01d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e01d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e01d-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0e01d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0e01d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e01d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e01d-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0e01d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e01d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e01d-113">Return value</span></span>

<span data-ttu-id="0e01d-114">La valeur renvoyée par un bouton créé à l’aide de la fonction [**BS \_ autocase**](button-styles.md), [**BS \_ RadioButton**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), [**BS \_ case**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)ou [**BS \_ 3STATE**](button-styles.md) style peut être l’une des suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e01d-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="0e01d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0e01d-115">Return code</span></span>                                                                                       | <span data-ttu-id="0e01d-116">Description</span><span class="sxs-lookup"><span data-stu-id="0e01d-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e01d-117"><dt>**BST \_ vérifié**</dt></span><span class="sxs-lookup"><span data-stu-id="0e01d-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="0e01d-118">Le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="0e01d-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="0e01d-119"><dt>**BST \_ indéterminé**</dt></span><span class="sxs-lookup"><span data-stu-id="0e01d-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="0e01d-120">Le bouton est grisé, ce qui indique un état indéterminé (s’applique uniquement si le bouton a le style [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="0e01d-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="0e01d-121"><dt>**BST \_ désactivé**</dt></span><span class="sxs-lookup"><span data-stu-id="0e01d-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="0e01d-122">Le bouton est désactivé</span><span class="sxs-lookup"><span data-stu-id="0e01d-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="0e01d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0e01d-123">Remarks</span></span>

<span data-ttu-id="0e01d-124">Si le style du bouton est différent de ceux indiqués dans la liste, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="0e01d-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e01d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e01d-125">Requirements</span></span>



| <span data-ttu-id="0e01d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e01d-126">Requirement</span></span> | <span data-ttu-id="0e01d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e01d-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e01d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e01d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e01d-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e01d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0e01d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e01d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e01d-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e01d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e01d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e01d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e01d-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e01d-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e01d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e01d-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e01d-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0e01d-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e01d-136">**\_GETSTATE BM**</span><span class="sxs-lookup"><span data-stu-id="0e01d-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="0e01d-137">**\_SETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="0e01d-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





