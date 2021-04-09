---
title: Message TVM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843289"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="9d3ee-105">TVM- \_ message INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="9d3ee-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="9d3ee-106">Insère un nouvel élément dans un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="9d3ee-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="9d3ee-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d3ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d3ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3ee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d3ee-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9d3ee-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9d3ee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d3ee-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ee-112">Pointeur vers une structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) qui spécifie les attributs de l’élément d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d3ee-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d3ee-113">Return value</span></span>

<span data-ttu-id="9d3ee-114">Retourne le handle **HTREEITEM** au nouvel élément en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9d3ee-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d3ee-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d3ee-115">Requirements</span></span>



| <span data-ttu-id="9d3ee-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d3ee-116">Requirement</span></span> | <span data-ttu-id="9d3ee-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d3ee-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3ee-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d3ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d3ee-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d3ee-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d3ee-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d3ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d3ee-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d3ee-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d3ee-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d3ee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d3ee-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ee-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9d3ee-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9d3ee-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d3ee-125">**TVM \_ INSERTITEMW** (Unicode) et **TVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9d3ee-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9d3ee-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d3ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3ee-127">TVN \_ ENDLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="9d3ee-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





