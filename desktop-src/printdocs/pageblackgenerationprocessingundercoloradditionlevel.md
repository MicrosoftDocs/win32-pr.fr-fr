---
description: En savoir plus sur l’élément PageBlackGenerationProcessingUnderColorAdditionLevel, qui décrit l’encre chromatique chromatique à ajouter aux zones avec BlackInkLimit.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b496fbe890f53d1da8d1054cc5a19fe6318811
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408412"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="e3f59-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="e3f59-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="e3f59-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e3f59-104">This topic is not current.</span></span> <span data-ttu-id="e3f59-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3f59-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3f59-106">Décrit l’encre chromatique chromatique (en gris, les ratios de composants) à ajouter aux zones où GCR/UCR a généré « BlackInkLimit » (ou UCAStart, s’il est spécifié) dans les zones neutres sombres et quasi neutres.</span><span class="sxs-lookup"><span data-stu-id="e3f59-106">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="e3f59-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e3f59-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3f59-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="e3f59-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e3f59-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e3f59-109">Element Information</span></span>



| <span data-ttu-id="e3f59-110">Nom</span><span class="sxs-lookup"><span data-stu-id="e3f59-110">Name</span></span> | <span data-ttu-id="e3f59-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3f59-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e3f59-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e3f59-112">Element Type</span></span> <br/>   | <span data-ttu-id="e3f59-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e3f59-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="e3f59-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e3f59-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3f59-115">Page</span><span class="sxs-lookup"><span data-stu-id="e3f59-115">Page</span></span><br/>                                            |
| <span data-ttu-id="e3f59-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e3f59-116">Notes</span></span> <br/>          | <span data-ttu-id="e3f59-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="e3f59-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e3f59-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="e3f59-118">Structure Content</span></span>

<span data-ttu-id="e3f59-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="e3f59-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="e3f59-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="e3f59-120">Structure Properties</span></span>

<span data-ttu-id="e3f59-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e3f59-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3f59-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="e3f59-122">Property</span></span>                | <span data-ttu-id="e3f59-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e3f59-123">xsi:type</span></span>           | <span data-ttu-id="e3f59-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3f59-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e3f59-125">DataType</span><span class="sxs-lookup"><span data-stu-id="e3f59-125">DataType</span></span><br/>     | <span data-ttu-id="e3f59-126">string</span><span class="sxs-lookup"><span data-stu-id="e3f59-126">string</span></span><br/>  | <span data-ttu-id="e3f59-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e3f59-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="e3f59-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e3f59-128">DefaultValue</span></span><br/> | <span data-ttu-id="e3f59-129">string</span><span class="sxs-lookup"><span data-stu-id="e3f59-129">string</span></span><br/>  | <span data-ttu-id="e3f59-130">non défini</span><span class="sxs-lookup"><span data-stu-id="e3f59-130">undefined</span></span><br/>       |
| <span data-ttu-id="e3f59-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e3f59-131">MaxValue</span></span><br/>     | <span data-ttu-id="e3f59-132">entier</span><span class="sxs-lookup"><span data-stu-id="e3f59-132">integer</span></span><br/> | <span data-ttu-id="e3f59-133">100</span><span class="sxs-lookup"><span data-stu-id="e3f59-133">100</span></span><br/>             |
| <span data-ttu-id="e3f59-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="e3f59-134">MinValue</span></span><br/>     | <span data-ttu-id="e3f59-135">entier</span><span class="sxs-lookup"><span data-stu-id="e3f59-135">integer</span></span><br/> | <span data-ttu-id="e3f59-136">0</span><span class="sxs-lookup"><span data-stu-id="e3f59-136">0</span></span><br/>               |
| <span data-ttu-id="e3f59-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="e3f59-137">Multiple</span></span><br/>     | <span data-ttu-id="e3f59-138">integer</span><span class="sxs-lookup"><span data-stu-id="e3f59-138">integer</span></span><br/> | <span data-ttu-id="e3f59-139">1</span><span class="sxs-lookup"><span data-stu-id="e3f59-139">1</span></span><br/>               |
| <span data-ttu-id="e3f59-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e3f59-140">Mandatory</span></span><br/>    | <span data-ttu-id="e3f59-141">string</span><span class="sxs-lookup"><span data-stu-id="e3f59-141">string</span></span><br/>  | <span data-ttu-id="e3f59-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="e3f59-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e3f59-143">Unité</span><span class="sxs-lookup"><span data-stu-id="e3f59-143">UnitType</span></span><br/>     | <span data-ttu-id="e3f59-144">string</span><span class="sxs-lookup"><span data-stu-id="e3f59-144">string</span></span><br/>  | <span data-ttu-id="e3f59-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="e3f59-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e3f59-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3f59-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f59-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e3f59-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




