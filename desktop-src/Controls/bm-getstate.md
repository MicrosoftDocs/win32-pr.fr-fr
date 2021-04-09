---
title: Message BM_GETSTATE (winuser. h)
description: Récupère l’état d’un bouton ou d’une case à cocher. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetState macro.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941721"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="460af-105">\_Message GETSTATE BM</span><span class="sxs-lookup"><span data-stu-id="460af-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="460af-106">Récupère l’état d’un bouton ou d’une case à cocher.</span><span class="sxs-lookup"><span data-stu-id="460af-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="460af-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span><span class="sxs-lookup"><span data-stu-id="460af-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="460af-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="460af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460af-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="460af-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="460af-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="460af-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="460af-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="460af-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="460af-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="460af-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="460af-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="460af-113">Return value</span></span>

<span data-ttu-id="460af-114">La valeur de retour spécifie l’état actuel du bouton.</span><span class="sxs-lookup"><span data-stu-id="460af-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="460af-115">Il s’agit d’une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="460af-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="460af-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="460af-116">Return code</span></span>                                                                                        | <span data-ttu-id="460af-117">Description</span><span class="sxs-lookup"><span data-stu-id="460af-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="460af-118"><dt>**BST \_ vérifié**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="460af-119">Le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="460af-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="460af-120"><dt>**BST \_ DROPDOWNPUSHED**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="460af-121">[Windows Vista](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="460af-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="460af-122">Le bouton est dans l’État déroulant.</span><span class="sxs-lookup"><span data-stu-id="460af-122">The button is in the drop-down state.</span></span> <span data-ttu-id="460af-123">S’applique uniquement si le bouton a le style de [**\_ liste déroulante TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="460af-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="460af-124"><dt>**\_focus BST**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="460af-125">Le bouton a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="460af-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="460af-126"><dt>**BST \_ chaud**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="460af-127">Le bouton est actif ; autrement dit, la souris pointe dessus.</span><span class="sxs-lookup"><span data-stu-id="460af-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="460af-128"><dt>**BST \_ indéterminé**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="460af-129">L’état du bouton est indéterminé.</span><span class="sxs-lookup"><span data-stu-id="460af-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="460af-130">S’applique uniquement si le bouton a le style [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="460af-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="460af-131"><dt>**BST \_ poussé**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="460af-132">Le bouton est affiché dans l’État pushd.</span><span class="sxs-lookup"><span data-stu-id="460af-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="460af-133"><dt>**BST \_ désactivé**</dt></span><span class="sxs-lookup"><span data-stu-id="460af-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="460af-134">Aucun état spécial.</span><span class="sxs-lookup"><span data-stu-id="460af-134">No special state.</span></span> <span data-ttu-id="460af-135">Équivalent à zéro.</span><span class="sxs-lookup"><span data-stu-id="460af-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="460af-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="460af-136">Requirements</span></span>



| <span data-ttu-id="460af-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="460af-137">Requirement</span></span> | <span data-ttu-id="460af-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="460af-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460af-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="460af-139">Minimum supported client</span></span><br/> | <span data-ttu-id="460af-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="460af-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="460af-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="460af-141">Minimum supported server</span></span><br/> | <span data-ttu-id="460af-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="460af-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="460af-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="460af-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="460af-144"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="460af-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="460af-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="460af-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="460af-146">**Référence**</span><span class="sxs-lookup"><span data-stu-id="460af-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="460af-147">**\_GETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="460af-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="460af-148">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="460af-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





