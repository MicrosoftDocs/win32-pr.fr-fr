---
description: Spécifie le type de confirmation qui peut se produire sur un objet IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Énumération ConfirmationType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514380"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="bd9e6-103">Énumération ConfirmationType</span><span class="sxs-lookup"><span data-stu-id="bd9e6-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="bd9e6-104">Spécifie le type de confirmation qui peut se produire sur un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="bd9e6-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd9e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd9e6-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="bd9e6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bd9e6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bd9e6-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="bd9e6-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="bd9e6-108">Aucune confirmation n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-108">No confirmation is applied.</span></span> <span data-ttu-id="bd9e6-109">Le [**IInkAnalyzer**](iinkanalyzer.md) est libre de modifier un nœud de contexte ou l’un de ses descendants si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="bd9e6-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**</span><span class="sxs-lookup"><span data-stu-id="bd9e6-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="bd9e6-111">Le [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas modifier le type ou les propriétés du nœud de contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="bd9e6-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType- \_ boundic**</span><span class="sxs-lookup"><span data-stu-id="bd9e6-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="bd9e6-113">Le [**IInkAnalyzer**](iinkanalyzer.md) n’effectue pas d’opérations, y compris l’ajout d’encre ou la fusion avec d’autres [**ContextNodes**](icontextnodes.md), qui entraînent le déplacement de la limite supérieure au-delà de la limite supérieure actuelle.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="bd9e6-114">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="bd9e6-114">For example:</span></span>

-   <span data-ttu-id="bd9e6-115">Une application analyse un jeu d’encre et un ParagraphNode est identifié.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="bd9e6-116">L’application confirme la limite de la limite de ce paragraphe.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="bd9e6-117">L’utilisateur de l’application écrit une nouvelle encre au-dessus du paragraphe actuel.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="bd9e6-118">Lorsque l’analyse est à nouveau appelée, la nouvelle encre n’est pas incorporée dans le nœud de paragraphe confirmé.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="bd9e6-119">Étant donné que seule la limite supérieure est confirmée, le ContextNode peut continuer à croître dans d’autres directions.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="bd9e6-120">La suppression des traits peut entraîner le déplacement de la limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="bd9e6-121">La traduction du ContextNode peut entraîner la modification de l’emplacement, mais n’autorisera pas la fusion de l’encre supplémentaire dans le nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="bd9e6-122">Ce ConfirmationType s’applique uniquement aux nœuds de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="bd9e6-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd9e6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bd9e6-123">Remarks</span></span>

<span data-ttu-id="bd9e6-124">Vous pouvez utiliser la valeur **NodeTypeAndProperties** uniquement pour les nœuds Word et Ink Drawing (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="bd9e6-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="bd9e6-125">Dans le cas contraire, un **E \_ INVALIDARG** est retourné à partir de [**IContextNode :: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="bd9e6-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd9e6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd9e6-126">Requirements</span></span>



| <span data-ttu-id="bd9e6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd9e6-127">Requirement</span></span> | <span data-ttu-id="bd9e6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd9e6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9e6-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd9e6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bd9e6-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd9e6-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd9e6-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd9e6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bd9e6-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd9e6-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bd9e6-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd9e6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd9e6-134"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bd9e6-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd9e6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd9e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd9e6-136">**IContextNode :: Confirm**</span><span class="sxs-lookup"><span data-stu-id="bd9e6-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="bd9e6-137">**IContextNode::IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="bd9e6-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




