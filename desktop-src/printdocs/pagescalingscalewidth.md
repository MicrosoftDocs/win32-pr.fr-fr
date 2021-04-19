---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7918f1a466621377e57190e0b967980fec1a07e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106537188"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="f9dd0-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="f9dd0-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="f9dd0-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="f9dd0-105">This topic is not current.</span></span> <span data-ttu-id="f9dd0-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f9dd0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f9dd0-107">Spécifie le facteur de mise à l’échelle dans la direction ImageableSizeWidth pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f9dd0-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="f9dd0-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f9dd0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f9dd0-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f9dd0-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f9dd0-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f9dd0-110">Element Information</span></span>



| <span data-ttu-id="f9dd0-111">Nom</span><span class="sxs-lookup"><span data-stu-id="f9dd0-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="f9dd0-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="f9dd0-112">Element Type</span></span> <br/>   | <span data-ttu-id="f9dd0-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f9dd0-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="f9dd0-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="f9dd0-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f9dd0-115">Page</span><span class="sxs-lookup"><span data-stu-id="f9dd0-115">Page</span></span><br/>                                         |
| <span data-ttu-id="f9dd0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f9dd0-116">Notes</span></span> <br/>          | <span data-ttu-id="f9dd0-117">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="f9dd0-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f9dd0-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f9dd0-118">Structure Content</span></span>

<span data-ttu-id="f9dd0-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="f9dd0-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="f9dd0-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="f9dd0-120">Structure Properties</span></span>

<span data-ttu-id="f9dd0-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="f9dd0-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f9dd0-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="f9dd0-122">Property</span></span>                | <span data-ttu-id="f9dd0-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f9dd0-123">xsi:type</span></span>           | <span data-ttu-id="f9dd0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9dd0-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f9dd0-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f9dd0-125">DataType</span></span><br/>     | <span data-ttu-id="f9dd0-126">String</span><span class="sxs-lookup"><span data-stu-id="f9dd0-126">String</span></span><br/>  | <span data-ttu-id="f9dd0-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f9dd0-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f9dd0-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f9dd0-128">DefaultValue</span></span><br/> | <span data-ttu-id="f9dd0-129">Integer</span><span class="sxs-lookup"><span data-stu-id="f9dd0-129">Integer</span></span><br/> | <span data-ttu-id="f9dd0-130">non défini</span><span class="sxs-lookup"><span data-stu-id="f9dd0-130">undefined</span></span><br/>       |
| <span data-ttu-id="f9dd0-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f9dd0-131">MaxValue</span></span><br/>     | <span data-ttu-id="f9dd0-132">Integer</span><span class="sxs-lookup"><span data-stu-id="f9dd0-132">Integer</span></span><br/> | <span data-ttu-id="f9dd0-133">non défini</span><span class="sxs-lookup"><span data-stu-id="f9dd0-133">undefined</span></span><br/>       |
| <span data-ttu-id="f9dd0-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f9dd0-134">MinValue</span></span><br/>     | <span data-ttu-id="f9dd0-135">Integer</span><span class="sxs-lookup"><span data-stu-id="f9dd0-135">Integer</span></span><br/> | <span data-ttu-id="f9dd0-136">1</span><span class="sxs-lookup"><span data-stu-id="f9dd0-136">1</span></span><br/>               |
| <span data-ttu-id="f9dd0-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9dd0-137">Mandatory</span></span><br/>    | <span data-ttu-id="f9dd0-138">String</span><span class="sxs-lookup"><span data-stu-id="f9dd0-138">String</span></span><br/>  | <span data-ttu-id="f9dd0-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="f9dd0-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f9dd0-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="f9dd0-140">Multiple</span></span><br/>     | <span data-ttu-id="f9dd0-141">Integer</span><span class="sxs-lookup"><span data-stu-id="f9dd0-141">Integer</span></span><br/> | <span data-ttu-id="f9dd0-142">1</span><span class="sxs-lookup"><span data-stu-id="f9dd0-142">1</span></span><br/>               |
| <span data-ttu-id="f9dd0-143">Unité</span><span class="sxs-lookup"><span data-stu-id="f9dd0-143">UnitType</span></span><br/>     | <span data-ttu-id="f9dd0-144">String</span><span class="sxs-lookup"><span data-stu-id="f9dd0-144">String</span></span><br/>  | <span data-ttu-id="f9dd0-145">microns</span><span class="sxs-lookup"><span data-stu-id="f9dd0-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f9dd0-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9dd0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9dd0-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f9dd0-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




