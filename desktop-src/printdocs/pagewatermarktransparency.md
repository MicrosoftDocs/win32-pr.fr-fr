---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106538440"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="bdc80-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="bdc80-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="bdc80-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="bdc80-105">This topic is not current.</span></span> <span data-ttu-id="bdc80-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bdc80-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bdc80-107">Spécifie la transparence pour le filigrane.</span><span class="sxs-lookup"><span data-stu-id="bdc80-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="bdc80-108">Entièrement opaque a une valeur de 0.</span><span class="sxs-lookup"><span data-stu-id="bdc80-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="bdc80-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bdc80-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bdc80-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="bdc80-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bdc80-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bdc80-111">Element Information</span></span>



| <span data-ttu-id="bdc80-112">Nom</span><span class="sxs-lookup"><span data-stu-id="bdc80-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="bdc80-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="bdc80-113">Element Type</span></span> <br/>   | <span data-ttu-id="bdc80-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bdc80-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="bdc80-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="bdc80-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bdc80-116">Page</span><span class="sxs-lookup"><span data-stu-id="bdc80-116">Page</span></span><br/>                            |
| <span data-ttu-id="bdc80-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bdc80-117">Notes</span></span> <br/>          | <span data-ttu-id="bdc80-118">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="bdc80-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bdc80-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="bdc80-119">Structure Content</span></span>

<span data-ttu-id="bdc80-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="bdc80-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="bdc80-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="bdc80-121">Structure Properties</span></span>

<span data-ttu-id="bdc80-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="bdc80-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bdc80-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="bdc80-123">Property</span></span>                | <span data-ttu-id="bdc80-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bdc80-124">xsi:type</span></span>           | <span data-ttu-id="bdc80-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdc80-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="bdc80-126">DataType</span><span class="sxs-lookup"><span data-stu-id="bdc80-126">DataType</span></span><br/>     | <span data-ttu-id="bdc80-127">string</span><span class="sxs-lookup"><span data-stu-id="bdc80-127">string</span></span><br/>  | <span data-ttu-id="bdc80-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bdc80-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="bdc80-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bdc80-129">DefaultValue</span></span><br/> | <span data-ttu-id="bdc80-130">integer</span><span class="sxs-lookup"><span data-stu-id="bdc80-130">integer</span></span><br/> | <span data-ttu-id="bdc80-131">0</span><span class="sxs-lookup"><span data-stu-id="bdc80-131">0</span></span><br/>               |
| <span data-ttu-id="bdc80-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bdc80-132">MaxValue</span></span><br/>     | <span data-ttu-id="bdc80-133">entier</span><span class="sxs-lookup"><span data-stu-id="bdc80-133">integer</span></span><br/> | <span data-ttu-id="bdc80-134">100</span><span class="sxs-lookup"><span data-stu-id="bdc80-134">100</span></span><br/>             |
| <span data-ttu-id="bdc80-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="bdc80-135">MinValue</span></span><br/>     | <span data-ttu-id="bdc80-136">integer</span><span class="sxs-lookup"><span data-stu-id="bdc80-136">integer</span></span><br/> | <span data-ttu-id="bdc80-137">0</span><span class="sxs-lookup"><span data-stu-id="bdc80-137">0</span></span><br/>               |
| <span data-ttu-id="bdc80-138">Multiple</span><span class="sxs-lookup"><span data-stu-id="bdc80-138">Multiple</span></span><br/>     | <span data-ttu-id="bdc80-139">integer</span><span class="sxs-lookup"><span data-stu-id="bdc80-139">integer</span></span><br/> | <span data-ttu-id="bdc80-140">1</span><span class="sxs-lookup"><span data-stu-id="bdc80-140">1</span></span><br/>               |
| <span data-ttu-id="bdc80-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bdc80-141">Mandatory</span></span><br/>    | <span data-ttu-id="bdc80-142">string</span><span class="sxs-lookup"><span data-stu-id="bdc80-142">string</span></span><br/>  | <span data-ttu-id="bdc80-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="bdc80-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="bdc80-144">Unité</span><span class="sxs-lookup"><span data-stu-id="bdc80-144">UnitType</span></span><br/>     | <span data-ttu-id="bdc80-145">string</span><span class="sxs-lookup"><span data-stu-id="bdc80-145">string</span></span><br/>  | <span data-ttu-id="bdc80-146">pour cent</span><span class="sxs-lookup"><span data-stu-id="bdc80-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="bdc80-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdc80-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc80-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="bdc80-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




