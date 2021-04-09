---
title: Message CB_GETDROPPEDSTATE (winuser. h)
description: Détermine si la zone de liste d’une zone de liste déroulante est déroulée.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033274"
---
# <a name="cb_getdroppedstate-message"></a><span data-ttu-id="7c4e6-104">\_Message GETDROPPEDSTATE CB</span><span class="sxs-lookup"><span data-stu-id="7c4e6-104">CB\_GETDROPPEDSTATE message</span></span>

<span data-ttu-id="7c4e6-105">Détermine si la zone de liste d’une zone de liste déroulante est déroulée.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-105">Determines whether the list box of a combo box is dropped down.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c4e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c4e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4e6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c4e6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4e6-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c4e6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c4e6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4e6-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c4e6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c4e6-111">Return value</span></span>

<span data-ttu-id="7c4e6-112">Si la zone de liste est visible, la valeur de retour est **true**; Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="7c4e6-112">If the list box is visible, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4e6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c4e6-113">Requirements</span></span>



| <span data-ttu-id="7c4e6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c4e6-114">Requirement</span></span> | <span data-ttu-id="7c4e6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c4e6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4e6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c4e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4e6-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c4e6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c4e6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c4e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4e6-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c4e6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c4e6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c4e6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4e6-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c4e6-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4e6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c4e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4e6-123">**\_SHOWDROPDOWN CB**</span><span class="sxs-lookup"><span data-stu-id="7c4e6-123">**CB\_SHOWDROPDOWN**</span></span>](cb-showdropdown.md)
</dt> </dl>

 

 





