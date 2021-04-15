---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393871"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="deace-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="deace-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="deace-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="deace-105">This topic is not current.</span></span> <span data-ttu-id="deace-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="deace-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="deace-107">Spécifie le décalage de mise à l’échelle dans la direction ImageableSizeHeight pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="deace-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="deace-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="deace-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="deace-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="deace-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="deace-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="deace-110">Element Information</span></span>



| <span data-ttu-id="deace-111">Nom</span><span class="sxs-lookup"><span data-stu-id="deace-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="deace-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="deace-112">Element Type</span></span> <br/>   | <span data-ttu-id="deace-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="deace-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="deace-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="deace-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="deace-115">Page</span><span class="sxs-lookup"><span data-stu-id="deace-115">Page</span></span><br/>                                         |
| <span data-ttu-id="deace-116">Notes</span><span class="sxs-lookup"><span data-stu-id="deace-116">Notes</span></span> <br/>          | <span data-ttu-id="deace-117">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="deace-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="deace-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="deace-118">Structure Content</span></span>

<span data-ttu-id="deace-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="deace-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="deace-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="deace-120">Structure Properties</span></span>

<span data-ttu-id="deace-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="deace-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="deace-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="deace-122">Property</span></span>                | <span data-ttu-id="deace-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="deace-123">xsi:type</span></span>           | <span data-ttu-id="deace-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="deace-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="deace-125">DataType</span><span class="sxs-lookup"><span data-stu-id="deace-125">DataType</span></span><br/>     | <span data-ttu-id="deace-126">string</span><span class="sxs-lookup"><span data-stu-id="deace-126">string</span></span><br/>  | <span data-ttu-id="deace-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="deace-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="deace-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="deace-128">DefaultValue</span></span><br/> | <span data-ttu-id="deace-129">entier</span><span class="sxs-lookup"><span data-stu-id="deace-129">integer</span></span><br/> | <span data-ttu-id="deace-130">non défini</span><span class="sxs-lookup"><span data-stu-id="deace-130">undefined</span></span><br/>       |
| <span data-ttu-id="deace-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="deace-131">MaxValue</span></span><br/>     | <span data-ttu-id="deace-132">entier</span><span class="sxs-lookup"><span data-stu-id="deace-132">integer</span></span><br/> | <span data-ttu-id="deace-133">non défini</span><span class="sxs-lookup"><span data-stu-id="deace-133">undefined</span></span><br/>       |
| <span data-ttu-id="deace-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="deace-134">MinValue</span></span><br/>     | <span data-ttu-id="deace-135">entier</span><span class="sxs-lookup"><span data-stu-id="deace-135">integer</span></span><br/> | <span data-ttu-id="deace-136">non défini</span><span class="sxs-lookup"><span data-stu-id="deace-136">undefined</span></span><br/>       |
| <span data-ttu-id="deace-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="deace-137">Mandatory</span></span><br/>    | <span data-ttu-id="deace-138">string</span><span class="sxs-lookup"><span data-stu-id="deace-138">string</span></span><br/>  | <span data-ttu-id="deace-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="deace-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="deace-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="deace-140">Multiple</span></span><br/>     | <span data-ttu-id="deace-141">integer</span><span class="sxs-lookup"><span data-stu-id="deace-141">integer</span></span><br/> | <span data-ttu-id="deace-142">1</span><span class="sxs-lookup"><span data-stu-id="deace-142">1</span></span><br/>               |
| <span data-ttu-id="deace-143">Unité</span><span class="sxs-lookup"><span data-stu-id="deace-143">UnitType</span></span><br/>     | <span data-ttu-id="deace-144">string</span><span class="sxs-lookup"><span data-stu-id="deace-144">string</span></span><br/>  | <span data-ttu-id="deace-145">microns</span><span class="sxs-lookup"><span data-stu-id="deace-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="deace-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="deace-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deace-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="deace-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




