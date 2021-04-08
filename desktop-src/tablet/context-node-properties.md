---
description: Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un IContextNode.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Propriétés du nœud de contexte (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8eb1034516c62e2121f835951d1f04db5710d275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861770"
---
# <a name="context-node-properties"></a><span data-ttu-id="61809-103">Propriétés du nœud de contexte</span><span class="sxs-lookup"><span data-stu-id="61809-103">Context Node Properties</span></span>

<span data-ttu-id="61809-104">Définit des identificateurs globaux uniques (GUID) pour les propriétés d’un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="61809-104">Defines globally unique identifiers (GUIDs) for properties of an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="61809-105">Le tableau suivant décrit les informations référencées par chaque constante.</span><span class="sxs-lookup"><span data-stu-id="61809-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="61809-106">Constante</span><span class="sxs-lookup"><span data-stu-id="61809-106">Constant</span></span>                                                                                                                                                                                                 | <span data-ttu-id="61809-107">Description</span><span class="sxs-lookup"><span data-stu-id="61809-107">Description</span></span>                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <span data-ttu-id="61809-108"><dt>**GUID \_ CNP \_ ALIGNMENTLEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-108"><dt>**GUID\_CNP\_ALIGNMENTLEVEL**</dt></span></span> </dl>             | <span data-ttu-id="61809-109">Niveau d’alignement d’un paragraphe.</span><span class="sxs-lookup"><span data-stu-id="61809-109">The alignment level of a paragraph.</span></span><br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <span data-ttu-id="61809-110"><dt>**GUID \_ CNP \_ ascendants**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-110"><dt>**GUID\_CNP\_ASCENDERS**</dt></span></span> </dl>                            | <span data-ttu-id="61809-111">Hampes supérieures d’un mot d’encre.</span><span class="sxs-lookup"><span data-stu-id="61809-111">The ascenders of an ink word.</span></span><br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <span data-ttu-id="61809-112"><dt>**\_ligne de \_ base GUID CNP**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-112"><dt>**GUID\_CNP\_BASELINE**</dt></span></span> </dl>                               | <span data-ttu-id="61809-113">Ligne de base d’un mot encre.</span><span class="sxs-lookup"><span data-stu-id="61809-113">The baseline of an ink word.</span></span><br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <span data-ttu-id="61809-114"><dt>**GUID \_ CNP \_ CONFIDENCELEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-114"><dt>**GUID\_CNP\_CONFIDENCELEVEL**</dt></span></span> </dl>          | <span data-ttu-id="61809-115">Niveau de confiance dans les résultats de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="61809-115">The confidence level in the recognition results.</span></span><br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <span data-ttu-id="61809-116"><dt>**GUID \_ CNP \_ CUSTOMRECOGNIZERID**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-116"><dt>**GUID\_CNP\_CUSTOMRECOGNIZERID**</dt></span></span> </dl> | <span data-ttu-id="61809-117">Identificateur du module de reconnaissance d’encre personnalisé pour un nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="61809-117">The identifier of the custom ink recognizer for a custom recognizer node.</span></span><br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <span data-ttu-id="61809-118"><dt>**GUID \_ CNP les \_ descendants**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-118"><dt>**GUID\_CNP\_DESCENDERS**</dt></span></span> </dl>                         | <span data-ttu-id="61809-119">Descendants d’un mot d’encre.</span><span class="sxs-lookup"><span data-stu-id="61809-119">The descenders of an ink word.</span></span><br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <span data-ttu-id="61809-120"><dt>**GUID \_ CNP- \_ média**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-120"><dt>**GUID\_CNP\_MIDLINE**</dt></span></span> </dl>                                  | <span data-ttu-id="61809-121">La médiane d’un mot manuscrit.</span><span class="sxs-lookup"><span data-stu-id="61809-121">The midline of an ink word.</span></span><br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <span data-ttu-id="61809-122"><dt>**GUID \_ CNP \_ NODEDATA**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-122"><dt>**GUID\_CNP\_NODEDATA**</dt></span></span> </dl>                               | <span data-ttu-id="61809-123">Données d’image ou données texte d’une image ou d’un mot de texte.</span><span class="sxs-lookup"><span data-stu-id="61809-123">The image data or text data of an image or a text word.</span></span><br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <span data-ttu-id="61809-124"><dt>**GUID \_ CNP \_ RECOGNIZEDSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-124"><dt>**GUID\_CNP\_RECOGNIZEDSTRING**</dt></span></span> </dl>       | <span data-ttu-id="61809-125">Chaîne reconnue.</span><span class="sxs-lookup"><span data-stu-id="61809-125">The recognized string.</span></span><br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <span data-ttu-id="61809-126"><dt>**GUID \_ CNP \_ ROTATEDBOUNDINGBOX**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-126"><dt>**GUID\_CNP\_ROTATEDBOUNDINGBOX**</dt></span></span> </dl> | <span data-ttu-id="61809-127">Rectangle englobant pivoté.</span><span class="sxs-lookup"><span data-stu-id="61809-127">The rotated bounding box.</span></span><br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <span data-ttu-id="61809-128"><dt>**GUID \_ CNP \_ SEMANTICTYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-128"><dt>**GUID\_CNP\_SEMANTICTYPE**</dt></span></span> </dl>                   | <span data-ttu-id="61809-129">La propriété contient des informations sur les types sémantiques utilisés pour la définition d’une annotation, par exemple s’il s’agit d’une légende, d’un commentaire, etc.</span><span class="sxs-lookup"><span data-stu-id="61809-129">The property contains information about the semantic types used in defining an annotation, such as whether it is a callout, a comment, and so on.</span></span><br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <span data-ttu-id="61809-130"><dt>**GUID \_ CNP \_ SHAPENAME**</dt></span><span class="sxs-lookup"><span data-stu-id="61809-130"><dt>**GUID\_CNP\_SHAPENAME**</dt></span></span> </dl>                            | <span data-ttu-id="61809-131">Nom de forme d’un nœud de dessin d’encre.</span><span class="sxs-lookup"><span data-stu-id="61809-131">The shape name of an ink drawing node.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="61809-132">Notes</span><span class="sxs-lookup"><span data-stu-id="61809-132">Remarks</span></span>

<span data-ttu-id="61809-133">Ces GUID sont utilisés pour identifier les propriétés que [**IInkAnalyzer**](iinkanalyzer.md) peut définir sur un [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="61809-133">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="61809-134">L’analyseur d’encre définit des données de propriété basées sur le type du nœud de contexte (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="61809-134">The ink analyzer sets some property data based on the context node's type (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="61809-135">Pour obtenir ou définir des propriétés spécifiques aux nœuds d’indicateurs d’analyse, consultez Propriétés de l' [**indicateur d’analyse**](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="61809-135">To get or set properties specific to analysis hint nodes, see [**Analysis Hint Properties**](analysis-hint-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61809-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61809-136">Requirements</span></span>



| <span data-ttu-id="61809-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61809-137">Requirement</span></span> | <span data-ttu-id="61809-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="61809-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61809-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61809-139">Minimum supported client</span></span><br/> | <span data-ttu-id="61809-140">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61809-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="61809-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61809-141">Minimum supported server</span></span><br/> | <span data-ttu-id="61809-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="61809-142">None supported</span></span><br/>                                                           |
| <span data-ttu-id="61809-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="61809-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="61809-144"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="61809-144"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61809-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61809-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61809-146">Propriétés de l’indicateur d’analyse</span><span class="sxs-lookup"><span data-stu-id="61809-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="61809-147">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="61809-147">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="61809-148">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="61809-148">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="61809-149">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="61809-149">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="61809-150">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="61809-150">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="61809-151">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="61809-151">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="61809-152">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="61809-152">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="61809-153">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="61809-153">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="61809-154">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="61809-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




