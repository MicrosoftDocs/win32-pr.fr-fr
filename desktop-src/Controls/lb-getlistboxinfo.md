---
title: Message LB_GETLISTBOXINFO (winuser. h)
description: Obtient le nombre d’éléments par colonne dans une zone de liste spécifiée.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- LB_GETLISTBOXINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032757"
---
# <a name="lb_getlistboxinfo-message"></a><span data-ttu-id="51717-104">\_Message GETLISTBOXINFO lb</span><span class="sxs-lookup"><span data-stu-id="51717-104">LB\_GETLISTBOXINFO message</span></span>

<span data-ttu-id="51717-105">Obtient le nombre d’éléments par colonne dans une zone de liste spécifiée.</span><span class="sxs-lookup"><span data-stu-id="51717-105">Gets the number of items per column in a specified list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="51717-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51717-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51717-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="51717-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51717-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51717-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="51717-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51717-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51717-111">Return value</span></span>

<span data-ttu-id="51717-112">La valeur de retour est le nombre d’éléments par colonne.</span><span class="sxs-lookup"><span data-stu-id="51717-112">The return value is the number of items per column.</span></span>

## <a name="remarks"></a><span data-ttu-id="51717-113">Notes</span><span class="sxs-lookup"><span data-stu-id="51717-113">Remarks</span></span>

<span data-ttu-id="51717-114">Ce message est équivalent à [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span><span class="sxs-lookup"><span data-stu-id="51717-114">This message is equivalent to [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="51717-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51717-115">Requirements</span></span>



| <span data-ttu-id="51717-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51717-116">Requirement</span></span> | <span data-ttu-id="51717-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="51717-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51717-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51717-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51717-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51717-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51717-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51717-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51717-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51717-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51717-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="51717-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51717-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51717-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51717-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51717-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51717-125">**GetListBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="51717-125">**GetListBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





