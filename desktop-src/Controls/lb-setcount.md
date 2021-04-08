---
title: Message LB_SETCOUNT (winuser. h)
description: Définit le nombre d’éléments dans une zone de liste créée avec le \_ style NoData et non créé avec le \_ style HASSTRINGS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033145"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="70e72-104">\_Message SETCOUNT lb</span><span class="sxs-lookup"><span data-stu-id="70e72-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="70e72-105">Définit le nombre d’éléments dans une zone de liste créée avec le style [**\_ NoData**](list-box-styles.md) et non créé avec le [**style \_ HASSTRINGS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="70e72-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="70e72-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70e72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e72-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70e72-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70e72-108">Spécifie le nouveau nombre d’éléments dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="70e72-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="70e72-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="70e72-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="70e72-110">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="70e72-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="70e72-111">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="70e72-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="70e72-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70e72-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70e72-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="70e72-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e72-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70e72-114">Return value</span></span>

<span data-ttu-id="70e72-115">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="70e72-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="70e72-116">Si la mémoire est insuffisante pour stocker les éléments, la valeur de retour est LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="70e72-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e72-117">Notes</span><span class="sxs-lookup"><span data-stu-id="70e72-117">Remarks</span></span>

<span data-ttu-id="70e72-118">Le **message \_ SETCOUNT lb** est pris en charge uniquement par les zones de liste créées avec le style de [**\_ données**](list-box-styles.md) de la lbs et non créées avec le style [**\_ HASSTRINGS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="70e72-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="70e72-119">Toutes les autres zones de liste renvoient l' \_ erreur lb.</span><span class="sxs-lookup"><span data-stu-id="70e72-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e72-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70e72-120">Requirements</span></span>



| <span data-ttu-id="70e72-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70e72-121">Requirement</span></span> | <span data-ttu-id="70e72-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="70e72-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70e72-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70e72-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70e72-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70e72-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70e72-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70e72-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70e72-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70e72-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70e72-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="70e72-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e72-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70e72-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e72-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70e72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e72-130">**LB \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="70e72-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 





