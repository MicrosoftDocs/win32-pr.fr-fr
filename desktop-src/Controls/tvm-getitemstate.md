---
title: Message TVM_GETITEMSTATE (commctrl. h)
description: Récupère tout ou partie des attributs d’état d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetItemState TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033040"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="8a7ec-105">TVM \_ GETITEMSTATE message</span><span class="sxs-lookup"><span data-stu-id="8a7ec-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="8a7ec-106">Récupère tout ou partie des attributs d’état d’un élément d’affichage d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="8a7ec-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="8a7ec-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetItemState TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="8a7ec-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a7ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a7ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a7ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a7ec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a7ec-110">Handle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8a7ec-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="8a7ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a7ec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a7ec-112">Masque utilisé pour spécifier les États à interroger.</span><span class="sxs-lookup"><span data-stu-id="8a7ec-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="8a7ec-113">Elle est équivalente au membre **stateMask** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="8a7ec-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a7ec-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a7ec-114">Return value</span></span>

<span data-ttu-id="8a7ec-115">Retourne une valeur **uint** avec les bits d’État appropriés ayant la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="8a7ec-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="8a7ec-116">Seuls les bits qui sont spécifiés par *lParam* et qui ont la **valeur true** seront définis.</span><span class="sxs-lookup"><span data-stu-id="8a7ec-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="8a7ec-117">Cette valeur est équivalente au membre d' **État** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="8a7ec-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7ec-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a7ec-118">Requirements</span></span>



| <span data-ttu-id="8a7ec-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a7ec-119">Requirement</span></span> | <span data-ttu-id="8a7ec-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a7ec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7ec-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a7ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7ec-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a7ec-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a7ec-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a7ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7ec-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a7ec-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a7ec-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a7ec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a7ec-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a7ec-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





