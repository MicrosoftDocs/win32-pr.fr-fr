---
title: Message LB_INSERTSTRING (winuser. h)
description: Insère une chaîne ou des données d’élément dans une zone de liste. Contrairement au \_ message lb ADDSTRING, le \_ message INSERTSTRING ne provoque pas le tri d’une liste avec le style de tri lbs \_ .
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105544"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="37c54-105">\_Message INSERTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="37c54-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="37c54-106">Insère une chaîne ou des données d’élément dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="37c54-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="37c54-107">Contrairement au message [**lb \_ ADDSTRING**](lb-addstring.md) , le **message \_ INSERTSTRING** ne provoque pas le tri d’une liste avec le style de [**\_ Tri lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="37c54-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="37c54-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37c54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37c54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37c54-110">Index de base zéro de la position à laquelle insérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="37c54-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="37c54-111">Si ce paramètre a la valeur-1, la chaîne est ajoutée à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="37c54-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="37c54-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37c54-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37c54-113">Pointeur vers la chaîne terminée par le caractère null à insérer.</span><span class="sxs-lookup"><span data-stu-id="37c54-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="37c54-114">Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , ce paramètre est stocké en tant que données d’élément au lieu d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="37c54-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="37c54-115">Vous pouvez envoyer les messages [**lb \_ GETITEMDATA**](lb-getitemdata.md) et [**\_ SETITEMDATA**](lb-setitemdata.md) pour extraire ou modifier les données de l’élément.</span><span class="sxs-lookup"><span data-stu-id="37c54-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c54-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37c54-116">Return value</span></span>

<span data-ttu-id="37c54-117">La valeur de retour est l’index de la position à laquelle la chaîne a été insérée.</span><span class="sxs-lookup"><span data-stu-id="37c54-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="37c54-118">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="37c54-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="37c54-119">Si l’espace est insuffisant pour stocker la nouvelle chaîne, la valeur de retour est LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="37c54-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c54-120">Notes</span><span class="sxs-lookup"><span data-stu-id="37c54-120">Remarks</span></span>

<span data-ttu-id="37c54-121">Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100).</span><span class="sxs-lookup"><span data-stu-id="37c54-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="37c54-122">Il réserve la quantité de mémoire spécifiée afin que les **messages \_ INSERTSTRING** suivants prennent le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="37c54-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="37c54-123">Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* .</span><span class="sxs-lookup"><span data-stu-id="37c54-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="37c54-124">Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.</span><span class="sxs-lookup"><span data-stu-id="37c54-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="37c54-125">Si la zone de liste a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous insérez une chaîne plus grande que la zone de liste, envoyez un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.</span><span class="sxs-lookup"><span data-stu-id="37c54-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="37c54-126">Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="37c54-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="37c54-127">Cela peut entraîner des problèmes.</span><span class="sxs-lookup"><span data-stu-id="37c54-127">This can cause problems.</span></span> <span data-ttu-id="37c54-128">Par exemple, les caractères romains accentués dans une zone de liste non Unicode dans les fenêtres japonaises sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="37c54-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="37c54-129">Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="37c54-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="37c54-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37c54-130">Requirements</span></span>



| <span data-ttu-id="37c54-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37c54-131">Requirement</span></span> | <span data-ttu-id="37c54-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="37c54-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c54-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37c54-133">Minimum supported client</span></span><br/> | <span data-ttu-id="37c54-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37c54-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="37c54-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37c54-135">Minimum supported server</span></span><br/> | <span data-ttu-id="37c54-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37c54-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37c54-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="37c54-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="37c54-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37c54-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c54-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37c54-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="37c54-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="37c54-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37c54-141">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="37c54-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="37c54-142">**\_SELECTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="37c54-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="37c54-143">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="37c54-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

