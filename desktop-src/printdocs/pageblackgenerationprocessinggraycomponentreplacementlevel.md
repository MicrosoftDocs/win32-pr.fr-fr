---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c0d55c2150f5a2299672ebf95d6656b238acc1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321730"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="6dab4-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="6dab4-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="6dab4-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="6dab4-105">This topic is not current.</span></span> <span data-ttu-id="6dab4-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6dab4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6dab4-107">Spécifie le pourcentage de remplacement des composants en gris à effectuer.</span><span class="sxs-lookup"><span data-stu-id="6dab4-107">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="6dab4-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6dab4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6dab4-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="6dab4-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6dab4-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6dab4-110">Element Information</span></span>



| <span data-ttu-id="6dab4-111">Nom</span><span class="sxs-lookup"><span data-stu-id="6dab4-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="6dab4-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="6dab4-112">Element Type</span></span> <br/>   | <span data-ttu-id="6dab4-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6dab4-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="6dab4-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="6dab4-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6dab4-115">Page</span><span class="sxs-lookup"><span data-stu-id="6dab4-115">Page</span></span><br/>                                            |
| <span data-ttu-id="6dab4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6dab4-116">Notes</span></span> <br/>          | <span data-ttu-id="6dab4-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="6dab4-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6dab4-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="6dab4-118">Structure Content</span></span>

<span data-ttu-id="6dab4-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="6dab4-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="6dab4-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="6dab4-120">Structure Properties</span></span>

<span data-ttu-id="6dab4-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="6dab4-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6dab4-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="6dab4-122">Property</span></span>                | <span data-ttu-id="6dab4-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6dab4-123">xsi:type</span></span>           | <span data-ttu-id="6dab4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dab4-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6dab4-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6dab4-125">DataType</span></span><br/>     | <span data-ttu-id="6dab4-126">string</span><span class="sxs-lookup"><span data-stu-id="6dab4-126">string</span></span><br/>  | <span data-ttu-id="6dab4-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6dab4-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="6dab4-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6dab4-128">DefaultValue</span></span><br/> | <span data-ttu-id="6dab4-129">string</span><span class="sxs-lookup"><span data-stu-id="6dab4-129">string</span></span><br/>  | <span data-ttu-id="6dab4-130">non défini</span><span class="sxs-lookup"><span data-stu-id="6dab4-130">undefined</span></span><br/>       |
| <span data-ttu-id="6dab4-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6dab4-131">MaxValue</span></span><br/>     | <span data-ttu-id="6dab4-132">entier</span><span class="sxs-lookup"><span data-stu-id="6dab4-132">integer</span></span><br/> | <span data-ttu-id="6dab4-133">100</span><span class="sxs-lookup"><span data-stu-id="6dab4-133">100</span></span><br/>             |
| <span data-ttu-id="6dab4-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="6dab4-134">MinValue</span></span><br/>     | <span data-ttu-id="6dab4-135">integer</span><span class="sxs-lookup"><span data-stu-id="6dab4-135">integer</span></span><br/> | <span data-ttu-id="6dab4-136">0</span><span class="sxs-lookup"><span data-stu-id="6dab4-136">0</span></span><br/>               |
| <span data-ttu-id="6dab4-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="6dab4-137">Multiple</span></span><br/>     | <span data-ttu-id="6dab4-138">integer</span><span class="sxs-lookup"><span data-stu-id="6dab4-138">integer</span></span><br/> | <span data-ttu-id="6dab4-139">1</span><span class="sxs-lookup"><span data-stu-id="6dab4-139">1</span></span><br/>               |
| <span data-ttu-id="6dab4-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6dab4-140">Mandatory</span></span><br/>    | <span data-ttu-id="6dab4-141">string</span><span class="sxs-lookup"><span data-stu-id="6dab4-141">string</span></span><br/>  | <span data-ttu-id="6dab4-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="6dab4-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6dab4-143">Unité</span><span class="sxs-lookup"><span data-stu-id="6dab4-143">UnitType</span></span><br/>     | <span data-ttu-id="6dab4-144">string</span><span class="sxs-lookup"><span data-stu-id="6dab4-144">string</span></span><br/>  | <span data-ttu-id="6dab4-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="6dab4-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6dab4-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6dab4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dab4-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="6dab4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




