---
description: 'Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un nœud d’indicateur d’analyse (consultez IContextNode :: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propriétés de l’indicateur d’analyse (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950886"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="61999-103">Propriétés de l’indicateur d’analyse</span><span class="sxs-lookup"><span data-stu-id="61999-103">Analysis Hint Properties</span></span>

<span data-ttu-id="61999-104">Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un nœud d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="61999-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="61999-105">Le tableau suivant décrit les informations référencées par chaque constante.</span><span class="sxs-lookup"><span data-stu-id="61999-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="61999-106">Constante</span><span class="sxs-lookup"><span data-stu-id="61999-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="61999-107">Description</span><span class="sxs-lookup"><span data-stu-id="61999-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="61999-108"><dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="61999-109">Indique si les termes partiels du dictionnaire sont autorisés sur un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="61999-110"><dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="61999-111">Nom d’un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="61999-112"><dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="61999-113">Indique si l’analyseur d’encre limite son analyse de l’encre dans la zone de l’indicateur pour se conformer au Factoid.</span><span class="sxs-lookup"><span data-stu-id="61999-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="61999-114"><dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="61999-115">L’indicateur contient un tableau de caractères qui représentent l’ensemble restreint de jeux de caractères Unicode pris en charge pris en charge par ce InkRecognizer.</span><span class="sxs-lookup"><span data-stu-id="61999-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="61999-116"><dt>**GUID \_ AHP \_ FACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="61999-117">Factoid sur un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="61999-118"><dt>**\_Guide AHP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="61999-119">Structure [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) qui représente le repère d’un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="61999-120"><dt>**GUID \_ AHP \_ PREFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="61999-121">Texte de préfixe sur un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="61999-122"><dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="61999-123">Texte de suffixe sur un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="61999-124"><dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="61999-125">Si les multiples segments dans les résultats de reconnaissance de l’encre sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="61999-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="61999-126"><dt>**AHP du GUID \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="61999-127">Tableau de chaînes qui représente la liste de mots d’un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="61999-128"><dt>**GUID \_ AHP \_ WORDMODE**</dt></span><span class="sxs-lookup"><span data-stu-id="61999-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="61999-129">Si l’analyseur d’encre établit une priorité pour les résultats à mots uniques sur les résultats à mots multiples pour un indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="61999-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="61999-130">Notes</span><span class="sxs-lookup"><span data-stu-id="61999-130">Remarks</span></span>

<span data-ttu-id="61999-131">Ces GUID sont utilisés pour identifier les propriétés que [**IInkAnalyzer**](iinkanalyzer.md) peut définir sur un nœud de contexte d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="61999-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="61999-132">Pour obtenir ou définir les propriétés d’un [**IContextNode**](icontextnode.md) en général, consultez [Propriétés du nœud de contexte](context-node-properties.md).</span><span class="sxs-lookup"><span data-stu-id="61999-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61999-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61999-133">Requirements</span></span>



| <span data-ttu-id="61999-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61999-134">Requirement</span></span> | <span data-ttu-id="61999-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="61999-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61999-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61999-136">Minimum supported client</span></span><br/> | <span data-ttu-id="61999-137">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61999-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="61999-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61999-138">Minimum supported server</span></span><br/> | <span data-ttu-id="61999-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="61999-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="61999-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="61999-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="61999-141"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="61999-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61999-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61999-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61999-143">Propriétés du nœud de contexte</span><span class="sxs-lookup"><span data-stu-id="61999-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="61999-144">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="61999-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="61999-145">**IInkAnalyzer :: CreateAnalysisHint, méthode**</span><span class="sxs-lookup"><span data-stu-id="61999-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="61999-146">**IInkAnalyzer :: GetAnalysisHintsByName, méthode**</span><span class="sxs-lookup"><span data-stu-id="61999-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="61999-147">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="61999-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="61999-148">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="61999-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="61999-149">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="61999-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="61999-150">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="61999-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="61999-151">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="61999-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="61999-152">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="61999-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="61999-153">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="61999-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




