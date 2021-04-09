---
title: Message LB_GETSELCOUNT (winuser. h)
description: Obtient le nombre total d’éléments sélectionnés dans une zone de liste à sélection multiple.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- LB_GETSELCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103368"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="50429-104">\_Message GETSELCOUNT lb</span><span class="sxs-lookup"><span data-stu-id="50429-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="50429-105">Obtient le nombre total d’éléments sélectionnés dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="50429-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="50429-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50429-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50429-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50429-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="50429-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50429-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50429-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50429-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="50429-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50429-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50429-111">Return value</span></span>

<span data-ttu-id="50429-112">La valeur de retour est le nombre d’éléments sélectionnés dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="50429-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="50429-113">Si la zone de liste est une zone de liste à sélection unique, la valeur de retour est LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="50429-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="50429-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50429-114">Requirements</span></span>



| <span data-ttu-id="50429-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50429-115">Requirement</span></span> | <span data-ttu-id="50429-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="50429-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50429-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50429-117">Minimum supported client</span></span><br/> | <span data-ttu-id="50429-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50429-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50429-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50429-119">Minimum supported server</span></span><br/> | <span data-ttu-id="50429-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50429-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50429-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="50429-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="50429-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50429-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50429-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50429-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50429-124">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="50429-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





