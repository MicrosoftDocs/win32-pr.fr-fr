---
description: Représente une relation entre deux objets IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interface IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514448"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="105b7-103">Interface IContextLink</span><span class="sxs-lookup"><span data-stu-id="105b7-103">IContextLink interface</span></span>

<span data-ttu-id="105b7-104">Représente une relation entre deux objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="105b7-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="105b7-105">Membres</span><span class="sxs-lookup"><span data-stu-id="105b7-105">Members</span></span>

<span data-ttu-id="105b7-106">L’interface **IContextLink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="105b7-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="105b7-107">**IContextLink** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="105b7-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="105b7-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="105b7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="105b7-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="105b7-109">Methods</span></span>

<span data-ttu-id="105b7-110">L’interface **IContextLink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="105b7-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="105b7-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="105b7-111">Method</span></span>                                                                  | <span data-ttu-id="105b7-112">Description</span><span class="sxs-lookup"><span data-stu-id="105b7-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="105b7-113">**GetContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="105b7-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="105b7-114">Récupère le type de relation représenté par ce **IContextLink** .</span><span class="sxs-lookup"><span data-stu-id="105b7-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="105b7-115">**GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="105b7-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="105b7-116">Récupère l’objet [**IContextNode**](icontextnode.md) qui est la destination de ce **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="105b7-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="105b7-117">**GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="105b7-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="105b7-118">Récupère l’objet [**IContextNode**](icontextnode.md) qui est la source de ce **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="105b7-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="105b7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="105b7-119">Remarks</span></span>

<span data-ttu-id="105b7-120">Voici un exemple de relation représentée par un objet **IContextLink** :</span><span class="sxs-lookup"><span data-stu-id="105b7-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="105b7-121">Lorsqu’un nœud AnalysisHint est utilisé dans l’analyse de l’encre, l’opération d’analyse de l’encre crée un objet **IContextLink** de type AnalysisHint entre le nœud de l’indicateur d’analyse et le nœud qui contient l’écriture dans la zone de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="105b7-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="105b7-122">Le nœud source est le nœud d’indicateur d’analyse et le nœud de destination est le nœud qui contient l’écriture.</span><span class="sxs-lookup"><span data-stu-id="105b7-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="105b7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="105b7-123">Requirements</span></span>



| <span data-ttu-id="105b7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="105b7-124">Requirement</span></span> | <span data-ttu-id="105b7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="105b7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="105b7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="105b7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="105b7-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="105b7-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="105b7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="105b7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="105b7-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="105b7-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="105b7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="105b7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="105b7-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="105b7-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="105b7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="105b7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="105b7-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="105b7-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="105b7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="105b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105b7-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="105b7-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="105b7-136">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="105b7-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="105b7-137">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="105b7-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="105b7-138">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="105b7-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

