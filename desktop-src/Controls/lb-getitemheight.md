---
title: Message LB_GETITEMHEIGHT (winuser. h)
description: Obtient la hauteur des éléments dans une zone de liste.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843433"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="92e05-104">\_Message GETITEMHEIGHT lb</span><span class="sxs-lookup"><span data-stu-id="92e05-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="92e05-105">Obtient la hauteur des éléments dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="92e05-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="92e05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92e05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92e05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92e05-108">Index de base zéro de l’élément de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="92e05-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="92e05-109">Cet index est utilisé uniquement si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) . sinon, elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="92e05-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="92e05-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="92e05-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="92e05-111">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="92e05-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="92e05-112">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="92e05-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="92e05-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92e05-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92e05-114">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="92e05-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e05-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92e05-115">Return value</span></span>

<span data-ttu-id="92e05-116">La valeur de retour correspond à la hauteur, en pixels, de chaque élément de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="92e05-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="92e05-117">La valeur de retour correspond à la hauteur de l’élément spécifié par le paramètre *wParam* si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="92e05-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="92e05-118">La valeur de retour est LB \_ Err si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="92e05-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e05-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92e05-119">Requirements</span></span>



| <span data-ttu-id="92e05-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92e05-120">Requirement</span></span> | <span data-ttu-id="92e05-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="92e05-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e05-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92e05-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92e05-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92e05-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="92e05-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92e05-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92e05-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92e05-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="92e05-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="92e05-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e05-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92e05-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e05-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92e05-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e05-129">**\_SETITEMHEIGHT lb**</span><span class="sxs-lookup"><span data-stu-id="92e05-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 





