---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9a790d66d1f7806a7ef86ee4a85f62225aa836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997706"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="34279-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="34279-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="34279-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="34279-105">This topic is not current.</span></span> <span data-ttu-id="34279-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="34279-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="34279-107">Décrit le dépassant les neutres (en couleurs chromatiques) qui s’appliquent à GCR.</span><span class="sxs-lookup"><span data-stu-id="34279-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="34279-108">0% = remplacement de composant uniforme, 100% = remplacement de composant en gris.</span><span class="sxs-lookup"><span data-stu-id="34279-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="34279-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="34279-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="34279-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="34279-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="34279-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="34279-111">Element Information</span></span>



| <span data-ttu-id="34279-112">Nom</span><span class="sxs-lookup"><span data-stu-id="34279-112">Name</span></span> | <span data-ttu-id="34279-113">Value</span><span class="sxs-lookup"><span data-stu-id="34279-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="34279-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="34279-114">Element Type</span></span> <br/>   | <span data-ttu-id="34279-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="34279-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="34279-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="34279-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="34279-117">Page</span><span class="sxs-lookup"><span data-stu-id="34279-117">Page</span></span><br/>                                            |
| <span data-ttu-id="34279-118">Notes</span><span class="sxs-lookup"><span data-stu-id="34279-118">Notes</span></span> <br/>          | <span data-ttu-id="34279-119">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="34279-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="34279-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="34279-120">Structure Content</span></span>

<span data-ttu-id="34279-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="34279-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="34279-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="34279-122">Structure Properties</span></span>

<span data-ttu-id="34279-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="34279-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="34279-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="34279-124">Property</span></span>                | <span data-ttu-id="34279-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="34279-125">xsi:type</span></span>           | <span data-ttu-id="34279-126">Value</span><span class="sxs-lookup"><span data-stu-id="34279-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="34279-127">DataType</span><span class="sxs-lookup"><span data-stu-id="34279-127">DataType</span></span><br/>     | <span data-ttu-id="34279-128">string</span><span class="sxs-lookup"><span data-stu-id="34279-128">string</span></span><br/>  | <span data-ttu-id="34279-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="34279-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="34279-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="34279-130">DefaultValue</span></span><br/> | <span data-ttu-id="34279-131">string</span><span class="sxs-lookup"><span data-stu-id="34279-131">string</span></span><br/>  | <span data-ttu-id="34279-132">non défini</span><span class="sxs-lookup"><span data-stu-id="34279-132">undefined</span></span><br/>       |
| <span data-ttu-id="34279-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="34279-133">MaxValue</span></span><br/>     | <span data-ttu-id="34279-134">entier</span><span class="sxs-lookup"><span data-stu-id="34279-134">integer</span></span><br/> | <span data-ttu-id="34279-135">100</span><span class="sxs-lookup"><span data-stu-id="34279-135">100</span></span><br/>             |
| <span data-ttu-id="34279-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="34279-136">MinValue</span></span><br/>     | <span data-ttu-id="34279-137">entier</span><span class="sxs-lookup"><span data-stu-id="34279-137">integer</span></span><br/> | <span data-ttu-id="34279-138">0</span><span class="sxs-lookup"><span data-stu-id="34279-138">0</span></span><br/>               |
| <span data-ttu-id="34279-139">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="34279-139">Multiple</span></span><br/>     | <span data-ttu-id="34279-140">integer</span><span class="sxs-lookup"><span data-stu-id="34279-140">integer</span></span><br/> | <span data-ttu-id="34279-141">1</span><span class="sxs-lookup"><span data-stu-id="34279-141">1</span></span><br/>               |
| <span data-ttu-id="34279-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="34279-142">Mandatory</span></span><br/>    | <span data-ttu-id="34279-143">string</span><span class="sxs-lookup"><span data-stu-id="34279-143">string</span></span><br/>  | <span data-ttu-id="34279-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="34279-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="34279-145">Unité</span><span class="sxs-lookup"><span data-stu-id="34279-145">UnitType</span></span><br/>     | <span data-ttu-id="34279-146">string</span><span class="sxs-lookup"><span data-stu-id="34279-146">string</span></span><br/>  | <span data-ttu-id="34279-147">pour cent</span><span class="sxs-lookup"><span data-stu-id="34279-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="34279-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34279-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34279-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="34279-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




