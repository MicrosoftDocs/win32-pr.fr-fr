---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Passez en revue le paramètre PageBlackGenerationProcessingUnderColorAdditionStart. Cette rubrique n’est pas à jour. Pour plus d’informations, consultez la spécification du schéma d’impression.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549347"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="714d3-105">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="714d3-105">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="714d3-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="714d3-106">This topic is not current.</span></span> <span data-ttu-id="714d3-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="714d3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="714d3-108">Décrit le niveau d’ombre au-dessous duquel l’algorithme UCA sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="714d3-108">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="714d3-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="714d3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="714d3-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="714d3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="714d3-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="714d3-111">Element Information</span></span>



| <span data-ttu-id="714d3-112">Nom</span><span class="sxs-lookup"><span data-stu-id="714d3-112">Name</span></span> | <span data-ttu-id="714d3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="714d3-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="714d3-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="714d3-114">Element Type</span></span> <br/>   | <span data-ttu-id="714d3-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="714d3-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="714d3-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="714d3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="714d3-117">Page</span><span class="sxs-lookup"><span data-stu-id="714d3-117">Page</span></span><br/>                                            |
| <span data-ttu-id="714d3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="714d3-118">Notes</span></span> <br/>          | <span data-ttu-id="714d3-119">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="714d3-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="714d3-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="714d3-120">Structure Content</span></span>

<span data-ttu-id="714d3-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="714d3-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
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

## <a name="structure-properties"></a><span data-ttu-id="714d3-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="714d3-122">Structure Properties</span></span>

<span data-ttu-id="714d3-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="714d3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="714d3-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="714d3-124">Property</span></span>                | <span data-ttu-id="714d3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="714d3-125">xsi:type</span></span>           | <span data-ttu-id="714d3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="714d3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="714d3-127">DataType</span><span class="sxs-lookup"><span data-stu-id="714d3-127">DataType</span></span><br/>     | <span data-ttu-id="714d3-128">string</span><span class="sxs-lookup"><span data-stu-id="714d3-128">string</span></span><br/>  | <span data-ttu-id="714d3-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="714d3-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="714d3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="714d3-130">DefaultValue</span></span><br/> | <span data-ttu-id="714d3-131">string</span><span class="sxs-lookup"><span data-stu-id="714d3-131">string</span></span><br/>  | <span data-ttu-id="714d3-132">non défini</span><span class="sxs-lookup"><span data-stu-id="714d3-132">undefined</span></span><br/>       |
| <span data-ttu-id="714d3-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="714d3-133">MaxValue</span></span><br/>     | <span data-ttu-id="714d3-134">entier</span><span class="sxs-lookup"><span data-stu-id="714d3-134">integer</span></span><br/> | <span data-ttu-id="714d3-135">100</span><span class="sxs-lookup"><span data-stu-id="714d3-135">100</span></span><br/>             |
| <span data-ttu-id="714d3-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="714d3-136">MinValue</span></span><br/>     | <span data-ttu-id="714d3-137">entier</span><span class="sxs-lookup"><span data-stu-id="714d3-137">integer</span></span><br/> | <span data-ttu-id="714d3-138">0</span><span class="sxs-lookup"><span data-stu-id="714d3-138">0</span></span><br/>               |
| <span data-ttu-id="714d3-139">Multiple</span><span class="sxs-lookup"><span data-stu-id="714d3-139">Multiple</span></span><br/>     | <span data-ttu-id="714d3-140">integer</span><span class="sxs-lookup"><span data-stu-id="714d3-140">integer</span></span><br/> | <span data-ttu-id="714d3-141">1</span><span class="sxs-lookup"><span data-stu-id="714d3-141">1</span></span><br/>               |
| <span data-ttu-id="714d3-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="714d3-142">Mandatory</span></span><br/>    | <span data-ttu-id="714d3-143">string</span><span class="sxs-lookup"><span data-stu-id="714d3-143">string</span></span><br/>  | <span data-ttu-id="714d3-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="714d3-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="714d3-145">Unité</span><span class="sxs-lookup"><span data-stu-id="714d3-145">UnitType</span></span><br/>     | <span data-ttu-id="714d3-146">string</span><span class="sxs-lookup"><span data-stu-id="714d3-146">string</span></span><br/>  | <span data-ttu-id="714d3-147">pour cent</span><span class="sxs-lookup"><span data-stu-id="714d3-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="714d3-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="714d3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="714d3-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="714d3-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




