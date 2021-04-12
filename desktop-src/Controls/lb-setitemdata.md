---
title: Message LB_SETITEMDATA (winuser. h)
description: Définit une valeur associée à l’élément spécifié dans une zone de liste.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- LB_SETITEMDATA les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105532"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="3c90b-104">\_Message SETITEMDATA lb</span><span class="sxs-lookup"><span data-stu-id="3c90b-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="3c90b-105">Définit une valeur associée à l’élément spécifié dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="3c90b-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c90b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c90b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c90b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c90b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c90b-108">Spécifie l’index de base zéro de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3c90b-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="3c90b-109">Si cette valeur est-1, la valeur *lParam* s’applique à tous les éléments de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="3c90b-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="3c90b-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3c90b-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="3c90b-111">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="3c90b-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="3c90b-112">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="3c90b-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="3c90b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c90b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c90b-114">Spécifie la valeur à associer à l’élément.</span><span class="sxs-lookup"><span data-stu-id="3c90b-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c90b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c90b-115">Return value</span></span>

<span data-ttu-id="3c90b-116">Si une erreur se produit, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3c90b-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c90b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3c90b-117">Remarks</span></span>

<span data-ttu-id="3c90b-118">Si l’élément se trouve dans une zone de liste owner-drawn créée sans le style [**\_ HASSTRINGS**](list-box-styles.md) , ce message remplace la valeur contenue dans le paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) qui a ajouté l’élément à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="3c90b-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c90b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c90b-119">Requirements</span></span>



| <span data-ttu-id="3c90b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c90b-120">Requirement</span></span> | <span data-ttu-id="3c90b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c90b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c90b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c90b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3c90b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c90b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c90b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c90b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3c90b-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c90b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c90b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c90b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c90b-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c90b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c90b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c90b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c90b-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3c90b-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c90b-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="3c90b-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="3c90b-131">**\_GETITEMDATA lb**</span><span class="sxs-lookup"><span data-stu-id="3c90b-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="3c90b-132">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="3c90b-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





