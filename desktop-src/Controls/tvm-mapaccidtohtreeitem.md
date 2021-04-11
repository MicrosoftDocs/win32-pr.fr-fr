---
title: Message TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Mappe un ID d’accessibilité à un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032598"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="a8e0b-104">TVM \_ MAPACCIDTOHTREEITEM message</span><span class="sxs-lookup"><span data-stu-id="a8e0b-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="a8e0b-105">Mappe un ID d’accessibilité à un **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="a8e0b-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8e0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8e0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e0b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8e0b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a8e0b-108">**Uint** qui contient l’ID d’accessibilité à mapper à un **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="a8e0b-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="a8e0b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8e0b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a8e0b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a8e0b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e0b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8e0b-111">Return value</span></span>

<span data-ttu-id="a8e0b-112">Retourne le **HTREEITEM** auquel l’ID d’accessibilité spécifié est mappé.</span><span class="sxs-lookup"><span data-stu-id="a8e0b-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e0b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a8e0b-113">Remarks</span></span>

<span data-ttu-id="a8e0b-114">Lorsque vous ajoutez un élément à un contrôle Tree-View, un **HTREEITEM** retourne, qui identifie de façon unique l’élément.</span><span class="sxs-lookup"><span data-stu-id="a8e0b-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="a8e0b-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="a8e0b-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a8e0b-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a8e0b-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8e0b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8e0b-117">Requirements</span></span>



| <span data-ttu-id="a8e0b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8e0b-118">Requirement</span></span> | <span data-ttu-id="a8e0b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8e0b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e0b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8e0b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e0b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8e0b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8e0b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8e0b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e0b-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8e0b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8e0b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8e0b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e0b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e0b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e0b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8e0b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e0b-127">**\_MapAccIDToHTREEITEM TreeView**</span><span class="sxs-lookup"><span data-stu-id="a8e0b-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





