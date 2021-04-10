---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219a86f016edf820532c20fa473876265776a4ee
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211330"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="7db02-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="7db02-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="7db02-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7db02-105">This topic is not current.</span></span> <span data-ttu-id="7db02-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7db02-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7db02-107">Spécifie la largeur de la marge de liaison.</span><span class="sxs-lookup"><span data-stu-id="7db02-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="7db02-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7db02-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7db02-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="7db02-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7db02-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7db02-110">Element Information</span></span>



| <span data-ttu-id="7db02-111">Nom</span><span class="sxs-lookup"><span data-stu-id="7db02-111">Name</span></span>                       |                                         |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="7db02-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7db02-112">Element Type</span></span> <br/>   | <span data-ttu-id="7db02-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7db02-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="7db02-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="7db02-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7db02-115">Travail</span><span class="sxs-lookup"><span data-stu-id="7db02-115">Job</span></span> <br/>                         |
| <span data-ttu-id="7db02-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7db02-116">Notes</span></span> <br/>          | <span data-ttu-id="7db02-117">Lié à l’élément JobBinding</span><span class="sxs-lookup"><span data-stu-id="7db02-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7db02-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="7db02-118">Structure Content</span></span>

<span data-ttu-id="7db02-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="7db02-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7db02-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="7db02-120">Structure Properties</span></span>

<span data-ttu-id="7db02-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="7db02-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7db02-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="7db02-122">Property</span></span>                | <span data-ttu-id="7db02-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7db02-123">xsi:type</span></span>           | <span data-ttu-id="7db02-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7db02-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7db02-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7db02-125">DataType</span></span><br/>     | <span data-ttu-id="7db02-126">string</span><span class="sxs-lookup"><span data-stu-id="7db02-126">string</span></span><br/>  | <span data-ttu-id="7db02-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7db02-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="7db02-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7db02-128">DefaultValue</span></span><br/> | <span data-ttu-id="7db02-129">entier</span><span class="sxs-lookup"><span data-stu-id="7db02-129">integer</span></span><br/> | <span data-ttu-id="7db02-130">non défini</span><span class="sxs-lookup"><span data-stu-id="7db02-130">undefined</span></span><br/>       |
| <span data-ttu-id="7db02-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7db02-131">MaxValue</span></span><br/>     | <span data-ttu-id="7db02-132">entier</span><span class="sxs-lookup"><span data-stu-id="7db02-132">integer</span></span><br/> | <span data-ttu-id="7db02-133">non défini</span><span class="sxs-lookup"><span data-stu-id="7db02-133">undefined</span></span><br/>       |
| <span data-ttu-id="7db02-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7db02-134">MinValue</span></span><br/>     | <span data-ttu-id="7db02-135">entier</span><span class="sxs-lookup"><span data-stu-id="7db02-135">integer</span></span><br/> | <span data-ttu-id="7db02-136">non défini</span><span class="sxs-lookup"><span data-stu-id="7db02-136">undefined</span></span><br/>       |
| <span data-ttu-id="7db02-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7db02-137">Mandatory</span></span><br/>    | <span data-ttu-id="7db02-138">String</span><span class="sxs-lookup"><span data-stu-id="7db02-138">String</span></span><br/>  | <span data-ttu-id="7db02-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="7db02-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7db02-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="7db02-140">Multiple</span></span><br/>     | <span data-ttu-id="7db02-141">integer</span><span class="sxs-lookup"><span data-stu-id="7db02-141">integer</span></span><br/> | <span data-ttu-id="7db02-142">1</span><span class="sxs-lookup"><span data-stu-id="7db02-142">1</span></span><br/>               |
| <span data-ttu-id="7db02-143">Unité</span><span class="sxs-lookup"><span data-stu-id="7db02-143">UnitType</span></span><br/>     | <span data-ttu-id="7db02-144">string</span><span class="sxs-lookup"><span data-stu-id="7db02-144">string</span></span><br/>  | <span data-ttu-id="7db02-145">microns</span><span class="sxs-lookup"><span data-stu-id="7db02-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7db02-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7db02-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7db02-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7db02-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




