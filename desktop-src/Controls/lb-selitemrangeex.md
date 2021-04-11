---
title: Message LB_SELITEMRANGEEX (winuser. h)
description: Sélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942659"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="0dc4d-104">\_Message SELITEMRANGEEX lb</span><span class="sxs-lookup"><span data-stu-id="0dc4d-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="0dc4d-105">Sélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0dc4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dc4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc4d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0dc4d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0dc4d-108">Spécifie l’index de base zéro du premier élément à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="0dc4d-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="0dc4d-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="0dc4d-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="0dc4d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0dc4d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0dc4d-113">Spécifie l’index de base zéro du dernier élément à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc4d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dc4d-114">Return value</span></span>

<span data-ttu-id="0dc4d-115">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc4d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0dc4d-116">Remarks</span></span>

<span data-ttu-id="0dc4d-117">Si le paramètre *wParam* est inférieur au paramètre *lParam* , la plage d’éléments spécifiée est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="0dc4d-118">Si *wParam* est supérieur ou égal à *lParam*, la plage est supprimée de la plage d’éléments spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="0dc4d-119">Pour sélectionner un seul élément, sélectionnez deux éléments, puis désélectionnez l’élément indésirable.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="0dc4d-120">Utilisez ce message uniquement avec les zones de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="0dc4d-121">Ce message peut sélectionner une plage uniquement dans les 65 536 premiers éléments.</span><span class="sxs-lookup"><span data-stu-id="0dc4d-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc4d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dc4d-122">Requirements</span></span>



| <span data-ttu-id="0dc4d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dc4d-123">Requirement</span></span> | <span data-ttu-id="0dc4d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dc4d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc4d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc4d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc4d-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc4d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0dc4d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc4d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc4d-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc4d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0dc4d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0dc4d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc4d-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dc4d-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dc4d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dc4d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="0dc4d-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0dc4d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0dc4d-133">**\_SELITEMRANGE lb**</span><span class="sxs-lookup"><span data-stu-id="0dc4d-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="0dc4d-134">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="0dc4d-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





