---
title: Message LB_GETSEL (winuser. h)
description: Obtient l’état de sélection d’un élément.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843797"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="fb4e8-104">\_Message GETSEL lb</span><span class="sxs-lookup"><span data-stu-id="fb4e8-104">LB\_GETSEL message</span></span>

<span data-ttu-id="fb4e8-105">Obtient l’état de sélection d’un élément.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb4e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb4e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb4e8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb4e8-108">Index de base zéro de l'élément.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-108">The zero-based index of the item.</span></span>

<span data-ttu-id="fb4e8-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="fb4e8-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="fb4e8-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="fb4e8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb4e8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb4e8-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4e8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb4e8-114">Return value</span></span>

<span data-ttu-id="fb4e8-115">Si un élément est sélectionné, la valeur de retour est supérieure à zéro ; dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="fb4e8-116">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="fb4e8-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4e8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb4e8-117">Requirements</span></span>



| <span data-ttu-id="fb4e8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb4e8-118">Requirement</span></span> | <span data-ttu-id="fb4e8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb4e8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4e8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb4e8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4e8-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb4e8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb4e8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb4e8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4e8-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb4e8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb4e8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb4e8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb4e8-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb4e8-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb4e8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb4e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4e8-127">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="fb4e8-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





