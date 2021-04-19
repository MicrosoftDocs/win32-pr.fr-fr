---
description: Déplace les données de trait de ce IContextNode vers le IContextNode spécifié.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'IContextNode :: ReparentStrokeByIdToNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542902"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="f2b51-103">IContextNode :: ReparentStrokeByIdToNode, méthode</span><span class="sxs-lookup"><span data-stu-id="f2b51-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="f2b51-104">Déplace les données de trait de ce [**IContextNode**](icontextnode.md) vers le **IContextNode** spécifié.</span><span class="sxs-lookup"><span data-stu-id="f2b51-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2b51-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="f2b51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2b51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b51-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2b51-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b51-108">Identificateur du trait à déplacer.</span><span class="sxs-lookup"><span data-stu-id="f2b51-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="f2b51-109">*pContextNodeDestination* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2b51-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b51-110">Objet [**IContextNode**](icontextnode.md) vers lequel déplacer les données de trait.</span><span class="sxs-lookup"><span data-stu-id="f2b51-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b51-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2b51-111">Return value</span></span>

<span data-ttu-id="f2b51-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f2b51-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b51-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f2b51-113">Remarks</span></span>

<span data-ttu-id="f2b51-114">L’objet [**IContextNode**](icontextnode.md) spécifié doit être l’un des types suivants des constantes de [type de nœud de contexte](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** ou **UnclassifiedInk**.</span><span class="sxs-lookup"><span data-stu-id="f2b51-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="f2b51-115">Si vous tentez de déplacer un trait vers tout autre type d’objet **IContextNode** , la valeur de retour **E \_ INVALIDARG** est retournée.</span><span class="sxs-lookup"><span data-stu-id="f2b51-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="f2b51-116">Cette méthode peut être appelée à partir de n’importe quel objet [**IContextNode**](icontextnode.md) , y compris les objets **IContextNode** terminaux non-Ink.</span><span class="sxs-lookup"><span data-stu-id="f2b51-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="f2b51-117">Le trait spécifié doit être référencé par l’un des descendants de cet objet **IContextNode** ou **E \_ INVALIDARG** est retourné.</span><span class="sxs-lookup"><span data-stu-id="f2b51-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="f2b51-118">Si ce [**IContextNode**](icontextnode.md) ou **IContextNode** dans *pContextNodeDestination* est confirmé, **E \_ INVALIDARG** est retourné (voir [**IContextNode :: IsConfirmed**](icontextnode-isconfirmed.md)).</span><span class="sxs-lookup"><span data-stu-id="f2b51-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="f2b51-119">L’analyseur d’encre ne supprime pas les nœuds de contexte vides de l’arborescence des résultats en réponse à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f2b51-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="f2b51-120">Un nœud terminal d’encre qui ne fait pas référence à des données de trait est un nœud vide.</span><span class="sxs-lookup"><span data-stu-id="f2b51-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="f2b51-121">Un nœud conteneur qui ne fait pas référence à un nœud enfant est un nœud vide.</span><span class="sxs-lookup"><span data-stu-id="f2b51-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="f2b51-122">Un nœud vide génère des erreurs s’il se trouve dans l’arborescence pendant une opération d’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f2b51-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="f2b51-123">Pour supprimer un nœud de l’arborescence de l’analyseur d’encre, appelez la méthode [**IContextNode ::D eletesubnode**](icontextnode-deletesubnode.md) du nœud parent (voir [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md)).</span><span class="sxs-lookup"><span data-stu-id="f2b51-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b51-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2b51-124">Requirements</span></span>



| <span data-ttu-id="f2b51-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2b51-125">Requirement</span></span> | <span data-ttu-id="f2b51-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2b51-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b51-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b51-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b51-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2b51-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f2b51-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b51-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b51-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2b51-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f2b51-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2b51-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b51-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f2b51-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f2b51-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f2b51-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2b51-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2b51-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f2b51-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2b51-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b51-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f2b51-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f2b51-137">**IContextNode::SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="f2b51-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="f2b51-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="f2b51-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




