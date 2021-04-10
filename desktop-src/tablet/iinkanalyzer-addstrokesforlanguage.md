---
description: Ajoute des données de trait pour plusieurs traits à IInkAnalyzer et assigne l’identificateur de culture spécifié aux traits.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'IInkAnalyzer :: AddStrokesForLanguage, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201505"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a><span data-ttu-id="52905-103">IInkAnalyzer :: AddStrokesForLanguage, méthode</span><span class="sxs-lookup"><span data-stu-id="52905-103">IInkAnalyzer::AddStrokesForLanguage method</span></span>

<span data-ttu-id="52905-104">Ajoute des données de trait pour plusieurs traits à [**IInkAnalyzer**](iinkanalyzer.md) et assigne l’identificateur de culture spécifié aux traits.</span><span class="sxs-lookup"><span data-stu-id="52905-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the specified culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="52905-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52905-105">Syntax</span></span>


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="52905-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52905-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52905-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-108">Nombre de traits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="52905-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="52905-109">*plIdofStrokesToAdd* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-109">*plIdofStrokesToAdd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-110">Tableau contenant les identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="52905-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="52905-111">*lStrokesLCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-112">Valeur qui représente l’identificateur de culture à assigner aux traits.</span><span class="sxs-lookup"><span data-stu-id="52905-112">A value that represents the culture identifier to assign to the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="52905-113">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-114">Nombre de propriétés dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="52905-114">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="52905-115">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-116">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="52905-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="52905-117">*pulPacketDataCountPerStroke* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-117">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-118">Tableau contenant le nombre de paquets dans chaque trait.</span><span class="sxs-lookup"><span data-stu-id="52905-118">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="52905-119">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52905-119">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-120">Tableau contenant les données du paquet pour les traits.</span><span class="sxs-lookup"><span data-stu-id="52905-120">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="52905-121">*ppContextNodeStrokeAddedTo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="52905-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52905-122">[**IContextNode**](icontextnode.md) auquel l’analyseur d’encre a ajouté les traits.</span><span class="sxs-lookup"><span data-stu-id="52905-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52905-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52905-123">Return value</span></span>

<span data-ttu-id="52905-124">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="52905-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52905-125">Notes</span><span class="sxs-lookup"><span data-stu-id="52905-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="52905-126">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="52905-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="52905-127">Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="52905-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="52905-128">[**IInkAnalyzer**](iinkanalyzer.md) ajoute les traits à un [**IContextNode**](icontextnode.md) de type UnclassifiedInk (consultez types de [nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="52905-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="52905-129">Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="52905-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="52905-130">[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture *lStrokeLCID* aux traits et ajoute les traits au premier nœud de contexte UnclassifiedInk sous le nœud racine de l’analyseur d’encre qui contient des traits avec le même identificateur de culture.</span><span class="sxs-lookup"><span data-stu-id="52905-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the *lStrokeLCID* culture identifier to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="52905-131">Si l’analyseur d’encre n’a pas de nœud avec le même identificateur de culture, il crée un nœud de contexte UnclassifiedInk sous son nœud racine et ajoute les traits au nouveau nœud de contexte UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="52905-131">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="52905-132">*plStrokePacketData* contient des données de paquet pour tous les traits.</span><span class="sxs-lookup"><span data-stu-id="52905-132">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="52905-133">*pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait.</span><span class="sxs-lookup"><span data-stu-id="52905-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="52905-134">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="52905-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="52905-135">Seuls les traits avec les mêmes descriptions de paquets peuvent être ajoutés dans un seul appel à la [**méthode IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="52905-135">Only strokes with the same packet descriptions can be added in a single call to [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md).</span></span>

 

<span data-ttu-id="52905-136">Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la zone et du cadre englobant des traits ajoutés.</span><span class="sxs-lookup"><span data-stu-id="52905-136">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="52905-137">Si le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que l’un des traits à ajouter, le **IInkAnalyzer** retourne un **HRESULT** d' **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="52905-137">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="52905-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52905-138">Requirements</span></span>



| <span data-ttu-id="52905-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52905-139">Requirement</span></span> | <span data-ttu-id="52905-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="52905-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52905-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52905-141">Minimum supported client</span></span><br/> | <span data-ttu-id="52905-142">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52905-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="52905-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52905-143">Minimum supported server</span></span><br/> | <span data-ttu-id="52905-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="52905-144">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="52905-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="52905-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="52905-146"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="52905-146"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="52905-147">DLL</span><span class="sxs-lookup"><span data-stu-id="52905-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52905-148"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52905-148"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="52905-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52905-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52905-150">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="52905-150">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="52905-151">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="52905-151">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="52905-152">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="52905-152">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="52905-153">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="52905-153">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="52905-154">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="52905-154">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="52905-155">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="52905-155">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="52905-156">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="52905-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

