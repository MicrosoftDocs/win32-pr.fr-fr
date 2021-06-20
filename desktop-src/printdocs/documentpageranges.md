---
description: En savoir plus sur l’élément DocumentPageRanges, qui décrit la plage de sortie du document dans les pages.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409252"
---
# <a name="documentpageranges"></a><span data-ttu-id="fcf5a-103">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="fcf5a-103">DocumentPageRanges</span></span>

<span data-ttu-id="fcf5a-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="fcf5a-104">This topic is not current.</span></span> <span data-ttu-id="fcf5a-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fcf5a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fcf5a-106">Décrit la plage de sortie du document dans les pages.</span><span class="sxs-lookup"><span data-stu-id="fcf5a-106">Describes the output range of the document in pages.</span></span> <span data-ttu-id="fcf5a-107">La valeur du paramètre doit être conforme à la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="fcf5a-107">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="fcf5a-108">PageRangeText : «*PageRange*» ou «*PageRange*,*PageRange*»</span><span class="sxs-lookup"><span data-stu-id="fcf5a-108">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="fcf5a-109">PageRange : «*pageNumber*»*ou « PageNumber* - *pageNumber*»</span><span class="sxs-lookup"><span data-stu-id="fcf5a-109">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="fcf5a-110">PageNumber : 1 à N, où N est le nombre de pages dans le document.</span><span class="sxs-lookup"><span data-stu-id="fcf5a-110">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="fcf5a-111">Si *pagenumber* > N, alors *pageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="fcf5a-111">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="fcf5a-112">Les espaces blancs dans la chaîne doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="fcf5a-112">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="fcf5a-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fcf5a-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fcf5a-114">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="fcf5a-114">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="fcf5a-115">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fcf5a-115">Element Information</span></span>



| <span data-ttu-id="fcf5a-116">Nom</span><span class="sxs-lookup"><span data-stu-id="fcf5a-116">Name</span></span> | <span data-ttu-id="fcf5a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcf5a-117">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="fcf5a-118">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="fcf5a-118">Element Type</span></span> <br/>   | <span data-ttu-id="fcf5a-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fcf5a-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="fcf5a-120">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="fcf5a-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fcf5a-121">Document</span><span class="sxs-lookup"><span data-stu-id="fcf5a-121">Document</span></span><br/>     |
| <span data-ttu-id="fcf5a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fcf5a-122">Notes</span></span> <br/>          | <span data-ttu-id="fcf5a-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="fcf5a-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="fcf5a-124">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="fcf5a-124">Structural Content</span></span>

<span data-ttu-id="fcf5a-125">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="fcf5a-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fcf5a-126">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="fcf5a-126">Structure Properties</span></span>

<span data-ttu-id="fcf5a-127">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="fcf5a-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fcf5a-128">Propriété</span><span class="sxs-lookup"><span data-stu-id="fcf5a-128">Property</span></span>                | <span data-ttu-id="fcf5a-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fcf5a-129">xsi:type</span></span>           | <span data-ttu-id="fcf5a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcf5a-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fcf5a-131">DataType</span><span class="sxs-lookup"><span data-stu-id="fcf5a-131">DataType</span></span><br/>     | <span data-ttu-id="fcf5a-132">string</span><span class="sxs-lookup"><span data-stu-id="fcf5a-132">string</span></span><br/>  | <span data-ttu-id="fcf5a-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="fcf5a-133">xs:string</span></span><br/>       |
| <span data-ttu-id="fcf5a-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fcf5a-134">DefaultValue</span></span><br/> | <span data-ttu-id="fcf5a-135">string</span><span class="sxs-lookup"><span data-stu-id="fcf5a-135">string</span></span><br/>  | <span data-ttu-id="fcf5a-136">non défini</span><span class="sxs-lookup"><span data-stu-id="fcf5a-136">undefined</span></span><br/>       |
| <span data-ttu-id="fcf5a-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="fcf5a-137">MaxLength</span></span><br/>    | <span data-ttu-id="fcf5a-138">entier</span><span class="sxs-lookup"><span data-stu-id="fcf5a-138">integer</span></span><br/> | <span data-ttu-id="fcf5a-139">non défini</span><span class="sxs-lookup"><span data-stu-id="fcf5a-139">undefined</span></span><br/>       |
| <span data-ttu-id="fcf5a-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="fcf5a-140">MinLength</span></span><br/>    | <span data-ttu-id="fcf5a-141">integer</span><span class="sxs-lookup"><span data-stu-id="fcf5a-141">integer</span></span><br/> | <span data-ttu-id="fcf5a-142">1</span><span class="sxs-lookup"><span data-stu-id="fcf5a-142">1</span></span><br/>               |
| <span data-ttu-id="fcf5a-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fcf5a-143">Mandatory</span></span><br/>    | <span data-ttu-id="fcf5a-144">string</span><span class="sxs-lookup"><span data-stu-id="fcf5a-144">string</span></span><br/>  | <span data-ttu-id="fcf5a-145">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="fcf5a-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fcf5a-146">Unité</span><span class="sxs-lookup"><span data-stu-id="fcf5a-146">UnitType</span></span><br/>     | <span data-ttu-id="fcf5a-147">string</span><span class="sxs-lookup"><span data-stu-id="fcf5a-147">string</span></span><br/>  | <span data-ttu-id="fcf5a-148">caractères</span><span class="sxs-lookup"><span data-stu-id="fcf5a-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="fcf5a-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcf5a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcf5a-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="fcf5a-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




