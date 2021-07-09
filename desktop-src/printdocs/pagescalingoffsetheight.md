---
description: Obtenir des informations sur le paramètre PageScalingOffsetHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f02370d28716dd3a8840001959bb7d963307d2f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548957"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="bf9a1-105">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="bf9a1-105">PageScalingOffsetHeight</span></span>

<span data-ttu-id="bf9a1-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-106">This topic is not current.</span></span> <span data-ttu-id="bf9a1-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bf9a1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bf9a1-108">Spécifie le décalage de mise à l’échelle dans la direction ImageableSizeHeight pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-108">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="bf9a1-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bf9a1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bf9a1-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="bf9a1-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bf9a1-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bf9a1-111">Element Information</span></span>



| <span data-ttu-id="bf9a1-112">Nom</span><span class="sxs-lookup"><span data-stu-id="bf9a1-112">Name</span></span> | <span data-ttu-id="bf9a1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf9a1-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="bf9a1-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="bf9a1-114">Element Type</span></span> <br/>   | <span data-ttu-id="bf9a1-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bf9a1-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="bf9a1-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="bf9a1-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bf9a1-117">Page</span><span class="sxs-lookup"><span data-stu-id="bf9a1-117">Page</span></span><br/>                                         |
| <span data-ttu-id="bf9a1-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf9a1-118">Notes</span></span> <br/>          | <span data-ttu-id="bf9a1-119">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="bf9a1-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bf9a1-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="bf9a1-120">Structure Content</span></span>

<span data-ttu-id="bf9a1-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="bf9a1-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="bf9a1-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="bf9a1-122">Structure Properties</span></span>

<span data-ttu-id="bf9a1-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="bf9a1-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bf9a1-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="bf9a1-124">Property</span></span>                | <span data-ttu-id="bf9a1-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bf9a1-125">xsi:type</span></span>           | <span data-ttu-id="bf9a1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf9a1-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="bf9a1-127">DataType</span><span class="sxs-lookup"><span data-stu-id="bf9a1-127">DataType</span></span><br/>     | <span data-ttu-id="bf9a1-128">string</span><span class="sxs-lookup"><span data-stu-id="bf9a1-128">string</span></span><br/>  | <span data-ttu-id="bf9a1-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bf9a1-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="bf9a1-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bf9a1-130">DefaultValue</span></span><br/> | <span data-ttu-id="bf9a1-131">entier</span><span class="sxs-lookup"><span data-stu-id="bf9a1-131">integer</span></span><br/> | <span data-ttu-id="bf9a1-132">non défini</span><span class="sxs-lookup"><span data-stu-id="bf9a1-132">undefined</span></span><br/>       |
| <span data-ttu-id="bf9a1-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bf9a1-133">MaxValue</span></span><br/>     | <span data-ttu-id="bf9a1-134">entier</span><span class="sxs-lookup"><span data-stu-id="bf9a1-134">integer</span></span><br/> | <span data-ttu-id="bf9a1-135">non défini</span><span class="sxs-lookup"><span data-stu-id="bf9a1-135">undefined</span></span><br/>       |
| <span data-ttu-id="bf9a1-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="bf9a1-136">MinValue</span></span><br/>     | <span data-ttu-id="bf9a1-137">entier</span><span class="sxs-lookup"><span data-stu-id="bf9a1-137">integer</span></span><br/> | <span data-ttu-id="bf9a1-138">non défini</span><span class="sxs-lookup"><span data-stu-id="bf9a1-138">undefined</span></span><br/>       |
| <span data-ttu-id="bf9a1-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bf9a1-139">Mandatory</span></span><br/>    | <span data-ttu-id="bf9a1-140">string</span><span class="sxs-lookup"><span data-stu-id="bf9a1-140">string</span></span><br/>  | <span data-ttu-id="bf9a1-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="bf9a1-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="bf9a1-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="bf9a1-142">Multiple</span></span><br/>     | <span data-ttu-id="bf9a1-143">integer</span><span class="sxs-lookup"><span data-stu-id="bf9a1-143">integer</span></span><br/> | <span data-ttu-id="bf9a1-144">1</span><span class="sxs-lookup"><span data-stu-id="bf9a1-144">1</span></span><br/>               |
| <span data-ttu-id="bf9a1-145">Unité</span><span class="sxs-lookup"><span data-stu-id="bf9a1-145">UnitType</span></span><br/>     | <span data-ttu-id="bf9a1-146">string</span><span class="sxs-lookup"><span data-stu-id="bf9a1-146">string</span></span><br/>  | <span data-ttu-id="bf9a1-147">microns</span><span class="sxs-lookup"><span data-stu-id="bf9a1-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="bf9a1-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf9a1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9a1-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="bf9a1-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




