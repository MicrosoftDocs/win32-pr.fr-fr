---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996876"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="8238c-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="8238c-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="8238c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="8238c-105">This topic is not current.</span></span> <span data-ttu-id="8238c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8238c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8238c-107">Spécifie la transparence pour le filigrane.</span><span class="sxs-lookup"><span data-stu-id="8238c-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="8238c-108">Entièrement opaque a une valeur de 0.</span><span class="sxs-lookup"><span data-stu-id="8238c-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="8238c-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8238c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8238c-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8238c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8238c-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8238c-111">Element Information</span></span>



| <span data-ttu-id="8238c-112">Nom</span><span class="sxs-lookup"><span data-stu-id="8238c-112">Name</span></span> | <span data-ttu-id="8238c-113">Value</span><span class="sxs-lookup"><span data-stu-id="8238c-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="8238c-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="8238c-114">Element Type</span></span> <br/>   | <span data-ttu-id="8238c-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8238c-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="8238c-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="8238c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8238c-117">Page</span><span class="sxs-lookup"><span data-stu-id="8238c-117">Page</span></span><br/>                            |
| <span data-ttu-id="8238c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8238c-118">Notes</span></span> <br/>          | <span data-ttu-id="8238c-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="8238c-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8238c-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8238c-120">Structure Content</span></span>

<span data-ttu-id="8238c-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="8238c-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8238c-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="8238c-122">Structure Properties</span></span>

<span data-ttu-id="8238c-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="8238c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8238c-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="8238c-124">Property</span></span>                | <span data-ttu-id="8238c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8238c-125">xsi:type</span></span>           | <span data-ttu-id="8238c-126">Value</span><span class="sxs-lookup"><span data-stu-id="8238c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8238c-127">DataType</span><span class="sxs-lookup"><span data-stu-id="8238c-127">DataType</span></span><br/>     | <span data-ttu-id="8238c-128">string</span><span class="sxs-lookup"><span data-stu-id="8238c-128">string</span></span><br/>  | <span data-ttu-id="8238c-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8238c-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="8238c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8238c-130">DefaultValue</span></span><br/> | <span data-ttu-id="8238c-131">entier</span><span class="sxs-lookup"><span data-stu-id="8238c-131">integer</span></span><br/> | <span data-ttu-id="8238c-132">0</span><span class="sxs-lookup"><span data-stu-id="8238c-132">0</span></span><br/>               |
| <span data-ttu-id="8238c-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8238c-133">MaxValue</span></span><br/>     | <span data-ttu-id="8238c-134">entier</span><span class="sxs-lookup"><span data-stu-id="8238c-134">integer</span></span><br/> | <span data-ttu-id="8238c-135">100</span><span class="sxs-lookup"><span data-stu-id="8238c-135">100</span></span><br/>             |
| <span data-ttu-id="8238c-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="8238c-136">MinValue</span></span><br/>     | <span data-ttu-id="8238c-137">entier</span><span class="sxs-lookup"><span data-stu-id="8238c-137">integer</span></span><br/> | <span data-ttu-id="8238c-138">0</span><span class="sxs-lookup"><span data-stu-id="8238c-138">0</span></span><br/>               |
| <span data-ttu-id="8238c-139">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="8238c-139">Multiple</span></span><br/>     | <span data-ttu-id="8238c-140">integer</span><span class="sxs-lookup"><span data-stu-id="8238c-140">integer</span></span><br/> | <span data-ttu-id="8238c-141">1</span><span class="sxs-lookup"><span data-stu-id="8238c-141">1</span></span><br/>               |
| <span data-ttu-id="8238c-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8238c-142">Mandatory</span></span><br/>    | <span data-ttu-id="8238c-143">string</span><span class="sxs-lookup"><span data-stu-id="8238c-143">string</span></span><br/>  | <span data-ttu-id="8238c-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="8238c-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8238c-145">Unité</span><span class="sxs-lookup"><span data-stu-id="8238c-145">UnitType</span></span><br/>     | <span data-ttu-id="8238c-146">string</span><span class="sxs-lookup"><span data-stu-id="8238c-146">string</span></span><br/>  | <span data-ttu-id="8238c-147">pour cent</span><span class="sxs-lookup"><span data-stu-id="8238c-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8238c-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8238c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8238c-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="8238c-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




