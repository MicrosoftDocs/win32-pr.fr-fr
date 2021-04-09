---
title: Message TVM_SETITEMHEIGHT (commctrl. h)
description: Définit la hauteur des éléments de l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetItemHeight TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942290"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="d2b11-105">TVM \_ SETITEMHEIGHT message</span><span class="sxs-lookup"><span data-stu-id="d2b11-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="d2b11-106">Définit la hauteur des éléments de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="d2b11-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="d2b11-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .</span><span class="sxs-lookup"><span data-stu-id="d2b11-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2b11-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2b11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b11-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2b11-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b11-110">Nouvelle hauteur de chaque élément dans l’arborescence, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d2b11-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="d2b11-111">Les hauteurs inférieures à 1 seront définis sur 1.</span><span class="sxs-lookup"><span data-stu-id="d2b11-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="d2b11-112">Si cet argument n’est pas pair et que le contrôle Tree-View n’a pas le style [**TV \_ NONEVENHEIGHT**](tree-view-control-window-styles.md) , cette valeur est arrondie à la valeur paire la plus proche.</span><span class="sxs-lookup"><span data-stu-id="d2b11-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="d2b11-113">Si cet argument a la valeur-1, le contrôle revient à l’utilisation de sa hauteur d’élément par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2b11-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="d2b11-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2b11-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2b11-115">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d2b11-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b11-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2b11-116">Return value</span></span>

<span data-ttu-id="d2b11-117">Retourne la hauteur précédente des éléments, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d2b11-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2b11-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d2b11-118">Remarks</span></span>

<span data-ttu-id="d2b11-119">Le contrôle Tree-View utilise cette valeur pour la hauteur de tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="d2b11-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="d2b11-120">Pour modifier la hauteur des éléments individuels, consultez la description du membre **iIntegral** de la structure [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="d2b11-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b11-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2b11-121">Requirements</span></span>



| <span data-ttu-id="d2b11-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2b11-122">Requirement</span></span> | <span data-ttu-id="d2b11-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2b11-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b11-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2b11-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b11-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2b11-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2b11-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2b11-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b11-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2b11-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2b11-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2b11-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2b11-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b11-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b11-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2b11-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b11-131">**TVM \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="d2b11-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





