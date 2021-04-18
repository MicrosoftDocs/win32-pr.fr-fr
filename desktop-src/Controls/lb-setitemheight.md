---
title: Message LB_SETITEMHEIGHT (winuser. h)
description: Définit la hauteur, en pixels, des éléments d’une zone de liste. Si la zone de liste présente le \_ style OWNERDRAWVARIABLE, ce message définit la hauteur de l’élément spécifié par le paramètre wParam. Dans le cas contraire, ce message définit la hauteur de tous les éléments de la zone de liste.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466523"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="83080-106">\_Message SETITEMHEIGHT lb</span><span class="sxs-lookup"><span data-stu-id="83080-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="83080-107">Définit la hauteur, en pixels, des éléments d’une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="83080-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="83080-108">Si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) , ce message définit la hauteur de l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="83080-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="83080-109">Dans le cas contraire, ce message définit la hauteur de tous les éléments de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="83080-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="83080-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83080-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83080-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83080-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83080-112">Spécifie l’index de base zéro de l’élément dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="83080-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="83080-113">Utilisez ce paramètre uniquement si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) . sinon, affectez-lui la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="83080-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="83080-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="83080-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="83080-115">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="83080-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="83080-116">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="83080-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="83080-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83080-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83080-118">Spécifie la hauteur, en pixels, de l’élément.</span><span class="sxs-lookup"><span data-stu-id="83080-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="83080-119">La hauteur maximale est de 255 pixels.</span><span class="sxs-lookup"><span data-stu-id="83080-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83080-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83080-120">Return value</span></span>

<span data-ttu-id="83080-121">Si l’index ou la hauteur n’est pas valide, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="83080-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="83080-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83080-122">Requirements</span></span>



| <span data-ttu-id="83080-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83080-123">Requirement</span></span> | <span data-ttu-id="83080-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="83080-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83080-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83080-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83080-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83080-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83080-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83080-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83080-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83080-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83080-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="83080-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="83080-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83080-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83080-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83080-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83080-132">**\_GETITEMHEIGHT lb**</span><span class="sxs-lookup"><span data-stu-id="83080-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 





