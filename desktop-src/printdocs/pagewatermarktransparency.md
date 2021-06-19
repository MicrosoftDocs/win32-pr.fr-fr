---
description: Obtenir des informations sur le paramètre PageWatermarkTransparency. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394784"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="06593-105">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="06593-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="06593-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="06593-106">This topic is not current.</span></span> <span data-ttu-id="06593-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="06593-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06593-108">Spécifie la transparence pour le filigrane.</span><span class="sxs-lookup"><span data-stu-id="06593-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="06593-109">Entièrement opaque a une valeur de 0.</span><span class="sxs-lookup"><span data-stu-id="06593-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="06593-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="06593-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06593-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="06593-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="06593-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="06593-112">Element Information</span></span>



| <span data-ttu-id="06593-113">Nom</span><span class="sxs-lookup"><span data-stu-id="06593-113">Name</span></span> | <span data-ttu-id="06593-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="06593-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="06593-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="06593-115">Element Type</span></span> <br/>   | <span data-ttu-id="06593-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="06593-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="06593-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="06593-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06593-118">Page</span><span class="sxs-lookup"><span data-stu-id="06593-118">Page</span></span><br/>                            |
| <span data-ttu-id="06593-119">Notes</span><span class="sxs-lookup"><span data-stu-id="06593-119">Notes</span></span> <br/>          | <span data-ttu-id="06593-120">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="06593-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="06593-121">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="06593-121">Structure Content</span></span>

<span data-ttu-id="06593-122">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="06593-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="06593-123">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="06593-123">Structure Properties</span></span>

<span data-ttu-id="06593-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="06593-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06593-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="06593-125">Property</span></span>                | <span data-ttu-id="06593-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="06593-126">xsi:type</span></span>           | <span data-ttu-id="06593-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="06593-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="06593-128">DataType</span><span class="sxs-lookup"><span data-stu-id="06593-128">DataType</span></span><br/>     | <span data-ttu-id="06593-129">string</span><span class="sxs-lookup"><span data-stu-id="06593-129">string</span></span><br/>  | <span data-ttu-id="06593-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06593-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="06593-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="06593-131">DefaultValue</span></span><br/> | <span data-ttu-id="06593-132">entier</span><span class="sxs-lookup"><span data-stu-id="06593-132">integer</span></span><br/> | <span data-ttu-id="06593-133">0</span><span class="sxs-lookup"><span data-stu-id="06593-133">0</span></span><br/>               |
| <span data-ttu-id="06593-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="06593-134">MaxValue</span></span><br/>     | <span data-ttu-id="06593-135">entier</span><span class="sxs-lookup"><span data-stu-id="06593-135">integer</span></span><br/> | <span data-ttu-id="06593-136">100</span><span class="sxs-lookup"><span data-stu-id="06593-136">100</span></span><br/>             |
| <span data-ttu-id="06593-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="06593-137">MinValue</span></span><br/>     | <span data-ttu-id="06593-138">entier</span><span class="sxs-lookup"><span data-stu-id="06593-138">integer</span></span><br/> | <span data-ttu-id="06593-139">0</span><span class="sxs-lookup"><span data-stu-id="06593-139">0</span></span><br/>               |
| <span data-ttu-id="06593-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="06593-140">Multiple</span></span><br/>     | <span data-ttu-id="06593-141">integer</span><span class="sxs-lookup"><span data-stu-id="06593-141">integer</span></span><br/> | <span data-ttu-id="06593-142">1</span><span class="sxs-lookup"><span data-stu-id="06593-142">1</span></span><br/>               |
| <span data-ttu-id="06593-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="06593-143">Mandatory</span></span><br/>    | <span data-ttu-id="06593-144">string</span><span class="sxs-lookup"><span data-stu-id="06593-144">string</span></span><br/>  | <span data-ttu-id="06593-145">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="06593-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="06593-146">Unité</span><span class="sxs-lookup"><span data-stu-id="06593-146">UnitType</span></span><br/>     | <span data-ttu-id="06593-147">string</span><span class="sxs-lookup"><span data-stu-id="06593-147">string</span></span><br/>  | <span data-ttu-id="06593-148">pour cent</span><span class="sxs-lookup"><span data-stu-id="06593-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="06593-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06593-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06593-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="06593-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




