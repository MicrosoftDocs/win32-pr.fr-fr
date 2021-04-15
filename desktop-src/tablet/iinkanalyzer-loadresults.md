---
description: Charge les résultats d’analyse enregistrés dans le IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'IInkAnalyzer :: LoadResults, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485073"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="8fe7b-103">IInkAnalyzer :: LoadResults, méthode</span><span class="sxs-lookup"><span data-stu-id="8fe7b-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="8fe7b-104">Charge les résultats d’analyse enregistrés dans le [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="8fe7b-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fe7b-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="8fe7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fe7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe7b-107">*ulDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe7b-108">Nombre d’octets dans *pbSerializedResults*.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="8fe7b-109">*pbSerializedResults* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe7b-110">Résultats de l’analyse sérialisée.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="8fe7b-111">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe7b-112">Nombre d’identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8fe7b-113">*plOriginalStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe7b-114">Tableau d’identificateurs de trait d’origine.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8fe7b-115">*plNewStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe7b-116">Tableau de nouveaux identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8fe7b-117">*pfSuccessful* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe7b-118">**Variante \_ TRUE** si le chargement a réussi ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe7b-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fe7b-119">Return value</span></span>

<span data-ttu-id="8fe7b-120">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe7b-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8fe7b-121">Remarks</span></span>

<span data-ttu-id="8fe7b-122">Lorsque [**IInkAnalyzer**](iinkanalyzer.md) ajoute un [**IContextNode**](icontextnode.md) à partir des résultats enregistrés, il attribue un nouvel identificateur global unique (Guid) au **IContextNode** (voir [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md) et les propriétés du [nœud de contexte](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="8fe7b-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="8fe7b-123">Cette méthode ajoute les résultats d’analyse enregistrés à l’arborescence [**IContextNode**](icontextnode.md) existante.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="8fe7b-124">Pour vous assurer que les résultats combinés sont triés correctement, ajoutez la zone contenant les nœuds de contexte chargés à la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) et Réanalysez l’encre.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="8fe7b-125">Les méthodes de méthode [**IInkAnalyzer :: SaveResults**](iinkanalyzer-saveresults.md), [**IInkAnalyzer :: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)et [**IInkAnalyzer :: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) n’enregistrent pas les données de paquet avec les résultats d’analyse.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="8fe7b-126">Chaque identificateur dans *plOriginalStrokeIds* est l’identificateur de trait du trait dans les résultats d’analyse enregistrés.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="8fe7b-127">Chaque identificateur dans *plNewStrokeIds* est le nouvel identificateur avec lequel remplacer l’identificateur d’origine dans les résultats de l’analyse chargée.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="8fe7b-128">Si un indicateur d’analyse enregistré est en conflit avec un indicateur d’analyse existant, le [**IInkAnalyzer**](iinkanalyzer.md) ne charge pas l’indicateur enregistré, mais charge le reste des résultats enregistrés.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="8fe7b-129">Toutefois, si le **IInkAnalyzer** charge des résultats pour un trait qui se trouve dans la zone d’un indicateur d’analyse enregistré que le **IInkAnalyzer** ne charge pas, le **IInkAnalyzer** ajoute le cadre englobant du trait à la région de modification de l’objet **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="8fe7b-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="8fe7b-130">En outre, si le **IInkAnalyzer** charge des résultats pour un trait qui se trouve dans une zone d’indicateur d’analyse existante, le **IInkAnalyzer** ajoute également le cadre englobant du trait à la région de modification de l’objet **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="8fe7b-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="8fe7b-131">Pour plus d’informations sur les indicateurs d’analyse, consultez Propriétés de l' [indicateur d’analyse](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8fe7b-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="8fe7b-132">Cette méthode peut déclencher les événements [**\_ IAnalysisProxyEvents :: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents :: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)et [**\_ IAnalysisProxyEvents :: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) lors du chargement des résultats enregistrés.</span><span class="sxs-lookup"><span data-stu-id="8fe7b-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe7b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe7b-133">Requirements</span></span>



| <span data-ttu-id="8fe7b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe7b-134">Requirement</span></span> | <span data-ttu-id="8fe7b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe7b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe7b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe7b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe7b-137">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe7b-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8fe7b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe7b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe7b-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe7b-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8fe7b-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fe7b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe7b-141"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8fe7b-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8fe7b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe7b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe7b-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe7b-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8fe7b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe7b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe7b-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-147">**IInkAnalyzer :: GetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-148">**IInkAnalyzer :: SetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-149">**IInkAnalyzer :: SaveResults, méthode**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-150">**IInkAnalyzer :: SaveResultsForNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-151">**IInkAnalyzer :: SaveResultsForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="8fe7b-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="8fe7b-152">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8fe7b-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




