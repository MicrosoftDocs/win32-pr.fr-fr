---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3f91f6b188dadbd86a18152be5228b62d21ab4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522518"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="3a53e-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="3a53e-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="3a53e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="3a53e-105">This topic is not current.</span></span> <span data-ttu-id="3a53e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3a53e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3a53e-107">Spécifie le facteur de mise à l’échelle dans la direction ImageableSizeHeight pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3a53e-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="3a53e-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3a53e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3a53e-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="3a53e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3a53e-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3a53e-110">Element Information</span></span>



| <span data-ttu-id="3a53e-111">Nom</span><span class="sxs-lookup"><span data-stu-id="3a53e-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="3a53e-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="3a53e-112">Element Type</span></span> <br/>   | <span data-ttu-id="3a53e-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3a53e-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="3a53e-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="3a53e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3a53e-115">Page</span><span class="sxs-lookup"><span data-stu-id="3a53e-115">Page</span></span><br/>                                         |
| <span data-ttu-id="3a53e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3a53e-116">Notes</span></span> <br/>          | <span data-ttu-id="3a53e-117">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="3a53e-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3a53e-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="3a53e-118">Structure Content</span></span>

<span data-ttu-id="3a53e-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="3a53e-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="3a53e-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="3a53e-120">Structure Properties</span></span>

<span data-ttu-id="3a53e-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="3a53e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3a53e-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="3a53e-122">Property</span></span>                | <span data-ttu-id="3a53e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3a53e-123">xsi:type</span></span>           | <span data-ttu-id="3a53e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a53e-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3a53e-125">DataType</span><span class="sxs-lookup"><span data-stu-id="3a53e-125">DataType</span></span><br/>     | <span data-ttu-id="3a53e-126">String</span><span class="sxs-lookup"><span data-stu-id="3a53e-126">String</span></span><br/>  | <span data-ttu-id="3a53e-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3a53e-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="3a53e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3a53e-128">DefaultValue</span></span><br/> | <span data-ttu-id="3a53e-129">Integer</span><span class="sxs-lookup"><span data-stu-id="3a53e-129">Integer</span></span><br/> | <span data-ttu-id="3a53e-130">non défini</span><span class="sxs-lookup"><span data-stu-id="3a53e-130">undefined</span></span><br/>       |
| <span data-ttu-id="3a53e-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3a53e-131">MaxValue</span></span><br/>     | <span data-ttu-id="3a53e-132">Integer</span><span class="sxs-lookup"><span data-stu-id="3a53e-132">Integer</span></span><br/> | <span data-ttu-id="3a53e-133">non défini</span><span class="sxs-lookup"><span data-stu-id="3a53e-133">undefined</span></span><br/>       |
| <span data-ttu-id="3a53e-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="3a53e-134">MinValue</span></span><br/>     | <span data-ttu-id="3a53e-135">Integer</span><span class="sxs-lookup"><span data-stu-id="3a53e-135">Integer</span></span><br/> | <span data-ttu-id="3a53e-136">1</span><span class="sxs-lookup"><span data-stu-id="3a53e-136">1</span></span><br/>               |
| <span data-ttu-id="3a53e-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3a53e-137">Mandatory</span></span><br/>    | <span data-ttu-id="3a53e-138">String</span><span class="sxs-lookup"><span data-stu-id="3a53e-138">String</span></span><br/>  | <span data-ttu-id="3a53e-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="3a53e-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3a53e-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="3a53e-140">Multiple</span></span><br/>     | <span data-ttu-id="3a53e-141">Integer</span><span class="sxs-lookup"><span data-stu-id="3a53e-141">Integer</span></span><br/> | <span data-ttu-id="3a53e-142">1</span><span class="sxs-lookup"><span data-stu-id="3a53e-142">1</span></span><br/>               |
| <span data-ttu-id="3a53e-143">Unité</span><span class="sxs-lookup"><span data-stu-id="3a53e-143">UnitType</span></span><br/>     | <span data-ttu-id="3a53e-144">String</span><span class="sxs-lookup"><span data-stu-id="3a53e-144">String</span></span><br/>  | <span data-ttu-id="3a53e-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="3a53e-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="3a53e-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a53e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a53e-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3a53e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




