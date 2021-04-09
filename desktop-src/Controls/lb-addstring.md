---
title: Message LB_ADDSTRING (winuser. h)
description: Ajoute une chaîne à une zone de liste. Si la zone de liste n’a pas le \_ style de tri lbs, la chaîne est ajoutée à la fin de la liste. Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032793"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="c56e0-106">Message g LB \_</span><span class="sxs-lookup"><span data-stu-id="c56e0-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="c56e0-107">Ajoute une chaîne à une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="c56e0-107">Adds a string to a list box.</span></span> <span data-ttu-id="c56e0-108">Si la zone de liste n’a pas le style de [**\_ Tri lbs**](list-box-styles.md) , la chaîne est ajoutée à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="c56e0-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="c56e0-109">Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.</span><span class="sxs-lookup"><span data-stu-id="c56e0-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="c56e0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c56e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56e0-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c56e0-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c56e0-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c56e0-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c56e0-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c56e0-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c56e0-114">Pointeur vers la chaîne terminée par le caractère null qui doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="c56e0-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="c56e0-115">Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , ce paramètre est stocké en tant que données d’élément au lieu d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c56e0-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="c56e0-116">Vous pouvez envoyer les messages **lb \_ GETITEMDATA** et **\_ SETITEMDATA** pour extraire ou modifier les données de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c56e0-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56e0-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c56e0-117">Return value</span></span>

<span data-ttu-id="c56e0-118">La valeur de retour est l’index de base zéro de la chaîne dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="c56e0-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="c56e0-119">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c56e0-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="c56e0-120">Si l’espace est insuffisant pour stocker la nouvelle chaîne, la valeur de retour est LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="c56e0-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56e0-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c56e0-121">Remarks</span></span>

<span data-ttu-id="c56e0-122">Si la zone de liste a un style owner-drawn et le style de [**\_ Tri lbs**](list-box-styles.md) , mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le système envoie une ou plusieurs fois le message [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour placer correctement le nouvel élément dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="c56e0-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="c56e0-123">Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100).</span><span class="sxs-lookup"><span data-stu-id="c56e0-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="c56e0-124">Il réserve la quantité de mémoire spécifiée, de sorte **que \_ les messages de** l’équilibreur de volume suivant prennent le plus de temps possible.</span><span class="sxs-lookup"><span data-stu-id="c56e0-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="c56e0-125">Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c56e0-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="c56e0-126">Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.</span><span class="sxs-lookup"><span data-stu-id="c56e0-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="c56e0-127">Si la zone de liste a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous ajoutez une chaîne plus grande que la zone de liste, envoyez un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c56e0-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="c56e0-128">Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="c56e0-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="c56e0-129">Cela peut entraîner des problèmes.</span><span class="sxs-lookup"><span data-stu-id="c56e0-129">This can cause problems.</span></span> <span data-ttu-id="c56e0-130">Par exemple, les caractères romains accentués dans une zone de liste non Unicode dans les fenêtres japonaises sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="c56e0-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="c56e0-131">Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="c56e0-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56e0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c56e0-132">Requirements</span></span>



| <span data-ttu-id="c56e0-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c56e0-133">Requirement</span></span> | <span data-ttu-id="c56e0-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c56e0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56e0-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c56e0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c56e0-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c56e0-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c56e0-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c56e0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c56e0-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c56e0-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c56e0-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="c56e0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c56e0-140"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c56e0-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56e0-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c56e0-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="c56e0-142">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c56e0-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c56e0-143">**\_DELETESTRING lb**</span><span class="sxs-lookup"><span data-stu-id="c56e0-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="c56e0-144">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="c56e0-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="c56e0-145">**\_SELECTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="c56e0-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="c56e0-146">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="c56e0-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="c56e0-147">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="c56e0-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

