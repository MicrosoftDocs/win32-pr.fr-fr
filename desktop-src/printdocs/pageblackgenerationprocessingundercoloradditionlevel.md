---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b43d8d9ee366fc742dc3d7b1617f6297fc96e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995666"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="37fd5-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="37fd5-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="37fd5-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="37fd5-105">This topic is not current.</span></span> <span data-ttu-id="37fd5-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="37fd5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="37fd5-107">Décrit l’encre chromatique chromatique (en gris, les ratios de composants) à ajouter aux zones où GCR/UCR a généré « BlackInkLimit » (ou UCAStart, s’il est spécifié) dans les zones neutres sombres et quasi neutres.</span><span class="sxs-lookup"><span data-stu-id="37fd5-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="37fd5-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="37fd5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="37fd5-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="37fd5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="37fd5-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="37fd5-110">Element Information</span></span>



| <span data-ttu-id="37fd5-111">Nom</span><span class="sxs-lookup"><span data-stu-id="37fd5-111">Name</span></span> | <span data-ttu-id="37fd5-112">Value</span><span class="sxs-lookup"><span data-stu-id="37fd5-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="37fd5-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="37fd5-113">Element Type</span></span> <br/>   | <span data-ttu-id="37fd5-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="37fd5-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="37fd5-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="37fd5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="37fd5-116">Page</span><span class="sxs-lookup"><span data-stu-id="37fd5-116">Page</span></span><br/>                                            |
| <span data-ttu-id="37fd5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="37fd5-117">Notes</span></span> <br/>          | <span data-ttu-id="37fd5-118">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="37fd5-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="37fd5-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="37fd5-119">Structure Content</span></span>

<span data-ttu-id="37fd5-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="37fd5-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="37fd5-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="37fd5-121">Structure Properties</span></span>

<span data-ttu-id="37fd5-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="37fd5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="37fd5-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="37fd5-123">Property</span></span>                | <span data-ttu-id="37fd5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="37fd5-124">xsi:type</span></span>           | <span data-ttu-id="37fd5-125">Value</span><span class="sxs-lookup"><span data-stu-id="37fd5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="37fd5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="37fd5-126">DataType</span></span><br/>     | <span data-ttu-id="37fd5-127">string</span><span class="sxs-lookup"><span data-stu-id="37fd5-127">string</span></span><br/>  | <span data-ttu-id="37fd5-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="37fd5-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="37fd5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="37fd5-129">DefaultValue</span></span><br/> | <span data-ttu-id="37fd5-130">string</span><span class="sxs-lookup"><span data-stu-id="37fd5-130">string</span></span><br/>  | <span data-ttu-id="37fd5-131">non défini</span><span class="sxs-lookup"><span data-stu-id="37fd5-131">undefined</span></span><br/>       |
| <span data-ttu-id="37fd5-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="37fd5-132">MaxValue</span></span><br/>     | <span data-ttu-id="37fd5-133">entier</span><span class="sxs-lookup"><span data-stu-id="37fd5-133">integer</span></span><br/> | <span data-ttu-id="37fd5-134">100</span><span class="sxs-lookup"><span data-stu-id="37fd5-134">100</span></span><br/>             |
| <span data-ttu-id="37fd5-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="37fd5-135">MinValue</span></span><br/>     | <span data-ttu-id="37fd5-136">entier</span><span class="sxs-lookup"><span data-stu-id="37fd5-136">integer</span></span><br/> | <span data-ttu-id="37fd5-137">0</span><span class="sxs-lookup"><span data-stu-id="37fd5-137">0</span></span><br/>               |
| <span data-ttu-id="37fd5-138">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="37fd5-138">Multiple</span></span><br/>     | <span data-ttu-id="37fd5-139">integer</span><span class="sxs-lookup"><span data-stu-id="37fd5-139">integer</span></span><br/> | <span data-ttu-id="37fd5-140">1</span><span class="sxs-lookup"><span data-stu-id="37fd5-140">1</span></span><br/>               |
| <span data-ttu-id="37fd5-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="37fd5-141">Mandatory</span></span><br/>    | <span data-ttu-id="37fd5-142">string</span><span class="sxs-lookup"><span data-stu-id="37fd5-142">string</span></span><br/>  | <span data-ttu-id="37fd5-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="37fd5-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="37fd5-144">Unité</span><span class="sxs-lookup"><span data-stu-id="37fd5-144">UnitType</span></span><br/>     | <span data-ttu-id="37fd5-145">string</span><span class="sxs-lookup"><span data-stu-id="37fd5-145">string</span></span><br/>  | <span data-ttu-id="37fd5-146">pour cent</span><span class="sxs-lookup"><span data-stu-id="37fd5-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="37fd5-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37fd5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37fd5-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="37fd5-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




