---
description: Ajoute des données de trait pour plusieurs traits à un nœud de reconnaissance personnalisé.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512985"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="0fa07-103">IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode</span><span class="sxs-lookup"><span data-stu-id="0fa07-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="0fa07-104">Ajoute des données de trait pour plusieurs traits à un nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0fa07-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fa07-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="0fa07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fa07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fa07-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-108">Nombre de traits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0fa07-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-110">Tableau contenant les identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="0fa07-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-111">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-112">Nombre de propriétés dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="0fa07-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-113">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-114">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="0fa07-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-115">*pulPacketDataCountPerStroke* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-116">Tableau contenant le nombre de paquets dans chaque trait.</span><span class="sxs-lookup"><span data-stu-id="0fa07-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-117">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-118">Tableau contenant les données du paquet pour les traits.</span><span class="sxs-lookup"><span data-stu-id="0fa07-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-119">*pCustomRecognizer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-120">[**IContextNode**](icontextnode.md) de type **CustomRecognizer** auquel ajouter les traits.</span><span class="sxs-lookup"><span data-stu-id="0fa07-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-121">*ppContextNodeStrokeAddedTo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fa07-122">[**IContextNode**](icontextnode.md) auquel l’analyseur d’encre a ajouté les traits.</span><span class="sxs-lookup"><span data-stu-id="0fa07-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fa07-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0fa07-123">Return value</span></span>

<span data-ttu-id="0fa07-124">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="0fa07-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0fa07-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0fa07-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0fa07-126">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="0fa07-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="0fa07-127">Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0fa07-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="0fa07-128">[**IInkAnalyzer**](iinkanalyzer.md) ajoute les traits à un [**IContextNode**](icontextnode.md) de type **CustomRecognizer** (consultez types de [nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa07-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="0fa07-129">Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="0fa07-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="0fa07-130">[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif aux traits et ajoute les traits au premier nœud **UnclassifiedInk** sous le nœud **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="0fa07-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="0fa07-131">Si aucun nœud **UnclassifiedInk** n’existe, il est créé.</span><span class="sxs-lookup"><span data-stu-id="0fa07-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="0fa07-132">Si le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associé au nœud **CustomRecognizer** ne prend pas en charge l’identificateur de culture, le **IInkAnalyzer** continue à analyser et génère un avertissement [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa07-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="0fa07-133">Cet avertissement a la valeur [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="0fa07-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="0fa07-134">*plStrokePacketData* contient des données de paquet pour tous les traits.</span><span class="sxs-lookup"><span data-stu-id="0fa07-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="0fa07-135">*pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait.</span><span class="sxs-lookup"><span data-stu-id="0fa07-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="0fa07-136">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0fa07-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="0fa07-137">Seuls les traits avec les mêmes descriptions de paquets peuvent être ajoutés dans un seul appel à la **méthode IInkAnalyzer :: AddStrokesToCustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="0fa07-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="0fa07-138">Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la zone et du cadre englobant des traits ajoutés.</span><span class="sxs-lookup"><span data-stu-id="0fa07-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="0fa07-139">[**IInkAnalyzer**](iinkanalyzer.md) retourne un **HRESULT** d' **E \_ INVALIDARG** dans les circonstances suivantes.</span><span class="sxs-lookup"><span data-stu-id="0fa07-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="0fa07-140">Le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que l’un des traits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0fa07-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="0fa07-141">Le paramètre *pCustomRecognizer* contient un nœud de reconnaissance personnalisé associé à un objet [**IInkAnalyzer**](iinkanalyzer.md) différent.</span><span class="sxs-lookup"><span data-stu-id="0fa07-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="0fa07-142">Le paramètre *pCustomRecognizer* contient un [**IContextNode**](icontextnode.md) qui n’est pas de type **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="0fa07-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa07-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fa07-143">Requirements</span></span>



| <span data-ttu-id="0fa07-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fa07-144">Requirement</span></span> | <span data-ttu-id="0fa07-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fa07-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa07-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fa07-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa07-147">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0fa07-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fa07-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa07-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0fa07-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0fa07-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fa07-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fa07-151"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0fa07-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0fa07-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0fa07-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fa07-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fa07-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0fa07-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fa07-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fa07-155">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="0fa07-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0fa07-156">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="0fa07-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="0fa07-157">**IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="0fa07-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0fa07-158">**IInkAnalyzer :: CreateCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="0fa07-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="0fa07-159">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="0fa07-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

