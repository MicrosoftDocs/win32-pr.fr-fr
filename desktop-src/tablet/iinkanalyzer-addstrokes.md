---
description: Ajoute des données de trait pour plusieurs traits à IInkAnalyzer et assigne l’identificateur de culture du thread d’entrée actif aux traits.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'IInkAnalyzer :: AddStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516268"
---
# <a name="iinkanalyzeraddstrokes-method"></a><span data-ttu-id="512fa-103">IInkAnalyzer :: AddStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="512fa-103">IInkAnalyzer::AddStrokes method</span></span>

<span data-ttu-id="512fa-104">Ajoute des données de trait pour plusieurs traits à [**IInkAnalyzer**](iinkanalyzer.md) et assigne l’identificateur de culture du thread d’entrée actif aux traits.</span><span class="sxs-lookup"><span data-stu-id="512fa-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="512fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="512fa-105">Syntax</span></span>


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="512fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="512fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="512fa-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="512fa-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-108">Nombre de traits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="512fa-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="512fa-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="512fa-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-110">Tableau contenant les identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="512fa-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="512fa-111">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="512fa-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-112">Nombre de propriétés dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="512fa-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="512fa-113">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="512fa-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-114">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="512fa-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="512fa-115">*pulPacketDataCountPerStroke* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="512fa-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-116">Tableau contenant le nombre de paquets dans chaque trait.</span><span class="sxs-lookup"><span data-stu-id="512fa-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="512fa-117">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="512fa-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-118">Tableau contenant les données du paquet pour les traits.</span><span class="sxs-lookup"><span data-stu-id="512fa-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="512fa-119">*ppContextNodeStrokeAddedTo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="512fa-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="512fa-120">[**IContextNode**](icontextnode.md) auquel l’analyseur d’encre a ajouté les traits.</span><span class="sxs-lookup"><span data-stu-id="512fa-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="512fa-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="512fa-121">Return value</span></span>

<span data-ttu-id="512fa-122">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="512fa-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="512fa-123">Notes</span><span class="sxs-lookup"><span data-stu-id="512fa-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="512fa-124">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="512fa-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="512fa-125">Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="512fa-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="512fa-126">[**IInkAnalyzer**](iinkanalyzer.md) ajoute les traits à un [**IContextNode**](icontextnode.md) de type UnclassifiedInk (consultez types de [nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="512fa-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="512fa-127">Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="512fa-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="512fa-128">[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif aux traits et ajoute les traits au premier nœud de contexte UnclassifiedInk sous le nœud racine de l’analyseur d’encre qui contient des traits avec le même identificateur de culture.</span><span class="sxs-lookup"><span data-stu-id="512fa-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="512fa-129">Si l’analyseur d’encre n’a pas de nœud avec le même identificateur de culture, il crée un nœud de contexte UnclassifiedInk sous son nœud racine et ajoute les traits au nouveau nœud de contexte UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="512fa-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="512fa-130">*plStrokePacketData* contient des données de paquet pour tous les traits.</span><span class="sxs-lookup"><span data-stu-id="512fa-130">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="512fa-131">*pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait.</span><span class="sxs-lookup"><span data-stu-id="512fa-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="512fa-132">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="512fa-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="512fa-133">Seuls les traits avec les mêmes descriptions de paquets peuvent être ajoutés dans un seul appel à la **méthode IInkAnalyzer :: AddStrokes**.</span><span class="sxs-lookup"><span data-stu-id="512fa-133">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokes Method**.</span></span>

 

<span data-ttu-id="512fa-134">Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la zone et du cadre englobant des traits ajoutés.</span><span class="sxs-lookup"><span data-stu-id="512fa-134">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="512fa-135">Si le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que l’un des traits à ajouter, le **IInkAnalyzer** retourne un **HRESULT** d' **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="512fa-135">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="512fa-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="512fa-136">Requirements</span></span>



| <span data-ttu-id="512fa-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="512fa-137">Requirement</span></span> | <span data-ttu-id="512fa-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="512fa-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="512fa-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="512fa-139">Minimum supported client</span></span><br/> | <span data-ttu-id="512fa-140">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="512fa-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="512fa-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="512fa-141">Minimum supported server</span></span><br/> | <span data-ttu-id="512fa-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="512fa-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="512fa-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="512fa-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="512fa-144"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="512fa-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="512fa-145">DLL</span><span class="sxs-lookup"><span data-stu-id="512fa-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="512fa-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="512fa-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="512fa-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="512fa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512fa-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="512fa-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="512fa-149">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="512fa-149">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="512fa-150">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="512fa-150">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="512fa-151">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="512fa-151">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="512fa-152">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="512fa-152">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="512fa-153">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="512fa-153">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="512fa-154">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="512fa-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

