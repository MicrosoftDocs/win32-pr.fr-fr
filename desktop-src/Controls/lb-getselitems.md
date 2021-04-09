---
title: Message LB_GETSELITEMS (winuser. h)
description: Remplit une mémoire tampon avec un tableau d’entiers qui spécifient les numéros d’élément des éléments sélectionnés dans une zone de liste à sélection multiple.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942202"
---
# <a name="lb_getselitems-message"></a><span data-ttu-id="3c2af-104">\_Message GETSELITEMS lb</span><span class="sxs-lookup"><span data-stu-id="3c2af-104">LB\_GETSELITEMS message</span></span>

<span data-ttu-id="3c2af-105">Remplit une mémoire tampon avec un tableau d’entiers qui spécifient les numéros d’élément des éléments sélectionnés dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="3c2af-105">Fills a buffer with an array of integers that specify the item numbers of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c2af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c2af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2af-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c2af-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c2af-108">Nombre maximal d’éléments sélectionnés dont les numéros d’élément doivent être placés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3c2af-108">The maximum number of selected items whose item numbers are to be placed in the buffer.</span></span>

<span data-ttu-id="3c2af-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3c2af-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="3c2af-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="3c2af-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="3c2af-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="3c2af-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="3c2af-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c2af-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c2af-113">Pointeur vers une mémoire tampon suffisamment grand pour le nombre d’entiers spécifiés par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3c2af-113">A pointer to a buffer large enough for the number of integers specified by the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2af-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c2af-114">Return value</span></span>

<span data-ttu-id="3c2af-115">La valeur de retour est le nombre d’éléments placés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3c2af-115">The return value is the number of items placed in the buffer.</span></span> <span data-ttu-id="3c2af-116">Si la zone de liste est une zone de liste à sélection unique, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3c2af-116">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2af-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c2af-117">Requirements</span></span>



| <span data-ttu-id="3c2af-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c2af-118">Requirement</span></span> | <span data-ttu-id="3c2af-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c2af-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2af-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c2af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2af-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c2af-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c2af-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c2af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2af-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c2af-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c2af-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c2af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2af-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2af-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2af-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c2af-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2af-127">**\_GETSELCOUNT lb**</span><span class="sxs-lookup"><span data-stu-id="3c2af-127">**LB\_GETSELCOUNT**</span></span>](lb-getselcount.md)
</dt> </dl>

 

 





