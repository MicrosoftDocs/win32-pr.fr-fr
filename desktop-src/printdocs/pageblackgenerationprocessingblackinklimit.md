---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f565b6190f9bda11727efde6e799b6fb979cecc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523118"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="c5a8a-104">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="c5a8a-104">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="c5a8a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c5a8a-105">This topic is not current.</span></span> <span data-ttu-id="c5a8a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c5a8a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c5a8a-107">Le contenu de l’application étiqueté avec la couleur nommée spécifiée doit apparaître dans toutes les séparations de couleurs.</span><span class="sxs-lookup"><span data-stu-id="c5a8a-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="c5a8a-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c5a8a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c5a8a-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="c5a8a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c5a8a-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c5a8a-110">Element Information</span></span>



| <span data-ttu-id="c5a8a-111">Nom</span><span class="sxs-lookup"><span data-stu-id="c5a8a-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="c5a8a-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c5a8a-112">Element Type</span></span> <br/>   | <span data-ttu-id="c5a8a-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c5a8a-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="c5a8a-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="c5a8a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c5a8a-115">Page</span><span class="sxs-lookup"><span data-stu-id="c5a8a-115">Page</span></span><br/>                                            |
| <span data-ttu-id="c5a8a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c5a8a-116">Notes</span></span> <br/>          | <span data-ttu-id="c5a8a-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="c5a8a-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c5a8a-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="c5a8a-118">Structure Content</span></span>

<span data-ttu-id="c5a8a-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="c5a8a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
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

## <a name="structure-properties"></a><span data-ttu-id="c5a8a-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="c5a8a-120">Structure Properties</span></span>

<span data-ttu-id="c5a8a-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="c5a8a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c5a8a-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="c5a8a-122">Property</span></span>                | <span data-ttu-id="c5a8a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c5a8a-123">xsi:type</span></span>           | <span data-ttu-id="c5a8a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5a8a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c5a8a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c5a8a-125">DataType</span></span><br/>     | <span data-ttu-id="c5a8a-126">string</span><span class="sxs-lookup"><span data-stu-id="c5a8a-126">string</span></span><br/>  | <span data-ttu-id="c5a8a-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c5a8a-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="c5a8a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c5a8a-128">DefaultValue</span></span><br/> | <span data-ttu-id="c5a8a-129">string</span><span class="sxs-lookup"><span data-stu-id="c5a8a-129">string</span></span><br/>  | <span data-ttu-id="c5a8a-130">non défini</span><span class="sxs-lookup"><span data-stu-id="c5a8a-130">undefined</span></span><br/>       |
| <span data-ttu-id="c5a8a-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c5a8a-131">MaxValue</span></span><br/>     | <span data-ttu-id="c5a8a-132">entier</span><span class="sxs-lookup"><span data-stu-id="c5a8a-132">integer</span></span><br/> | <span data-ttu-id="c5a8a-133">100</span><span class="sxs-lookup"><span data-stu-id="c5a8a-133">100</span></span><br/>             |
| <span data-ttu-id="c5a8a-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="c5a8a-134">MinValue</span></span><br/>     | <span data-ttu-id="c5a8a-135">integer</span><span class="sxs-lookup"><span data-stu-id="c5a8a-135">integer</span></span><br/> | <span data-ttu-id="c5a8a-136">0</span><span class="sxs-lookup"><span data-stu-id="c5a8a-136">0</span></span><br/>               |
| <span data-ttu-id="c5a8a-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="c5a8a-137">Multiple</span></span><br/>     | <span data-ttu-id="c5a8a-138">integer</span><span class="sxs-lookup"><span data-stu-id="c5a8a-138">integer</span></span><br/> | <span data-ttu-id="c5a8a-139">1</span><span class="sxs-lookup"><span data-stu-id="c5a8a-139">1</span></span><br/>               |
| <span data-ttu-id="c5a8a-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c5a8a-140">Mandatory</span></span><br/>    | <span data-ttu-id="c5a8a-141">string</span><span class="sxs-lookup"><span data-stu-id="c5a8a-141">string</span></span><br/>  | <span data-ttu-id="c5a8a-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="c5a8a-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c5a8a-143">Unité</span><span class="sxs-lookup"><span data-stu-id="c5a8a-143">UnitType</span></span><br/>     | <span data-ttu-id="c5a8a-144">string</span><span class="sxs-lookup"><span data-stu-id="c5a8a-144">string</span></span><br/>  | <span data-ttu-id="c5a8a-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="c5a8a-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c5a8a-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5a8a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5a8a-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c5a8a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




