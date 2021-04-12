---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321698"
---
# <a name="documentpageranges"></a><span data-ttu-id="2f80f-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="2f80f-104">DocumentPageRanges</span></span>

<span data-ttu-id="2f80f-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="2f80f-105">This topic is not current.</span></span> <span data-ttu-id="2f80f-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2f80f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2f80f-107">Décrit la plage de sortie du document dans les pages.</span><span class="sxs-lookup"><span data-stu-id="2f80f-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="2f80f-108">La valeur du paramètre doit être conforme à la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="2f80f-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="2f80f-109">PageRangeText : «*PageRange*» ou «*PageRange*,*PageRange*»</span><span class="sxs-lookup"><span data-stu-id="2f80f-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="2f80f-110">PageRange : «*pageNumber*»*ou « PageNumber* - *pageNumber*»</span><span class="sxs-lookup"><span data-stu-id="2f80f-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="2f80f-111">PageNumber : 1 à N, où N est le nombre de pages dans le document.</span><span class="sxs-lookup"><span data-stu-id="2f80f-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="2f80f-112">Si *pagenumber* > N, alors *pageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="2f80f-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="2f80f-113">Les espaces blancs dans la chaîne doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="2f80f-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="2f80f-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2f80f-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2f80f-115">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="2f80f-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="2f80f-116">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2f80f-116">Element Information</span></span>



| <span data-ttu-id="2f80f-117">Nom</span><span class="sxs-lookup"><span data-stu-id="2f80f-117">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="2f80f-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="2f80f-118">Element Type</span></span> <br/>   | <span data-ttu-id="2f80f-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2f80f-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="2f80f-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="2f80f-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2f80f-121">Document</span><span class="sxs-lookup"><span data-stu-id="2f80f-121">Document</span></span><br/>     |
| <span data-ttu-id="2f80f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="2f80f-122">Notes</span></span> <br/>          | <span data-ttu-id="2f80f-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="2f80f-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="2f80f-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="2f80f-124">Structural Content</span></span>

<span data-ttu-id="2f80f-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="2f80f-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2f80f-126">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="2f80f-126">Structure Properties</span></span>

<span data-ttu-id="2f80f-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="2f80f-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2f80f-128">Propriété</span><span class="sxs-lookup"><span data-stu-id="2f80f-128">Property</span></span>                | <span data-ttu-id="2f80f-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2f80f-129">xsi:type</span></span>           | <span data-ttu-id="2f80f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f80f-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2f80f-131">DataType</span><span class="sxs-lookup"><span data-stu-id="2f80f-131">DataType</span></span><br/>     | <span data-ttu-id="2f80f-132">string</span><span class="sxs-lookup"><span data-stu-id="2f80f-132">string</span></span><br/>  | <span data-ttu-id="2f80f-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="2f80f-133">xs:string</span></span><br/>       |
| <span data-ttu-id="2f80f-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2f80f-134">DefaultValue</span></span><br/> | <span data-ttu-id="2f80f-135">string</span><span class="sxs-lookup"><span data-stu-id="2f80f-135">string</span></span><br/>  | <span data-ttu-id="2f80f-136">non défini</span><span class="sxs-lookup"><span data-stu-id="2f80f-136">undefined</span></span><br/>       |
| <span data-ttu-id="2f80f-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="2f80f-137">MaxLength</span></span><br/>    | <span data-ttu-id="2f80f-138">entier</span><span class="sxs-lookup"><span data-stu-id="2f80f-138">integer</span></span><br/> | <span data-ttu-id="2f80f-139">non défini</span><span class="sxs-lookup"><span data-stu-id="2f80f-139">undefined</span></span><br/>       |
| <span data-ttu-id="2f80f-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="2f80f-140">MinLength</span></span><br/>    | <span data-ttu-id="2f80f-141">integer</span><span class="sxs-lookup"><span data-stu-id="2f80f-141">integer</span></span><br/> | <span data-ttu-id="2f80f-142">1</span><span class="sxs-lookup"><span data-stu-id="2f80f-142">1</span></span><br/>               |
| <span data-ttu-id="2f80f-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f80f-143">Mandatory</span></span><br/>    | <span data-ttu-id="2f80f-144">string</span><span class="sxs-lookup"><span data-stu-id="2f80f-144">string</span></span><br/>  | <span data-ttu-id="2f80f-145">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="2f80f-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2f80f-146">Unité</span><span class="sxs-lookup"><span data-stu-id="2f80f-146">UnitType</span></span><br/>     | <span data-ttu-id="2f80f-147">string</span><span class="sxs-lookup"><span data-stu-id="2f80f-147">string</span></span><br/>  | <span data-ttu-id="2f80f-148">caractères</span><span class="sxs-lookup"><span data-stu-id="2f80f-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="2f80f-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f80f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f80f-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="2f80f-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




