---
title: Message LB_SETCURSEL (winuser. h)
description: Sélectionne une chaîne et la fait défiler en vue, si nécessaire. Lorsque la nouvelle chaîne est sélectionnée, la zone de liste supprime la mise en surbrillance de la chaîne précédemment sélectionnée.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511794"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="5a0be-105">\_Message SETCURSEL lb</span><span class="sxs-lookup"><span data-stu-id="5a0be-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="5a0be-106">Sélectionne une chaîne et la fait défiler en vue, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5a0be-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="5a0be-107">Lorsque la nouvelle chaîne est sélectionnée, la zone de liste supprime la mise en surbrillance de la chaîne précédemment sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5a0be-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a0be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a0be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a0be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a0be-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a0be-110">Spécifie l’index de base zéro de la chaîne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5a0be-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="5a0be-111">Si ce paramètre a la valeur-1, la zone de liste est définie sur ne pas sélectionner.</span><span class="sxs-lookup"><span data-stu-id="5a0be-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="5a0be-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5a0be-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5a0be-113">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="5a0be-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5a0be-114">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="5a0be-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5a0be-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a0be-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a0be-116">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5a0be-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a0be-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a0be-117">Return value</span></span>

<span data-ttu-id="5a0be-118">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="5a0be-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="5a0be-119">Si le paramètre *wParam* est-1, la valeur de retour est lb \_ Err même si aucune erreur ne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5a0be-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a0be-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5a0be-120">Remarks</span></span>

<span data-ttu-id="5a0be-121">Utilisez ce message uniquement avec les zones de liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="5a0be-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="5a0be-122">Vous ne pouvez pas l’utiliser pour définir ou supprimer une sélection dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="5a0be-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0be-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a0be-123">Requirements</span></span>



| <span data-ttu-id="5a0be-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a0be-124">Requirement</span></span> | <span data-ttu-id="5a0be-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a0be-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0be-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a0be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0be-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a0be-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a0be-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a0be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0be-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a0be-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a0be-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a0be-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a0be-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a0be-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0be-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a0be-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0be-133">**\_GETCURSEL lb**</span><span class="sxs-lookup"><span data-stu-id="5a0be-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





