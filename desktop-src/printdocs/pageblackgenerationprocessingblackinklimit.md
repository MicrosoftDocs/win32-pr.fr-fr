---
description: En savoir plus sur le paramètre PageBlackGenerationProcessingBlackInkLimit. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118424"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="a7852-105">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="a7852-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="a7852-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a7852-106">This topic is not current.</span></span> <span data-ttu-id="a7852-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7852-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a7852-108">Le contenu de l’application étiqueté avec la couleur nommée spécifiée doit apparaître dans toutes les séparations de couleurs.</span><span class="sxs-lookup"><span data-stu-id="a7852-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="a7852-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a7852-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a7852-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a7852-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a7852-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a7852-111">Element Information</span></span>



| <span data-ttu-id="a7852-112">Nom</span><span class="sxs-lookup"><span data-stu-id="a7852-112">Name</span></span> | <span data-ttu-id="a7852-113">Value</span><span class="sxs-lookup"><span data-stu-id="a7852-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="a7852-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a7852-114">Element Type</span></span> <br/>   | <span data-ttu-id="a7852-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a7852-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="a7852-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a7852-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a7852-117">Page</span><span class="sxs-lookup"><span data-stu-id="a7852-117">Page</span></span><br/>                                            |
| <span data-ttu-id="a7852-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7852-118">Notes</span></span> <br/>          | <span data-ttu-id="a7852-119">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="a7852-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a7852-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a7852-120">Structure Content</span></span>

<span data-ttu-id="a7852-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a7852-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a7852-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="a7852-122">Structure Properties</span></span>

<span data-ttu-id="a7852-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a7852-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a7852-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="a7852-124">Property</span></span>                | <span data-ttu-id="a7852-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a7852-125">xsi:type</span></span>           | <span data-ttu-id="a7852-126">Value</span><span class="sxs-lookup"><span data-stu-id="a7852-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a7852-127">DataType</span><span class="sxs-lookup"><span data-stu-id="a7852-127">DataType</span></span><br/>     | <span data-ttu-id="a7852-128">string</span><span class="sxs-lookup"><span data-stu-id="a7852-128">string</span></span><br/>  | <span data-ttu-id="a7852-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a7852-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="a7852-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a7852-130">DefaultValue</span></span><br/> | <span data-ttu-id="a7852-131">string</span><span class="sxs-lookup"><span data-stu-id="a7852-131">string</span></span><br/>  | <span data-ttu-id="a7852-132">non défini</span><span class="sxs-lookup"><span data-stu-id="a7852-132">undefined</span></span><br/>       |
| <span data-ttu-id="a7852-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a7852-133">MaxValue</span></span><br/>     | <span data-ttu-id="a7852-134">entier</span><span class="sxs-lookup"><span data-stu-id="a7852-134">integer</span></span><br/> | <span data-ttu-id="a7852-135">100</span><span class="sxs-lookup"><span data-stu-id="a7852-135">100</span></span><br/>             |
| <span data-ttu-id="a7852-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="a7852-136">MinValue</span></span><br/>     | <span data-ttu-id="a7852-137">entier</span><span class="sxs-lookup"><span data-stu-id="a7852-137">integer</span></span><br/> | <span data-ttu-id="a7852-138">0</span><span class="sxs-lookup"><span data-stu-id="a7852-138">0</span></span><br/>               |
| <span data-ttu-id="a7852-139">Multiple</span><span class="sxs-lookup"><span data-stu-id="a7852-139">Multiple</span></span><br/>     | <span data-ttu-id="a7852-140">integer</span><span class="sxs-lookup"><span data-stu-id="a7852-140">integer</span></span><br/> | <span data-ttu-id="a7852-141">1</span><span class="sxs-lookup"><span data-stu-id="a7852-141">1</span></span><br/>               |
| <span data-ttu-id="a7852-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a7852-142">Mandatory</span></span><br/>    | <span data-ttu-id="a7852-143">string</span><span class="sxs-lookup"><span data-stu-id="a7852-143">string</span></span><br/>  | <span data-ttu-id="a7852-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="a7852-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a7852-145">Unité</span><span class="sxs-lookup"><span data-stu-id="a7852-145">UnitType</span></span><br/>     | <span data-ttu-id="a7852-146">string</span><span class="sxs-lookup"><span data-stu-id="a7852-146">string</span></span><br/>  | <span data-ttu-id="a7852-147">pour cent</span><span class="sxs-lookup"><span data-stu-id="a7852-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a7852-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7852-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7852-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a7852-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




