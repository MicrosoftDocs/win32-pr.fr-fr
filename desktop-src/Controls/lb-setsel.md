---
title: Message LB_SETSEL (winuser. h)
description: Sélectionne un élément dans une zone de liste à sélection multiple et, si nécessaire, fait défiler l’élément dans l’affichage.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466522"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="c8795-104">\_Message SETSEL lb</span><span class="sxs-lookup"><span data-stu-id="c8795-104">LB\_SETSEL message</span></span>

<span data-ttu-id="c8795-105">Sélectionne un élément dans une zone de liste à sélection multiple et, si nécessaire, fait défiler l’élément dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="c8795-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8795-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8795-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8795-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8795-108">Spécifie comment définir la sélection.</span><span class="sxs-lookup"><span data-stu-id="c8795-108">Specifies how to set the selection.</span></span> <span data-ttu-id="c8795-109">Si ce paramètre a la **valeur true**, l’élément est sélectionné et mis en surbrillance ; Si la **valeur est false**, la mise en surbrillance est supprimée et l’élément n’est plus sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c8795-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="c8795-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8795-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8795-111">Spécifie l’index de base zéro de l’élément à définir.</span><span class="sxs-lookup"><span data-stu-id="c8795-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="c8795-112">Si ce paramètre a la valeur-1, la sélection est ajoutée ou supprimée de tous les éléments, en fonction de la valeur de *wParam*, et aucun défilement ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c8795-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8795-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8795-113">Return value</span></span>

<span data-ttu-id="c8795-114">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c8795-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8795-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c8795-115">Remarks</span></span>

<span data-ttu-id="c8795-116">Utilisez ce message uniquement avec les zones de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="c8795-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8795-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8795-117">Requirements</span></span>



| <span data-ttu-id="c8795-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8795-118">Requirement</span></span> | <span data-ttu-id="c8795-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8795-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8795-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8795-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8795-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8795-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8795-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8795-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8795-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8795-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8795-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8795-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8795-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8795-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8795-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8795-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8795-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c8795-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8795-128">**\_GETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="c8795-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="c8795-129">**\_SELITEMRANGE lb**</span><span class="sxs-lookup"><span data-stu-id="c8795-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





