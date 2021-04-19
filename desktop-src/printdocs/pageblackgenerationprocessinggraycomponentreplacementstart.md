---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dedf425cd31dd83bce877358c456d1cd16183fa
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106532172"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="f75aa-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="f75aa-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="f75aa-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="f75aa-105">This topic is not current.</span></span> <span data-ttu-id="f75aa-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f75aa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f75aa-107">Décrit le point dans la plage « mettre en surbrillance pour l’ombre » où GCR doit démarrer (100% de l’ombre la plus sombre).</span><span class="sxs-lookup"><span data-stu-id="f75aa-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="f75aa-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f75aa-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f75aa-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f75aa-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f75aa-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f75aa-110">Element Information</span></span>



| <span data-ttu-id="f75aa-111">Nom</span><span class="sxs-lookup"><span data-stu-id="f75aa-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="f75aa-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="f75aa-112">Element Type</span></span> <br/>   | <span data-ttu-id="f75aa-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f75aa-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="f75aa-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="f75aa-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f75aa-115">Page</span><span class="sxs-lookup"><span data-stu-id="f75aa-115">Page</span></span><br/>                                            |
| <span data-ttu-id="f75aa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f75aa-116">Notes</span></span> <br/>          | <span data-ttu-id="f75aa-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="f75aa-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f75aa-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f75aa-118">Structure Content</span></span>

<span data-ttu-id="f75aa-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="f75aa-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="f75aa-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="f75aa-120">Structure Properties</span></span>

<span data-ttu-id="f75aa-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="f75aa-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f75aa-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="f75aa-122">Property</span></span>                | <span data-ttu-id="f75aa-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f75aa-123">xsi:type</span></span>           | <span data-ttu-id="f75aa-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f75aa-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f75aa-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f75aa-125">DataType</span></span><br/>     | <span data-ttu-id="f75aa-126">string</span><span class="sxs-lookup"><span data-stu-id="f75aa-126">string</span></span><br/>  | <span data-ttu-id="f75aa-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f75aa-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f75aa-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f75aa-128">DefaultValue</span></span><br/> | <span data-ttu-id="f75aa-129">string</span><span class="sxs-lookup"><span data-stu-id="f75aa-129">string</span></span><br/>  | <span data-ttu-id="f75aa-130">non défini</span><span class="sxs-lookup"><span data-stu-id="f75aa-130">undefined</span></span><br/>       |
| <span data-ttu-id="f75aa-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f75aa-131">MaxValue</span></span><br/>     | <span data-ttu-id="f75aa-132">entier</span><span class="sxs-lookup"><span data-stu-id="f75aa-132">integer</span></span><br/> | <span data-ttu-id="f75aa-133">100</span><span class="sxs-lookup"><span data-stu-id="f75aa-133">100</span></span><br/>             |
| <span data-ttu-id="f75aa-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f75aa-134">MinValue</span></span><br/>     | <span data-ttu-id="f75aa-135">integer</span><span class="sxs-lookup"><span data-stu-id="f75aa-135">integer</span></span><br/> | <span data-ttu-id="f75aa-136">0</span><span class="sxs-lookup"><span data-stu-id="f75aa-136">0</span></span><br/>               |
| <span data-ttu-id="f75aa-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="f75aa-137">Multiple</span></span><br/>     | <span data-ttu-id="f75aa-138">integer</span><span class="sxs-lookup"><span data-stu-id="f75aa-138">integer</span></span><br/> | <span data-ttu-id="f75aa-139">1</span><span class="sxs-lookup"><span data-stu-id="f75aa-139">1</span></span><br/>               |
| <span data-ttu-id="f75aa-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f75aa-140">Mandatory</span></span><br/>    | <span data-ttu-id="f75aa-141">string</span><span class="sxs-lookup"><span data-stu-id="f75aa-141">string</span></span><br/>  | <span data-ttu-id="f75aa-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="f75aa-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f75aa-143">Unité</span><span class="sxs-lookup"><span data-stu-id="f75aa-143">UnitType</span></span><br/>     | <span data-ttu-id="f75aa-144">string</span><span class="sxs-lookup"><span data-stu-id="f75aa-144">string</span></span><br/>  | <span data-ttu-id="f75aa-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="f75aa-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f75aa-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f75aa-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f75aa-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f75aa-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




