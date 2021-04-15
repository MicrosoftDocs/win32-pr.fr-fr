---
title: Message LB_GETCOUNT (winuser. h)
description: Obtient le nombre d’éléments dans une zone de liste.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466806"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="9300b-104">\_Message lb GETCOUNT</span><span class="sxs-lookup"><span data-stu-id="9300b-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="9300b-105">Obtient le nombre d’éléments dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="9300b-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9300b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9300b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9300b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9300b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9300b-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9300b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9300b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9300b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9300b-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9300b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9300b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9300b-111">Return value</span></span>

<span data-ttu-id="9300b-112">La valeur de retour est le nombre d’éléments dans la zone de liste, ou LB \_ Err si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="9300b-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="9300b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9300b-113">Remarks</span></span>

<span data-ttu-id="9300b-114">Le nombre retourné est supérieur à la valeur d’index du dernier élément (l’index est de base zéro).</span><span class="sxs-lookup"><span data-stu-id="9300b-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="9300b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9300b-115">Requirements</span></span>



| <span data-ttu-id="9300b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9300b-116">Requirement</span></span> | <span data-ttu-id="9300b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9300b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9300b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9300b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9300b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9300b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9300b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9300b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9300b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9300b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9300b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9300b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9300b-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9300b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9300b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9300b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9300b-125">**\_SETCOUNT lb**</span><span class="sxs-lookup"><span data-stu-id="9300b-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 





