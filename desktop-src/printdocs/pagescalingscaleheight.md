---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d718d80f6b3cc369ddcb5c088a1299d639634b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997476"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="8fc4f-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="8fc4f-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="8fc4f-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="8fc4f-105">This topic is not current.</span></span> <span data-ttu-id="8fc4f-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8fc4f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8fc4f-107">Spécifie le facteur de mise à l’échelle dans la direction ImageableSizeHeight pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8fc4f-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="8fc4f-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8fc4f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8fc4f-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8fc4f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8fc4f-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="8fc4f-110">Element Information</span></span>



| <span data-ttu-id="8fc4f-111">Nom</span><span class="sxs-lookup"><span data-stu-id="8fc4f-111">Name</span></span> | <span data-ttu-id="8fc4f-112">Value</span><span class="sxs-lookup"><span data-stu-id="8fc4f-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="8fc4f-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="8fc4f-113">Element Type</span></span> <br/>   | <span data-ttu-id="8fc4f-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8fc4f-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="8fc4f-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="8fc4f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8fc4f-116">Page</span><span class="sxs-lookup"><span data-stu-id="8fc4f-116">Page</span></span><br/>                                         |
| <span data-ttu-id="8fc4f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8fc4f-117">Notes</span></span> <br/>          | <span data-ttu-id="8fc4f-118">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="8fc4f-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8fc4f-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="8fc4f-119">Structure Content</span></span>

<span data-ttu-id="8fc4f-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="8fc4f-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8fc4f-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="8fc4f-121">Structure Properties</span></span>

<span data-ttu-id="8fc4f-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="8fc4f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8fc4f-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="8fc4f-123">Property</span></span>                | <span data-ttu-id="8fc4f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8fc4f-124">xsi:type</span></span>           | <span data-ttu-id="8fc4f-125">Value</span><span class="sxs-lookup"><span data-stu-id="8fc4f-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8fc4f-126">DataType</span><span class="sxs-lookup"><span data-stu-id="8fc4f-126">DataType</span></span><br/>     | <span data-ttu-id="8fc4f-127">String</span><span class="sxs-lookup"><span data-stu-id="8fc4f-127">String</span></span><br/>  | <span data-ttu-id="8fc4f-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8fc4f-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="8fc4f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8fc4f-129">DefaultValue</span></span><br/> | <span data-ttu-id="8fc4f-130">Integer</span><span class="sxs-lookup"><span data-stu-id="8fc4f-130">Integer</span></span><br/> | <span data-ttu-id="8fc4f-131">non défini</span><span class="sxs-lookup"><span data-stu-id="8fc4f-131">undefined</span></span><br/>       |
| <span data-ttu-id="8fc4f-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8fc4f-132">MaxValue</span></span><br/>     | <span data-ttu-id="8fc4f-133">Integer</span><span class="sxs-lookup"><span data-stu-id="8fc4f-133">Integer</span></span><br/> | <span data-ttu-id="8fc4f-134">non défini</span><span class="sxs-lookup"><span data-stu-id="8fc4f-134">undefined</span></span><br/>       |
| <span data-ttu-id="8fc4f-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="8fc4f-135">MinValue</span></span><br/>     | <span data-ttu-id="8fc4f-136">Integer</span><span class="sxs-lookup"><span data-stu-id="8fc4f-136">Integer</span></span><br/> | <span data-ttu-id="8fc4f-137">1</span><span class="sxs-lookup"><span data-stu-id="8fc4f-137">1</span></span><br/>               |
| <span data-ttu-id="8fc4f-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8fc4f-138">Mandatory</span></span><br/>    | <span data-ttu-id="8fc4f-139">String</span><span class="sxs-lookup"><span data-stu-id="8fc4f-139">String</span></span><br/>  | <span data-ttu-id="8fc4f-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="8fc4f-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8fc4f-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="8fc4f-141">Multiple</span></span><br/>     | <span data-ttu-id="8fc4f-142">Integer</span><span class="sxs-lookup"><span data-stu-id="8fc4f-142">Integer</span></span><br/> | <span data-ttu-id="8fc4f-143">1</span><span class="sxs-lookup"><span data-stu-id="8fc4f-143">1</span></span><br/>               |
| <span data-ttu-id="8fc4f-144">Unité</span><span class="sxs-lookup"><span data-stu-id="8fc4f-144">UnitType</span></span><br/>     | <span data-ttu-id="8fc4f-145">String</span><span class="sxs-lookup"><span data-stu-id="8fc4f-145">String</span></span><br/>  | <span data-ttu-id="8fc4f-146">pour cent</span><span class="sxs-lookup"><span data-stu-id="8fc4f-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8fc4f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fc4f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc4f-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="8fc4f-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




