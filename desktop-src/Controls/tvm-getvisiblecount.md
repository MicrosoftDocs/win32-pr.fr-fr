---
title: Message TVM_GETVISIBLECOUNT (commctrl. h)
description: Obtient le nombre d’éléments qui peuvent être complètement visibles dans la fenêtre cliente d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetVisibleCount TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941839"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="8c81a-105">TVM \_ GETVISIBLECOUNT message</span><span class="sxs-lookup"><span data-stu-id="8c81a-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="8c81a-106">Obtient le nombre d’éléments qui peuvent être complètement visibles dans la fenêtre cliente d’un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="8c81a-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="8c81a-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetVisibleCount TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .</span><span class="sxs-lookup"><span data-stu-id="8c81a-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c81a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c81a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c81a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c81a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8c81a-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8c81a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8c81a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c81a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8c81a-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8c81a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c81a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c81a-113">Return value</span></span>

<span data-ttu-id="8c81a-114">Retourne le nombre d’éléments qui peuvent être complètement visibles dans la fenêtre cliente du contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="8c81a-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c81a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8c81a-115">Remarks</span></span>

<span data-ttu-id="8c81a-116">Le nombre d’éléments pouvant être entièrement visibles peut être supérieur au nombre d’éléments dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8c81a-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="8c81a-117">Le contrôle calcule cette valeur en divisant la hauteur de la fenêtre client par la hauteur d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8c81a-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="8c81a-118">Notez que la valeur de retour est le nombre d’éléments qui peuvent être *entièrement* visibles.</span><span class="sxs-lookup"><span data-stu-id="8c81a-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="8c81a-119">Si vous pouvez voir tous les 20 éléments et une partie d’un autre élément, la valeur de retour est 20.</span><span class="sxs-lookup"><span data-stu-id="8c81a-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c81a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c81a-120">Requirements</span></span>



| <span data-ttu-id="8c81a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c81a-121">Requirement</span></span> | <span data-ttu-id="8c81a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c81a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c81a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c81a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c81a-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c81a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c81a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c81a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c81a-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c81a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c81a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c81a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c81a-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c81a-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





