---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a9cd5532bf4d109b94c579ef2ad21d242aca9a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522516"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="a42ed-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="a42ed-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="a42ed-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a42ed-105">This topic is not current.</span></span> <span data-ttu-id="a42ed-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a42ed-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a42ed-107">Spécifie le décalage de mise à l’échelle dans la direction ImageableSizeWidth pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a42ed-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="a42ed-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a42ed-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a42ed-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a42ed-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a42ed-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a42ed-110">Element Information</span></span>



| <span data-ttu-id="a42ed-111">Nom</span><span class="sxs-lookup"><span data-stu-id="a42ed-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="a42ed-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a42ed-112">Element Type</span></span> <br/>   | <span data-ttu-id="a42ed-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a42ed-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="a42ed-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a42ed-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a42ed-115">Page</span><span class="sxs-lookup"><span data-stu-id="a42ed-115">Page</span></span><br/>                                         |
| <span data-ttu-id="a42ed-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a42ed-116">Notes</span></span> <br/>          | <span data-ttu-id="a42ed-117">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="a42ed-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a42ed-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a42ed-118">Structure Content</span></span>

<span data-ttu-id="a42ed-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a42ed-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="a42ed-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="a42ed-120">Structure Properties</span></span>

<span data-ttu-id="a42ed-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a42ed-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a42ed-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="a42ed-122">Property</span></span>                | <span data-ttu-id="a42ed-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a42ed-123">xsi:type</span></span>           | <span data-ttu-id="a42ed-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a42ed-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a42ed-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a42ed-125">DataType</span></span><br/>     | <span data-ttu-id="a42ed-126">string</span><span class="sxs-lookup"><span data-stu-id="a42ed-126">string</span></span><br/>  | <span data-ttu-id="a42ed-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a42ed-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="a42ed-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a42ed-128">DefaultValue</span></span><br/> | <span data-ttu-id="a42ed-129">entier</span><span class="sxs-lookup"><span data-stu-id="a42ed-129">integer</span></span><br/> | <span data-ttu-id="a42ed-130">non défini</span><span class="sxs-lookup"><span data-stu-id="a42ed-130">undefined</span></span><br/>       |
| <span data-ttu-id="a42ed-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a42ed-131">MaxValue</span></span><br/>     | <span data-ttu-id="a42ed-132">entier</span><span class="sxs-lookup"><span data-stu-id="a42ed-132">integer</span></span><br/> | <span data-ttu-id="a42ed-133">non défini</span><span class="sxs-lookup"><span data-stu-id="a42ed-133">undefined</span></span><br/>       |
| <span data-ttu-id="a42ed-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="a42ed-134">MinValue</span></span><br/>     | <span data-ttu-id="a42ed-135">entier</span><span class="sxs-lookup"><span data-stu-id="a42ed-135">integer</span></span><br/> | <span data-ttu-id="a42ed-136">non défini</span><span class="sxs-lookup"><span data-stu-id="a42ed-136">undefined</span></span><br/>       |
| <span data-ttu-id="a42ed-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a42ed-137">Mandatory</span></span><br/>    | <span data-ttu-id="a42ed-138">string</span><span class="sxs-lookup"><span data-stu-id="a42ed-138">string</span></span><br/>  | <span data-ttu-id="a42ed-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="a42ed-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a42ed-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="a42ed-140">Multiple</span></span><br/>     | <span data-ttu-id="a42ed-141">integer</span><span class="sxs-lookup"><span data-stu-id="a42ed-141">integer</span></span><br/> | <span data-ttu-id="a42ed-142">1</span><span class="sxs-lookup"><span data-stu-id="a42ed-142">1</span></span><br/>               |
| <span data-ttu-id="a42ed-143">Unité</span><span class="sxs-lookup"><span data-stu-id="a42ed-143">UnitType</span></span><br/>     | <span data-ttu-id="a42ed-144">string</span><span class="sxs-lookup"><span data-stu-id="a42ed-144">string</span></span><br/>  | <span data-ttu-id="a42ed-145">microns</span><span class="sxs-lookup"><span data-stu-id="a42ed-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a42ed-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a42ed-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a42ed-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a42ed-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




