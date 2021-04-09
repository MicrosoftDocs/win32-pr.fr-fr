---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869657"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="96b6e-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="96b6e-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="96b6e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="96b6e-105">This topic is not current.</span></span> <span data-ttu-id="96b6e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="96b6e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="96b6e-107">Décrit le dépassant les neutres (en couleurs chromatiques) qui s’appliquent à GCR.</span><span class="sxs-lookup"><span data-stu-id="96b6e-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="96b6e-108">0% = remplacement de composant uniforme, 100% = remplacement de composant en gris.</span><span class="sxs-lookup"><span data-stu-id="96b6e-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="96b6e-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="96b6e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="96b6e-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="96b6e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="96b6e-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="96b6e-111">Element Information</span></span>



| <span data-ttu-id="96b6e-112">Nom</span><span class="sxs-lookup"><span data-stu-id="96b6e-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="96b6e-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="96b6e-113">Element Type</span></span> <br/>   | <span data-ttu-id="96b6e-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="96b6e-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="96b6e-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="96b6e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="96b6e-116">Page</span><span class="sxs-lookup"><span data-stu-id="96b6e-116">Page</span></span><br/>                                            |
| <span data-ttu-id="96b6e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="96b6e-117">Notes</span></span> <br/>          | <span data-ttu-id="96b6e-118">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="96b6e-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="96b6e-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="96b6e-119">Structure Content</span></span>

<span data-ttu-id="96b6e-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="96b6e-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="96b6e-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="96b6e-121">Structure Properties</span></span>

<span data-ttu-id="96b6e-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="96b6e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="96b6e-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="96b6e-123">Property</span></span>                | <span data-ttu-id="96b6e-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="96b6e-124">xsi:type</span></span>           | <span data-ttu-id="96b6e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="96b6e-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="96b6e-126">DataType</span><span class="sxs-lookup"><span data-stu-id="96b6e-126">DataType</span></span><br/>     | <span data-ttu-id="96b6e-127">string</span><span class="sxs-lookup"><span data-stu-id="96b6e-127">string</span></span><br/>  | <span data-ttu-id="96b6e-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96b6e-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="96b6e-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="96b6e-129">DefaultValue</span></span><br/> | <span data-ttu-id="96b6e-130">string</span><span class="sxs-lookup"><span data-stu-id="96b6e-130">string</span></span><br/>  | <span data-ttu-id="96b6e-131">non défini</span><span class="sxs-lookup"><span data-stu-id="96b6e-131">undefined</span></span><br/>       |
| <span data-ttu-id="96b6e-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="96b6e-132">MaxValue</span></span><br/>     | <span data-ttu-id="96b6e-133">entier</span><span class="sxs-lookup"><span data-stu-id="96b6e-133">integer</span></span><br/> | <span data-ttu-id="96b6e-134">100</span><span class="sxs-lookup"><span data-stu-id="96b6e-134">100</span></span><br/>             |
| <span data-ttu-id="96b6e-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="96b6e-135">MinValue</span></span><br/>     | <span data-ttu-id="96b6e-136">integer</span><span class="sxs-lookup"><span data-stu-id="96b6e-136">integer</span></span><br/> | <span data-ttu-id="96b6e-137">0</span><span class="sxs-lookup"><span data-stu-id="96b6e-137">0</span></span><br/>               |
| <span data-ttu-id="96b6e-138">Multiple</span><span class="sxs-lookup"><span data-stu-id="96b6e-138">Multiple</span></span><br/>     | <span data-ttu-id="96b6e-139">integer</span><span class="sxs-lookup"><span data-stu-id="96b6e-139">integer</span></span><br/> | <span data-ttu-id="96b6e-140">1</span><span class="sxs-lookup"><span data-stu-id="96b6e-140">1</span></span><br/>               |
| <span data-ttu-id="96b6e-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="96b6e-141">Mandatory</span></span><br/>    | <span data-ttu-id="96b6e-142">string</span><span class="sxs-lookup"><span data-stu-id="96b6e-142">string</span></span><br/>  | <span data-ttu-id="96b6e-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="96b6e-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="96b6e-144">Unité</span><span class="sxs-lookup"><span data-stu-id="96b6e-144">UnitType</span></span><br/>     | <span data-ttu-id="96b6e-145">string</span><span class="sxs-lookup"><span data-stu-id="96b6e-145">string</span></span><br/>  | <span data-ttu-id="96b6e-146">pour cent</span><span class="sxs-lookup"><span data-stu-id="96b6e-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="96b6e-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96b6e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b6e-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="96b6e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




