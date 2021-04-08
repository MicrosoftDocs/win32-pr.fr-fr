---
title: Message TVM_GETITEMHEIGHT (commctrl. h)
description: Récupère la hauteur actuelle de chaque élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetItemHeight TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844434"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="2884c-105">TVM \_ GETITEMHEIGHT message</span><span class="sxs-lookup"><span data-stu-id="2884c-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="2884c-106">Récupère la hauteur actuelle de chaque élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="2884c-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="2884c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .</span><span class="sxs-lookup"><span data-stu-id="2884c-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2884c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2884c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2884c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2884c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2884c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2884c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2884c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2884c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2884c-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2884c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2884c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2884c-113">Return value</span></span>

<span data-ttu-id="2884c-114">Retourne la hauteur de chaque élément, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2884c-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="2884c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2884c-115">Requirements</span></span>



| <span data-ttu-id="2884c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2884c-116">Requirement</span></span> | <span data-ttu-id="2884c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2884c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2884c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2884c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2884c-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2884c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2884c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2884c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2884c-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2884c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2884c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2884c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2884c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2884c-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2884c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2884c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2884c-125">**TVM \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="2884c-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





