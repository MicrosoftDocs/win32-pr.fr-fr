---
title: Message TVM_SETHOT (commctrl. h)
description: Définit l’élément réactif pour un contrôle d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetHot TreeView.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942696"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="9acb2-105">TVM \_ SETHOT message</span><span class="sxs-lookup"><span data-stu-id="9acb2-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="9acb2-106">\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="9acb2-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="9acb2-107">Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9acb2-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="9acb2-108">Définit l’élément réactif pour un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="9acb2-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="9acb2-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetHot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .</span><span class="sxs-lookup"><span data-stu-id="9acb2-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9acb2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9acb2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9acb2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9acb2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9acb2-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9acb2-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9acb2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9acb2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9acb2-114">Handle vers le nouvel élément réactif.</span><span class="sxs-lookup"><span data-stu-id="9acb2-114">Handle to the new hot item.</span></span> <span data-ttu-id="9acb2-115">Si cette valeur est **null**, le contrôle Tree-View est défini sur ne pas avoir d’élément réactif.</span><span class="sxs-lookup"><span data-stu-id="9acb2-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9acb2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9acb2-116">Return value</span></span>

<span data-ttu-id="9acb2-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9acb2-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="9acb2-118">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="9acb2-118">Security Considerations</span></span>

<span data-ttu-id="9acb2-119">L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="9acb2-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="9acb2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="9acb2-120">Remarks</span></span>

<span data-ttu-id="9acb2-121">L' *élément réactif* est l’élément sur lequel pointe la souris.</span><span class="sxs-lookup"><span data-stu-id="9acb2-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="9acb2-122">Ce message se présente comme s’il s’agissait de l’élément réactif, même si la souris n’est pas positionnée dessus.</span><span class="sxs-lookup"><span data-stu-id="9acb2-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="9acb2-123">Ce message n’a aucun effet visible si le style [**TV \_ TRACKSELECT**](tree-view-control-window-styles.md) n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9acb2-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="9acb2-124">Si elle est réussie, ce message entraîne le redessin de l’élément réactif.</span><span class="sxs-lookup"><span data-stu-id="9acb2-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="9acb2-125">Ce message est ignoré si *lParam* a la **valeur null** et que le contrôle Tree-View effectue le suivi de la souris.</span><span class="sxs-lookup"><span data-stu-id="9acb2-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="9acb2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9acb2-126">Requirements</span></span>



| <span data-ttu-id="9acb2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9acb2-127">Requirement</span></span> | <span data-ttu-id="9acb2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9acb2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9acb2-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9acb2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9acb2-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9acb2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9acb2-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9acb2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9acb2-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9acb2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9acb2-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9acb2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9acb2-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9acb2-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9acb2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9acb2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9acb2-136">**\_SetHot TreeView**</span><span class="sxs-lookup"><span data-stu-id="9acb2-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





