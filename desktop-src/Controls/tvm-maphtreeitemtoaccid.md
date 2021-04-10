---
title: Message TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Mappe un HTREEITEM à un ID d’accessibilité.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103720"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="6bd33-104">TVM \_ MAPHTREEITEMTOACCID message</span><span class="sxs-lookup"><span data-stu-id="6bd33-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="6bd33-105">Mappe un **HTREEITEM** à un ID d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6bd33-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bd33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bd33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd33-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6bd33-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6bd33-108">**HTREEITEM** mappé à un ID d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6bd33-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="6bd33-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bd33-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6bd33-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6bd33-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bd33-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6bd33-111">Return value</span></span>

<span data-ttu-id="6bd33-112">Retourne un ID d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="6bd33-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bd33-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6bd33-113">Remarks</span></span>

<span data-ttu-id="6bd33-114">Lorsque vous ajoutez un élément à un contrôle Tree-View, un descripteur **HTREEITEM** qui identifie de façon unique l’élément est retourné.</span><span class="sxs-lookup"><span data-stu-id="6bd33-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="6bd33-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="6bd33-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6bd33-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6bd33-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6bd33-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bd33-117">Requirements</span></span>



| <span data-ttu-id="6bd33-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bd33-118">Requirement</span></span> | <span data-ttu-id="6bd33-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bd33-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd33-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bd33-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd33-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bd33-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6bd33-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bd33-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd33-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bd33-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bd33-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bd33-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bd33-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bd33-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd33-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bd33-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd33-127">**\_MapHTREEITEMtoAccID TreeView**</span><span class="sxs-lookup"><span data-stu-id="6bd33-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





