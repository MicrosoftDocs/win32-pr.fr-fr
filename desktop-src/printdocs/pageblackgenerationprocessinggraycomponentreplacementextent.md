---
description: Le paramètre PageBlackGenerationProcessingGrayComponentReplacementExtent décrit l’étendue au-delà des neutres dans les couleurs chromatiques que GCR applique.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3bd5e4fdbafba97884a7aed608b23e4c26ce1c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408502"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="dd11f-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="dd11f-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="dd11f-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="dd11f-104">This topic is not current.</span></span> <span data-ttu-id="dd11f-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dd11f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd11f-106">Décrit le dépassant les neutres (en couleurs chromatiques) qui s’appliquent à GCR.</span><span class="sxs-lookup"><span data-stu-id="dd11f-106">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="dd11f-107">0% = remplacement de composant uniforme, 100% = remplacement de composant en gris.</span><span class="sxs-lookup"><span data-stu-id="dd11f-107">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="dd11f-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dd11f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dd11f-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="dd11f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dd11f-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dd11f-110">Element Information</span></span>



| <span data-ttu-id="dd11f-111">Nom</span><span class="sxs-lookup"><span data-stu-id="dd11f-111">Name</span></span> | <span data-ttu-id="dd11f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd11f-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="dd11f-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="dd11f-113">Element Type</span></span> <br/>   | <span data-ttu-id="dd11f-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dd11f-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="dd11f-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="dd11f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dd11f-116">Page</span><span class="sxs-lookup"><span data-stu-id="dd11f-116">Page</span></span><br/>                                            |
| <span data-ttu-id="dd11f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="dd11f-117">Notes</span></span> <br/>          | <span data-ttu-id="dd11f-118">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="dd11f-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dd11f-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="dd11f-119">Structure Content</span></span>

<span data-ttu-id="dd11f-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="dd11f-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="dd11f-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="dd11f-121">Structure Properties</span></span>

<span data-ttu-id="dd11f-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="dd11f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dd11f-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="dd11f-123">Property</span></span>                | <span data-ttu-id="dd11f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dd11f-124">xsi:type</span></span>           | <span data-ttu-id="dd11f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd11f-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dd11f-126">DataType</span><span class="sxs-lookup"><span data-stu-id="dd11f-126">DataType</span></span><br/>     | <span data-ttu-id="dd11f-127">string</span><span class="sxs-lookup"><span data-stu-id="dd11f-127">string</span></span><br/>  | <span data-ttu-id="dd11f-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dd11f-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="dd11f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dd11f-129">DefaultValue</span></span><br/> | <span data-ttu-id="dd11f-130">string</span><span class="sxs-lookup"><span data-stu-id="dd11f-130">string</span></span><br/>  | <span data-ttu-id="dd11f-131">non défini</span><span class="sxs-lookup"><span data-stu-id="dd11f-131">undefined</span></span><br/>       |
| <span data-ttu-id="dd11f-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dd11f-132">MaxValue</span></span><br/>     | <span data-ttu-id="dd11f-133">entier</span><span class="sxs-lookup"><span data-stu-id="dd11f-133">integer</span></span><br/> | <span data-ttu-id="dd11f-134">100</span><span class="sxs-lookup"><span data-stu-id="dd11f-134">100</span></span><br/>             |
| <span data-ttu-id="dd11f-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="dd11f-135">MinValue</span></span><br/>     | <span data-ttu-id="dd11f-136">entier</span><span class="sxs-lookup"><span data-stu-id="dd11f-136">integer</span></span><br/> | <span data-ttu-id="dd11f-137">0</span><span class="sxs-lookup"><span data-stu-id="dd11f-137">0</span></span><br/>               |
| <span data-ttu-id="dd11f-138">Multiple</span><span class="sxs-lookup"><span data-stu-id="dd11f-138">Multiple</span></span><br/>     | <span data-ttu-id="dd11f-139">integer</span><span class="sxs-lookup"><span data-stu-id="dd11f-139">integer</span></span><br/> | <span data-ttu-id="dd11f-140">1</span><span class="sxs-lookup"><span data-stu-id="dd11f-140">1</span></span><br/>               |
| <span data-ttu-id="dd11f-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dd11f-141">Mandatory</span></span><br/>    | <span data-ttu-id="dd11f-142">string</span><span class="sxs-lookup"><span data-stu-id="dd11f-142">string</span></span><br/>  | <span data-ttu-id="dd11f-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="dd11f-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dd11f-144">Unité</span><span class="sxs-lookup"><span data-stu-id="dd11f-144">UnitType</span></span><br/>     | <span data-ttu-id="dd11f-145">string</span><span class="sxs-lookup"><span data-stu-id="dd11f-145">string</span></span><br/>  | <span data-ttu-id="dd11f-146">pour cent</span><span class="sxs-lookup"><span data-stu-id="dd11f-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dd11f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd11f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd11f-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="dd11f-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




