---
description: Obtenir des informations sur le paramètre PageScalingScale. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c6cee5fc46568e3cf7f15ecd43c07c6584c856
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548827"
---
# <a name="pagescalingscale"></a><span data-ttu-id="0ba9a-105">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="0ba9a-105">PageScalingScale</span></span>

<span data-ttu-id="0ba9a-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0ba9a-106">This topic is not current.</span></span> <span data-ttu-id="0ba9a-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0ba9a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0ba9a-108">Spécifie le facteur d’échelle pour la mise à l’échelle carrée personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0ba9a-108">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="0ba9a-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0ba9a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0ba9a-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="0ba9a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0ba9a-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0ba9a-111">Element Information</span></span>



| <span data-ttu-id="0ba9a-112">Nom</span><span class="sxs-lookup"><span data-stu-id="0ba9a-112">Name</span></span> | <span data-ttu-id="0ba9a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ba9a-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="0ba9a-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0ba9a-114">Element Type</span></span> <br/>   | <span data-ttu-id="0ba9a-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0ba9a-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="0ba9a-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0ba9a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0ba9a-117">Page</span><span class="sxs-lookup"><span data-stu-id="0ba9a-117">Page</span></span><br/>                                         |
| <span data-ttu-id="0ba9a-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ba9a-118">Notes</span></span> <br/>          | <span data-ttu-id="0ba9a-119">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="0ba9a-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0ba9a-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="0ba9a-120">Structure Content</span></span>

<span data-ttu-id="0ba9a-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0ba9a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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

## <a name="structure-properties"></a><span data-ttu-id="0ba9a-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="0ba9a-122">Structure Properties</span></span>

<span data-ttu-id="0ba9a-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0ba9a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0ba9a-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ba9a-124">Property</span></span>                | <span data-ttu-id="0ba9a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0ba9a-125">xsi:type</span></span>           | <span data-ttu-id="0ba9a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ba9a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0ba9a-127">DataType</span><span class="sxs-lookup"><span data-stu-id="0ba9a-127">DataType</span></span><br/>     | <span data-ttu-id="0ba9a-128">string</span><span class="sxs-lookup"><span data-stu-id="0ba9a-128">string</span></span><br/>  | <span data-ttu-id="0ba9a-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0ba9a-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="0ba9a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0ba9a-130">DefaultValue</span></span><br/> | <span data-ttu-id="0ba9a-131">entier</span><span class="sxs-lookup"><span data-stu-id="0ba9a-131">integer</span></span><br/> | <span data-ttu-id="0ba9a-132">non défini</span><span class="sxs-lookup"><span data-stu-id="0ba9a-132">undefined</span></span><br/>       |
| <span data-ttu-id="0ba9a-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0ba9a-133">MaxValue</span></span><br/>     | <span data-ttu-id="0ba9a-134">entier</span><span class="sxs-lookup"><span data-stu-id="0ba9a-134">integer</span></span><br/> | <span data-ttu-id="0ba9a-135">non défini</span><span class="sxs-lookup"><span data-stu-id="0ba9a-135">undefined</span></span><br/>       |
| <span data-ttu-id="0ba9a-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="0ba9a-136">MinValue</span></span><br/>     | <span data-ttu-id="0ba9a-137">integer</span><span class="sxs-lookup"><span data-stu-id="0ba9a-137">integer</span></span><br/> | <span data-ttu-id="0ba9a-138">1</span><span class="sxs-lookup"><span data-stu-id="0ba9a-138">1</span></span><br/>               |
| <span data-ttu-id="0ba9a-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0ba9a-139">Mandatory</span></span><br/>    | <span data-ttu-id="0ba9a-140">string</span><span class="sxs-lookup"><span data-stu-id="0ba9a-140">string</span></span><br/>  | <span data-ttu-id="0ba9a-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="0ba9a-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0ba9a-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="0ba9a-142">Multiple</span></span><br/>     | <span data-ttu-id="0ba9a-143">integer</span><span class="sxs-lookup"><span data-stu-id="0ba9a-143">integer</span></span><br/> | <span data-ttu-id="0ba9a-144">1</span><span class="sxs-lookup"><span data-stu-id="0ba9a-144">1</span></span><br/>               |
| <span data-ttu-id="0ba9a-145">Unité</span><span class="sxs-lookup"><span data-stu-id="0ba9a-145">UnitType</span></span><br/>     | <span data-ttu-id="0ba9a-146">string</span><span class="sxs-lookup"><span data-stu-id="0ba9a-146">string</span></span><br/>  | <span data-ttu-id="0ba9a-147">pour cent</span><span class="sxs-lookup"><span data-stu-id="0ba9a-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0ba9a-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ba9a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ba9a-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0ba9a-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




