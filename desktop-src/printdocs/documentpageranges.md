---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997176"
---
# <a name="documentpageranges"></a><span data-ttu-id="cc049-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="cc049-104">DocumentPageRanges</span></span>

<span data-ttu-id="cc049-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="cc049-105">This topic is not current.</span></span> <span data-ttu-id="cc049-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cc049-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cc049-107">Décrit la plage de sortie du document dans les pages.</span><span class="sxs-lookup"><span data-stu-id="cc049-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="cc049-108">La valeur du paramètre doit être conforme à la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="cc049-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="cc049-109">PageRangeText : «*PageRange*» ou «*PageRange*,*PageRange*»</span><span class="sxs-lookup"><span data-stu-id="cc049-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="cc049-110">PageRange : «*pageNumber*»*ou « PageNumber* - *pageNumber*»</span><span class="sxs-lookup"><span data-stu-id="cc049-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="cc049-111">PageNumber : 1 à N, où N est le nombre de pages dans le document.</span><span class="sxs-lookup"><span data-stu-id="cc049-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="cc049-112">Si *pagenumber* > N, alors *pageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="cc049-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="cc049-113">Les espaces blancs dans la chaîne doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="cc049-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="cc049-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cc049-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cc049-115">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cc049-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="cc049-116">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cc049-116">Element Information</span></span>



| <span data-ttu-id="cc049-117">Nom</span><span class="sxs-lookup"><span data-stu-id="cc049-117">Name</span></span> | <span data-ttu-id="cc049-118">Value</span><span class="sxs-lookup"><span data-stu-id="cc049-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="cc049-119">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="cc049-119">Element Type</span></span> <br/>   | <span data-ttu-id="cc049-120">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cc049-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="cc049-121">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="cc049-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cc049-122">Document</span><span class="sxs-lookup"><span data-stu-id="cc049-122">Document</span></span><br/>     |
| <span data-ttu-id="cc049-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cc049-123">Notes</span></span> <br/>          | <span data-ttu-id="cc049-124">Aucun</span><span class="sxs-lookup"><span data-stu-id="cc049-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="cc049-125">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cc049-125">Structural Content</span></span>

<span data-ttu-id="cc049-126">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="cc049-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="cc049-127">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="cc049-127">Structure Properties</span></span>

<span data-ttu-id="cc049-128">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="cc049-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cc049-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="cc049-129">Property</span></span>                | <span data-ttu-id="cc049-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cc049-130">xsi:type</span></span>           | <span data-ttu-id="cc049-131">Value</span><span class="sxs-lookup"><span data-stu-id="cc049-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cc049-132">DataType</span><span class="sxs-lookup"><span data-stu-id="cc049-132">DataType</span></span><br/>     | <span data-ttu-id="cc049-133">string</span><span class="sxs-lookup"><span data-stu-id="cc049-133">string</span></span><br/>  | <span data-ttu-id="cc049-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc049-134">xs:string</span></span><br/>       |
| <span data-ttu-id="cc049-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cc049-135">DefaultValue</span></span><br/> | <span data-ttu-id="cc049-136">string</span><span class="sxs-lookup"><span data-stu-id="cc049-136">string</span></span><br/>  | <span data-ttu-id="cc049-137">non défini</span><span class="sxs-lookup"><span data-stu-id="cc049-137">undefined</span></span><br/>       |
| <span data-ttu-id="cc049-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="cc049-138">MaxLength</span></span><br/>    | <span data-ttu-id="cc049-139">entier</span><span class="sxs-lookup"><span data-stu-id="cc049-139">integer</span></span><br/> | <span data-ttu-id="cc049-140">non défini</span><span class="sxs-lookup"><span data-stu-id="cc049-140">undefined</span></span><br/>       |
| <span data-ttu-id="cc049-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="cc049-141">MinLength</span></span><br/>    | <span data-ttu-id="cc049-142">integer</span><span class="sxs-lookup"><span data-stu-id="cc049-142">integer</span></span><br/> | <span data-ttu-id="cc049-143">1</span><span class="sxs-lookup"><span data-stu-id="cc049-143">1</span></span><br/>               |
| <span data-ttu-id="cc049-144">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cc049-144">Mandatory</span></span><br/>    | <span data-ttu-id="cc049-145">string</span><span class="sxs-lookup"><span data-stu-id="cc049-145">string</span></span><br/>  | <span data-ttu-id="cc049-146">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="cc049-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cc049-147">Unité</span><span class="sxs-lookup"><span data-stu-id="cc049-147">UnitType</span></span><br/>     | <span data-ttu-id="cc049-148">string</span><span class="sxs-lookup"><span data-stu-id="cc049-148">string</span></span><br/>  | <span data-ttu-id="cc049-149">caractères</span><span class="sxs-lookup"><span data-stu-id="cc049-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="cc049-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc049-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc049-151">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="cc049-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




