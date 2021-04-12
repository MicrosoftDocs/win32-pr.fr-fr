---
title: Message TVM_SETITEM (commctrl. h)
description: Le \_ message TVM SETITEM définit une partie ou la totalité des attributs d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetItem TreeView.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465463"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="9d5fb-105">TVM \_ SETITEM message</span><span class="sxs-lookup"><span data-stu-id="9d5fb-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="9d5fb-106">Le message **TVM \_ SETITEM** définit une partie ou la totalité des attributs d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="9d5fb-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="9d5fb-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d5fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d5fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d5fb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5fb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9d5fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d5fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5fb-112">Pointeur vers une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient les nouveaux attributs d’élément.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="9d5fb-113">Avec la [version 4,71](common-control-versions.md) et les versions ultérieures, vous pouvez utiliser une structure [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) à la place.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5fb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d5fb-114">Return value</span></span>

<span data-ttu-id="9d5fb-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5fb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9d5fb-116">Remarks</span></span>

<span data-ttu-id="9d5fb-117">Le membre **hitem** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifie l’élément et le membre **Mask** spécifie les attributs à définir.</span><span class="sxs-lookup"><span data-stu-id="9d5fb-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5fb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d5fb-118">Requirements</span></span>



| <span data-ttu-id="9d5fb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d5fb-119">Requirement</span></span> | <span data-ttu-id="9d5fb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d5fb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5fb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5fb-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d5fb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d5fb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5fb-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d5fb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d5fb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d5fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5fb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5fb-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9d5fb-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9d5fb-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d5fb-128">**TVM \_ SETITEMW** (Unicode) et **TVM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d5fb-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





