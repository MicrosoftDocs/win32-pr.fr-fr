---
title: Message TVM_GETCOUNT (commctrl. h)
description: Récupère le nombre d’éléments dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView GetCount.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466483"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="3445d-105">TVM \_ GETCOUNT (message)</span><span class="sxs-lookup"><span data-stu-id="3445d-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="3445d-106">Récupère le nombre d’éléments dans un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="3445d-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="3445d-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .</span><span class="sxs-lookup"><span data-stu-id="3445d-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3445d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3445d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3445d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3445d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3445d-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3445d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3445d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3445d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3445d-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3445d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3445d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3445d-113">Return value</span></span>

<span data-ttu-id="3445d-114">Retourne le nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="3445d-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="3445d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3445d-115">Remarks</span></span>

<span data-ttu-id="3445d-116">Le nombre de nœuds retourné par [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) est limité aux valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="3445d-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="3445d-117">Si vous ajoutez un nœud au-delà de 32767, la macro retourne une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="3445d-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="3445d-118">Après l’ajout de nœuds 65536, le nombre retourne à zéro.</span><span class="sxs-lookup"><span data-stu-id="3445d-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="3445d-119">Dans ce cas, le contrôle Tree-View apparaît vide sans barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="3445d-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="3445d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3445d-120">Requirements</span></span>



| <span data-ttu-id="3445d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3445d-121">Requirement</span></span> | <span data-ttu-id="3445d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3445d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3445d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3445d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3445d-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3445d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3445d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3445d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3445d-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3445d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3445d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3445d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3445d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3445d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





