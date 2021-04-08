---
title: Message LB_SETCARETINDEX (winuser. h)
description: Définit le rectangle de focus sur l’élément à l’index spécifié dans une zone de liste à sélection multiple. Si l’élément n’est pas visible, il fait l’objet d’un défilement dans la vue.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844113"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="7d120-105">\_Message SETCARETINDEX lb</span><span class="sxs-lookup"><span data-stu-id="7d120-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="7d120-106">Définit le rectangle de focus sur l’élément à l’index spécifié dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="7d120-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="7d120-107">Si l’élément n’est pas visible, il fait l’objet d’un défilement dans la vue.</span><span class="sxs-lookup"><span data-stu-id="7d120-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d120-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d120-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d120-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d120-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d120-110">Spécifie l’index de base zéro de l’élément de zone de liste qui doit recevoir le rectangle de focus.</span><span class="sxs-lookup"><span data-stu-id="7d120-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="7d120-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7d120-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="7d120-112">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="7d120-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="7d120-113">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="7d120-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="7d120-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d120-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d120-115">Si cette valeur est **false**, l’élément fait l’objet d’un défilement jusqu’à ce qu’il soit entièrement visible. Si la **valeur est true**, l’élément fait l’objet d’un défilement jusqu’à ce qu’il soit au moins partiellement visible.</span><span class="sxs-lookup"><span data-stu-id="7d120-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d120-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d120-116">Return value</span></span>

<span data-ttu-id="7d120-117">Si une erreur se produit, la valeur de retour est LB \_ Err (-1).</span><span class="sxs-lookup"><span data-stu-id="7d120-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="7d120-118">Dans le cas contraire, LB \_ Okay (0) est retourné.</span><span class="sxs-lookup"><span data-stu-id="7d120-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d120-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7d120-119">Remarks</span></span>

<span data-ttu-id="7d120-120">Si ce message est envoyé à une zone de liste à sélection unique qui ne contient pas d’élément sélectionné, l’index du signe insertion est défini sur l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="7d120-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="7d120-121">Si la zone de liste à sélection unique contient un élément sélectionné, la zone de liste retourne LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="7d120-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d120-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d120-122">Requirements</span></span>



| <span data-ttu-id="7d120-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d120-123">Requirement</span></span> | <span data-ttu-id="7d120-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d120-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d120-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d120-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7d120-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d120-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d120-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d120-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7d120-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d120-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d120-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d120-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d120-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d120-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d120-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d120-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d120-132">**\_GETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="7d120-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





