---
title: Message TVM_SETINSERTMARK (commctrl. h)
description: Définit la marque d’insertion dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetInsertMark TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843781"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="2d235-105">TVM \_ SETINSERTMARK message</span><span class="sxs-lookup"><span data-stu-id="2d235-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="2d235-106">Définit la marque d’insertion dans un contrôle TreeView.</span><span class="sxs-lookup"><span data-stu-id="2d235-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="2d235-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetInsertMark TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .</span><span class="sxs-lookup"><span data-stu-id="2d235-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d235-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d235-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d235-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d235-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d235-110">Valeur **booléenne** qui spécifie si la marque d’insertion est placée avant ou après l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d235-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="2d235-111">Si cet argument est différent de zéro, la marque d’insertion sera placée après l’élément.</span><span class="sxs-lookup"><span data-stu-id="2d235-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="2d235-112">Si cet argument est égal à zéro, la marque d’insertion sera placée avant l’élément.</span><span class="sxs-lookup"><span data-stu-id="2d235-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="2d235-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d235-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d235-114">**HTREEITEM** qui spécifie à quel élément la marque d’insertion sera placée.</span><span class="sxs-lookup"><span data-stu-id="2d235-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="2d235-115">Si cet argument a la **valeur null**, la marque d’insertion est supprimée.</span><span class="sxs-lookup"><span data-stu-id="2d235-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d235-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d235-116">Return value</span></span>

<span data-ttu-id="2d235-117">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2d235-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d235-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2d235-118">Remarks</span></span>

<span data-ttu-id="2d235-119">Dans certains cas, la marque d’insertion peut apparaître à deux emplacements après le développement d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="2d235-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="2d235-120">Si vous utilisez des marques d’insertion, il est recommandé de forcer une actualisation du contrôle après le développement d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="2d235-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d235-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d235-121">Requirements</span></span>



| <span data-ttu-id="2d235-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d235-122">Requirement</span></span> | <span data-ttu-id="2d235-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d235-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d235-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d235-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2d235-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d235-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d235-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d235-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2d235-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d235-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d235-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d235-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d235-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d235-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





