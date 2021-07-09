---
description: Obtenir des informations sur le paramètre PageScalingOffsetWidth. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63152e6a3d9f8ea47bac3b5a0efe559e71e0cb35
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548847"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="3d990-105">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="3d990-105">PageScalingOffsetWidth</span></span>

<span data-ttu-id="3d990-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="3d990-106">This topic is not current.</span></span> <span data-ttu-id="3d990-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3d990-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3d990-108">Spécifie le décalage de mise à l’échelle dans la direction ImageableSizeWidth pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3d990-108">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="3d990-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3d990-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3d990-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="3d990-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3d990-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3d990-111">Element Information</span></span>



| <span data-ttu-id="3d990-112">Nom</span><span class="sxs-lookup"><span data-stu-id="3d990-112">Name</span></span> | <span data-ttu-id="3d990-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d990-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d990-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="3d990-114">Element Type</span></span> <br/>   | <span data-ttu-id="3d990-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3d990-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="3d990-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="3d990-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3d990-117">Page</span><span class="sxs-lookup"><span data-stu-id="3d990-117">Page</span></span><br/>                                         |
| <span data-ttu-id="3d990-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d990-118">Notes</span></span> <br/>          | <span data-ttu-id="3d990-119">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="3d990-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3d990-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="3d990-120">Structure Content</span></span>

<span data-ttu-id="3d990-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="3d990-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3d990-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="3d990-122">Structure Properties</span></span>

<span data-ttu-id="3d990-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="3d990-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3d990-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="3d990-124">Property</span></span>                | <span data-ttu-id="3d990-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3d990-125">xsi:type</span></span>           | <span data-ttu-id="3d990-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d990-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3d990-127">DataType</span><span class="sxs-lookup"><span data-stu-id="3d990-127">DataType</span></span><br/>     | <span data-ttu-id="3d990-128">string</span><span class="sxs-lookup"><span data-stu-id="3d990-128">string</span></span><br/>  | <span data-ttu-id="3d990-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3d990-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="3d990-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3d990-130">DefaultValue</span></span><br/> | <span data-ttu-id="3d990-131">entier</span><span class="sxs-lookup"><span data-stu-id="3d990-131">integer</span></span><br/> | <span data-ttu-id="3d990-132">non défini</span><span class="sxs-lookup"><span data-stu-id="3d990-132">undefined</span></span><br/>       |
| <span data-ttu-id="3d990-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3d990-133">MaxValue</span></span><br/>     | <span data-ttu-id="3d990-134">entier</span><span class="sxs-lookup"><span data-stu-id="3d990-134">integer</span></span><br/> | <span data-ttu-id="3d990-135">non défini</span><span class="sxs-lookup"><span data-stu-id="3d990-135">undefined</span></span><br/>       |
| <span data-ttu-id="3d990-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="3d990-136">MinValue</span></span><br/>     | <span data-ttu-id="3d990-137">entier</span><span class="sxs-lookup"><span data-stu-id="3d990-137">integer</span></span><br/> | <span data-ttu-id="3d990-138">non défini</span><span class="sxs-lookup"><span data-stu-id="3d990-138">undefined</span></span><br/>       |
| <span data-ttu-id="3d990-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d990-139">Mandatory</span></span><br/>    | <span data-ttu-id="3d990-140">string</span><span class="sxs-lookup"><span data-stu-id="3d990-140">string</span></span><br/>  | <span data-ttu-id="3d990-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="3d990-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3d990-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="3d990-142">Multiple</span></span><br/>     | <span data-ttu-id="3d990-143">integer</span><span class="sxs-lookup"><span data-stu-id="3d990-143">integer</span></span><br/> | <span data-ttu-id="3d990-144">1</span><span class="sxs-lookup"><span data-stu-id="3d990-144">1</span></span><br/>               |
| <span data-ttu-id="3d990-145">Unité</span><span class="sxs-lookup"><span data-stu-id="3d990-145">UnitType</span></span><br/>     | <span data-ttu-id="3d990-146">string</span><span class="sxs-lookup"><span data-stu-id="3d990-146">string</span></span><br/>  | <span data-ttu-id="3d990-147">microns</span><span class="sxs-lookup"><span data-stu-id="3d990-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="3d990-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d990-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d990-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3d990-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




