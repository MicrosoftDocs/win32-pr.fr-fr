---
description: Obtenir des informations sur le paramètre PageScalingScaleHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51bdb5577b5e3863cfadab1fa9eb74ff40d54da
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548837"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="9efe4-105">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="9efe4-105">PageScalingScaleHeight</span></span>

<span data-ttu-id="9efe4-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9efe4-106">This topic is not current.</span></span> <span data-ttu-id="9efe4-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9efe4-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9efe4-108">Spécifie le facteur de mise à l’échelle dans la direction ImageableSizeHeight pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9efe4-108">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="9efe4-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9efe4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9efe4-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="9efe4-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9efe4-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9efe4-111">Element Information</span></span>



| <span data-ttu-id="9efe4-112">Nom</span><span class="sxs-lookup"><span data-stu-id="9efe4-112">Name</span></span> | <span data-ttu-id="9efe4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9efe4-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="9efe4-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="9efe4-114">Element Type</span></span> <br/>   | <span data-ttu-id="9efe4-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9efe4-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="9efe4-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="9efe4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9efe4-117">Page</span><span class="sxs-lookup"><span data-stu-id="9efe4-117">Page</span></span><br/>                                         |
| <span data-ttu-id="9efe4-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="9efe4-118">Notes</span></span> <br/>          | <span data-ttu-id="9efe4-119">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="9efe4-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9efe4-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="9efe4-120">Structure Content</span></span>

<span data-ttu-id="9efe4-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="9efe4-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9efe4-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="9efe4-122">Structure Properties</span></span>

<span data-ttu-id="9efe4-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="9efe4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9efe4-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="9efe4-124">Property</span></span>                | <span data-ttu-id="9efe4-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9efe4-125">xsi:type</span></span>           | <span data-ttu-id="9efe4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="9efe4-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9efe4-127">DataType</span><span class="sxs-lookup"><span data-stu-id="9efe4-127">DataType</span></span><br/>     | <span data-ttu-id="9efe4-128">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9efe4-128">String</span></span><br/>  | <span data-ttu-id="9efe4-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9efe4-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="9efe4-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9efe4-130">DefaultValue</span></span><br/> | <span data-ttu-id="9efe4-131">Entier</span><span class="sxs-lookup"><span data-stu-id="9efe4-131">Integer</span></span><br/> | <span data-ttu-id="9efe4-132">non défini</span><span class="sxs-lookup"><span data-stu-id="9efe4-132">undefined</span></span><br/>       |
| <span data-ttu-id="9efe4-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9efe4-133">MaxValue</span></span><br/>     | <span data-ttu-id="9efe4-134">Entier</span><span class="sxs-lookup"><span data-stu-id="9efe4-134">Integer</span></span><br/> | <span data-ttu-id="9efe4-135">non défini</span><span class="sxs-lookup"><span data-stu-id="9efe4-135">undefined</span></span><br/>       |
| <span data-ttu-id="9efe4-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="9efe4-136">MinValue</span></span><br/>     | <span data-ttu-id="9efe4-137">Integer</span><span class="sxs-lookup"><span data-stu-id="9efe4-137">Integer</span></span><br/> | <span data-ttu-id="9efe4-138">1</span><span class="sxs-lookup"><span data-stu-id="9efe4-138">1</span></span><br/>               |
| <span data-ttu-id="9efe4-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9efe4-139">Mandatory</span></span><br/>    | <span data-ttu-id="9efe4-140">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9efe4-140">String</span></span><br/>  | <span data-ttu-id="9efe4-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="9efe4-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9efe4-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="9efe4-142">Multiple</span></span><br/>     | <span data-ttu-id="9efe4-143">Integer</span><span class="sxs-lookup"><span data-stu-id="9efe4-143">Integer</span></span><br/> | <span data-ttu-id="9efe4-144">1</span><span class="sxs-lookup"><span data-stu-id="9efe4-144">1</span></span><br/>               |
| <span data-ttu-id="9efe4-145">Unité</span><span class="sxs-lookup"><span data-stu-id="9efe4-145">UnitType</span></span><br/>     | <span data-ttu-id="9efe4-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9efe4-146">String</span></span><br/>  | <span data-ttu-id="9efe4-147">pour cent</span><span class="sxs-lookup"><span data-stu-id="9efe4-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="9efe4-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9efe4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9efe4-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9efe4-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




