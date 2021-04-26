---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998376"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="b2dc6-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="b2dc6-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="b2dc6-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b2dc6-105">This topic is not current.</span></span> <span data-ttu-id="b2dc6-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b2dc6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b2dc6-107">Spécifie la largeur de la marge de liaison.</span><span class="sxs-lookup"><span data-stu-id="b2dc6-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="b2dc6-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b2dc6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b2dc6-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b2dc6-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b2dc6-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b2dc6-110">Element Information</span></span>



| <span data-ttu-id="b2dc6-111">Nom</span><span class="sxs-lookup"><span data-stu-id="b2dc6-111">Name</span></span> | <span data-ttu-id="b2dc6-112">Value</span><span class="sxs-lookup"><span data-stu-id="b2dc6-112">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="b2dc6-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b2dc6-113">Element Type</span></span> <br/>   | <span data-ttu-id="b2dc6-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b2dc6-114">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="b2dc6-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b2dc6-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b2dc6-116">Travail</span><span class="sxs-lookup"><span data-stu-id="b2dc6-116">Job</span></span> <br/>                         |
| <span data-ttu-id="b2dc6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b2dc6-117">Notes</span></span> <br/>          | <span data-ttu-id="b2dc6-118">Lié à l’élément JobBinding</span><span class="sxs-lookup"><span data-stu-id="b2dc6-118">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b2dc6-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b2dc6-119">Structure Content</span></span>

<span data-ttu-id="b2dc6-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="b2dc6-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="b2dc6-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="b2dc6-121">Structure Properties</span></span>

<span data-ttu-id="b2dc6-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b2dc6-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b2dc6-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="b2dc6-123">Property</span></span>                | <span data-ttu-id="b2dc6-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b2dc6-124">xsi:type</span></span>           | <span data-ttu-id="b2dc6-125">Value</span><span class="sxs-lookup"><span data-stu-id="b2dc6-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b2dc6-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b2dc6-126">DataType</span></span><br/>     | <span data-ttu-id="b2dc6-127">string</span><span class="sxs-lookup"><span data-stu-id="b2dc6-127">string</span></span><br/>  | <span data-ttu-id="b2dc6-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b2dc6-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="b2dc6-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b2dc6-129">DefaultValue</span></span><br/> | <span data-ttu-id="b2dc6-130">entier</span><span class="sxs-lookup"><span data-stu-id="b2dc6-130">integer</span></span><br/> | <span data-ttu-id="b2dc6-131">non défini</span><span class="sxs-lookup"><span data-stu-id="b2dc6-131">undefined</span></span><br/>       |
| <span data-ttu-id="b2dc6-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b2dc6-132">MaxValue</span></span><br/>     | <span data-ttu-id="b2dc6-133">entier</span><span class="sxs-lookup"><span data-stu-id="b2dc6-133">integer</span></span><br/> | <span data-ttu-id="b2dc6-134">non défini</span><span class="sxs-lookup"><span data-stu-id="b2dc6-134">undefined</span></span><br/>       |
| <span data-ttu-id="b2dc6-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="b2dc6-135">MinValue</span></span><br/>     | <span data-ttu-id="b2dc6-136">entier</span><span class="sxs-lookup"><span data-stu-id="b2dc6-136">integer</span></span><br/> | <span data-ttu-id="b2dc6-137">non défini</span><span class="sxs-lookup"><span data-stu-id="b2dc6-137">undefined</span></span><br/>       |
| <span data-ttu-id="b2dc6-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2dc6-138">Mandatory</span></span><br/>    | <span data-ttu-id="b2dc6-139">String</span><span class="sxs-lookup"><span data-stu-id="b2dc6-139">String</span></span><br/>  | <span data-ttu-id="b2dc6-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="b2dc6-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b2dc6-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="b2dc6-141">Multiple</span></span><br/>     | <span data-ttu-id="b2dc6-142">integer</span><span class="sxs-lookup"><span data-stu-id="b2dc6-142">integer</span></span><br/> | <span data-ttu-id="b2dc6-143">1</span><span class="sxs-lookup"><span data-stu-id="b2dc6-143">1</span></span><br/>               |
| <span data-ttu-id="b2dc6-144">Unité</span><span class="sxs-lookup"><span data-stu-id="b2dc6-144">UnitType</span></span><br/>     | <span data-ttu-id="b2dc6-145">string</span><span class="sxs-lookup"><span data-stu-id="b2dc6-145">string</span></span><br/>  | <span data-ttu-id="b2dc6-146">microns</span><span class="sxs-lookup"><span data-stu-id="b2dc6-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="b2dc6-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2dc6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2dc6-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b2dc6-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




