---
description: Modifie le type de confirmation, qui contrôle ce que l’objet IInkAnalyzer peut modifier à propos du IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'IContextNode :: Confirm, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519314"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="da7f5-103">IContextNode :: Confirm, méthode</span><span class="sxs-lookup"><span data-stu-id="da7f5-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="da7f5-104">Modifie le type de confirmation, qui contrôle ce que l’objet [**IInkAnalyzer**](iinkanalyzer.md) peut modifier à propos du [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="da7f5-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da7f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da7f5-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="da7f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da7f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da7f5-107">*confirmedType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da7f5-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da7f5-108">[**ConfirmationType**](confirmationtype.md) appliqué au nœud.</span><span class="sxs-lookup"><span data-stu-id="da7f5-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da7f5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da7f5-109">Return value</span></span>

<span data-ttu-id="da7f5-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="da7f5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da7f5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="da7f5-111">Remarks</span></span>

<span data-ttu-id="da7f5-112">Utilisez cette méthode pour permettre à l’utilisateur final de confirmer que le [**IInkAnalyzer**](iinkanalyzer.md) a correctement analysé les traits.</span><span class="sxs-lookup"><span data-stu-id="da7f5-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="da7f5-113">Après l’appel de **IContextNode :: Confirm** , le **IInkAnalyzer** ne modifie pas les objets [**IContextNode**](icontextnode.md) pour ces traits lors de l’analyse ultérieure.</span><span class="sxs-lookup"><span data-stu-id="da7f5-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="da7f5-114">Utilisez **IContextNode :: Confirm** lorsque l’utilisateur a confirmé les résultats de l’analyse et ne veut pas que le [**IInkAnalyzer**](iinkanalyzer.md) change un [**IContextNode**](icontextnode.md) lors de l’analyse ultérieure.</span><span class="sxs-lookup"><span data-stu-id="da7f5-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="da7f5-115">Par exemple, si l’utilisateur écrit le mot « vers », puis que l’application appelle la [**méthode IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md), l’analyseur d’encre génère un nœud InkWord avec la valeur « to ».</span><span class="sxs-lookup"><span data-stu-id="da7f5-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="da7f5-116">Si l’utilisateur ajoute ensuite « me » après « to » comme un seul mot et que l’application appelle de nouveau la **méthode IInkAnalyzer :: Analyze** , l’analyseur d’encre peut supprimer le nœud InkWord précédent et créer un nouveau nœud InkWord avec la valeur « tome ».</span><span class="sxs-lookup"><span data-stu-id="da7f5-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="da7f5-117">Toutefois, si, après le premier appel à la **méthode IInkAnalyzer :: Analyze**, l’application appelle **IContextNode :: Confirm** sur le nœud InkWord pour « to » avec la valeur [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, avant que l’utilisateur n’ajoute le « me », quand l’application appelle la **méthode IInkAnalyzer :: Analyze**, l’analyseur d’encre ne supprime pas ou ne modifie pas le nœud « to ».</span><span class="sxs-lookup"><span data-stu-id="da7f5-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="da7f5-118">À la place, l’analyseur d’encre peut reconnaître deux nœuds InkWord pour « to » et « me ».</span><span class="sxs-lookup"><span data-stu-id="da7f5-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="da7f5-119">[**IContextNode**](icontextnode.md) peut uniquement confirmer les objets de type InkWord et InkDrawing (consultez [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="da7f5-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="da7f5-120">**IContextNode :: Confirm** retourne **E \_ INVALIDARG** lorsque le nœud n’est pas un nœud terminal.</span><span class="sxs-lookup"><span data-stu-id="da7f5-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="da7f5-121">Les méthodes [**IInkAnalyzer :: RemoveStroke**](iinkanalyzer-removestroke.md) et [**IInkAnalyzer :: RemoveStrokes**](iinkanalyzer-removestrokes.md) déconfirment les nœuds à partir desquels ils suppriment les données de trait.</span><span class="sxs-lookup"><span data-stu-id="da7f5-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="da7f5-122">[**IContextNode :: SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md)et [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) retournent le biais du **Core \_ E \_ INVALIDOPERATION** si l’objet [**IContextNode**](icontextnode.md) est déjà confirmé.</span><span class="sxs-lookup"><span data-stu-id="da7f5-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="da7f5-123">[**IContextNode :: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) retourne une erreur si le nœud source ou de destination est confirmé.</span><span class="sxs-lookup"><span data-stu-id="da7f5-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="da7f5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da7f5-124">Requirements</span></span>



| <span data-ttu-id="da7f5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da7f5-125">Requirement</span></span> | <span data-ttu-id="da7f5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="da7f5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da7f5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da7f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="da7f5-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da7f5-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="da7f5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da7f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="da7f5-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="da7f5-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="da7f5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="da7f5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="da7f5-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="da7f5-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da7f5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="da7f5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da7f5-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da7f5-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="da7f5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da7f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da7f5-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="da7f5-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="da7f5-137">**IContextNode::IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="da7f5-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="da7f5-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="da7f5-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




