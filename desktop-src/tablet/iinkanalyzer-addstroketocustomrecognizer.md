---
description: Ajoute des données de trait pour un seul trait à un nœud de reconnaissance personnalisé.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516478"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="a1f76-103">IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode</span><span class="sxs-lookup"><span data-stu-id="a1f76-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="a1f76-104">Ajoute des données de trait pour un seul trait à un nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a1f76-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f76-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1f76-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="a1f76-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1f76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f76-107">*ulStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-108">Identificateur du trait à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a1f76-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="a1f76-109">*ulStrokePacketDataCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-110">Nombre de paquets dans le trait.</span><span class="sxs-lookup"><span data-stu-id="a1f76-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a1f76-111">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-112">Tableau contenant les données de paquet pour le trait.</span><span class="sxs-lookup"><span data-stu-id="a1f76-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a1f76-113">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-114">Nombre de propriétés de paquet dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="a1f76-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="a1f76-115">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-116">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="a1f76-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="a1f76-117">*pCustomRecognizer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-118">[**IContextNode**](icontextnode.md) de type **CustomRecognizer** auquel ajouter le trait.</span><span class="sxs-lookup"><span data-stu-id="a1f76-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a1f76-119">*ppContextNodeStrokeAddedTo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f76-120">[**IContextNode**](icontextnode.md) auquel l’analyseur d’encre a ajouté le trait.</span><span class="sxs-lookup"><span data-stu-id="a1f76-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f76-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1f76-121">Return value</span></span>

<span data-ttu-id="a1f76-122">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a1f76-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f76-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a1f76-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a1f76-124">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeStrokeAddedTo* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="a1f76-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a1f76-125">Quand *ppContextNodeStrokeAddedTo* a la valeur **null**, il indique que l’appelant ne s’intéresse pas à la valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a1f76-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="a1f76-126">[**IInkAnalyzer**](iinkanalyzer.md) ajoute le trait à un [**IContextNode**](icontextnode.md) de type **CustomRecognizer** (consultez [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="a1f76-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="a1f76-127">Ce nœud se trouve dans la collection de sous-nœuds du nœud racine (consultez les méthodes [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="a1f76-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="a1f76-128">[**IInkAnalyzer**](iinkanalyzer.md) assigne l’identificateur de culture du thread d’entrée actif au trait et ajoute le trait au premier nœud **UnclassifiedInk** sous le nœud **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="a1f76-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="a1f76-129">Si aucun nœud **UnclassifiedInk** n’existe, il est créé.</span><span class="sxs-lookup"><span data-stu-id="a1f76-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="a1f76-130">Si le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associé au nœud **CustomRecognizer** ne prend pas en charge l’identificateur de culture, le **IInkAnalyzer** continue à analyser et génère un avertissement [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f76-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="a1f76-131">Cet avertissement a la valeur [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="a1f76-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="a1f76-132">*plStrokePacketData* contient des données de paquet pour tous les points du trait.</span><span class="sxs-lookup"><span data-stu-id="a1f76-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="a1f76-133">*pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait.</span><span class="sxs-lookup"><span data-stu-id="a1f76-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="a1f76-134">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a1f76-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="a1f76-135">Cette méthode étend la région modifiée à l’Union de la valeur actuelle de la région et de la zone englobante du trait ajouté.</span><span class="sxs-lookup"><span data-stu-id="a1f76-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="a1f76-136">[**IInkAnalyzer**](iinkanalyzer.md) retourne un **HRESULT** d' **E \_ INVALIDARG** dans les circonstances suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1f76-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="a1f76-137">Le [**IInkAnalyzer**](iinkanalyzer.md) contient déjà un trait avec le même identificateur que le trait à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a1f76-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="a1f76-138">Le paramètre *pCustomRecognizer* contient un nœud de reconnaissance personnalisé associé à un objet [**IInkAnalyzer**](iinkanalyzer.md) différent.</span><span class="sxs-lookup"><span data-stu-id="a1f76-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="a1f76-139">Le paramètre *pCustomRecognizer* contient un [**IContextNode**](icontextnode.md) qui n’est pas de type **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="a1f76-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f76-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1f76-140">Requirements</span></span>



| <span data-ttu-id="a1f76-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1f76-141">Requirement</span></span> | <span data-ttu-id="a1f76-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f76-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f76-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f76-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f76-144">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1f76-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1f76-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f76-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f76-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f76-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a1f76-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1f76-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1f76-148"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1f76-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1f76-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a1f76-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1f76-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1f76-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a1f76-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1f76-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f76-152">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a1f76-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a1f76-153">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="a1f76-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="a1f76-154">**IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="a1f76-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a1f76-155">**IInkAnalyzer :: CreateCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="a1f76-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a1f76-156">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a1f76-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

