---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2372636ea22610e6a209cfad3f1fe6297be34833
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997186"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="fc745-104">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="fc745-104">DocumentBindingGutter</span></span>

<span data-ttu-id="fc745-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="fc745-105">This topic is not current.</span></span> <span data-ttu-id="fc745-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fc745-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fc745-107">Spécifie la largeur de la marge de liaison.</span><span class="sxs-lookup"><span data-stu-id="fc745-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="fc745-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fc745-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fc745-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="fc745-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fc745-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fc745-110">Element Information</span></span>



| <span data-ttu-id="fc745-111">Nom</span><span class="sxs-lookup"><span data-stu-id="fc745-111">Name</span></span> | <span data-ttu-id="fc745-112">Value</span><span class="sxs-lookup"><span data-stu-id="fc745-112">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="fc745-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="fc745-113">Element Type</span></span> <br/>   | <span data-ttu-id="fc745-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fc745-114">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="fc745-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="fc745-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fc745-116">Document</span><span class="sxs-lookup"><span data-stu-id="fc745-116">Document</span></span><br/>                          |
| <span data-ttu-id="fc745-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fc745-117">Notes</span></span> <br/>          | <span data-ttu-id="fc745-118">Lié à l’élément DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="fc745-118">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fc745-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="fc745-119">Structure Content</span></span>

<span data-ttu-id="fc745-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="fc745-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="fc745-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="fc745-121">Structure Properties</span></span>

<span data-ttu-id="fc745-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="fc745-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fc745-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="fc745-123">Property</span></span>                | <span data-ttu-id="fc745-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fc745-124">xsi:type</span></span>           | <span data-ttu-id="fc745-125">Value</span><span class="sxs-lookup"><span data-stu-id="fc745-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fc745-126">DataType</span><span class="sxs-lookup"><span data-stu-id="fc745-126">DataType</span></span><br/>     | <span data-ttu-id="fc745-127">string</span><span class="sxs-lookup"><span data-stu-id="fc745-127">string</span></span><br/>  | <span data-ttu-id="fc745-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fc745-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="fc745-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fc745-129">DefaultValue</span></span><br/> | <span data-ttu-id="fc745-130">entier</span><span class="sxs-lookup"><span data-stu-id="fc745-130">integer</span></span><br/> | <span data-ttu-id="fc745-131">non défini</span><span class="sxs-lookup"><span data-stu-id="fc745-131">undefined</span></span><br/>       |
| <span data-ttu-id="fc745-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fc745-132">MaxValue</span></span><br/>     | <span data-ttu-id="fc745-133">entier</span><span class="sxs-lookup"><span data-stu-id="fc745-133">integer</span></span><br/> | <span data-ttu-id="fc745-134">non défini</span><span class="sxs-lookup"><span data-stu-id="fc745-134">undefined</span></span><br/>       |
| <span data-ttu-id="fc745-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="fc745-135">MinValue</span></span><br/>     | <span data-ttu-id="fc745-136">entier</span><span class="sxs-lookup"><span data-stu-id="fc745-136">integer</span></span><br/> | <span data-ttu-id="fc745-137">non défini</span><span class="sxs-lookup"><span data-stu-id="fc745-137">undefined</span></span><br/>       |
| <span data-ttu-id="fc745-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fc745-138">Mandatory</span></span><br/>    | <span data-ttu-id="fc745-139">String</span><span class="sxs-lookup"><span data-stu-id="fc745-139">String</span></span><br/>  | <span data-ttu-id="fc745-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="fc745-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fc745-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="fc745-141">Multiple</span></span><br/>     | <span data-ttu-id="fc745-142">integer</span><span class="sxs-lookup"><span data-stu-id="fc745-142">integer</span></span><br/> | <span data-ttu-id="fc745-143">1</span><span class="sxs-lookup"><span data-stu-id="fc745-143">1</span></span><br/>               |
| <span data-ttu-id="fc745-144">Unité</span><span class="sxs-lookup"><span data-stu-id="fc745-144">UnitType</span></span><br/>     | <span data-ttu-id="fc745-145">string</span><span class="sxs-lookup"><span data-stu-id="fc745-145">string</span></span><br/>  | <span data-ttu-id="fc745-146">microns</span><span class="sxs-lookup"><span data-stu-id="fc745-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fc745-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc745-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc745-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="fc745-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




