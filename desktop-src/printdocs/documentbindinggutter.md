---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf00f146373502564d559d00f66dedd24abf5b9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211331"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="5a5b8-104">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="5a5b8-104">DocumentBindingGutter</span></span>

<span data-ttu-id="5a5b8-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-105">This topic is not current.</span></span> <span data-ttu-id="5a5b8-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a5b8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a5b8-107">Spécifie la largeur de la marge de liaison.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="5a5b8-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5a5b8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5a5b8-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="5a5b8-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5a5b8-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5a5b8-110">Element Information</span></span>



| <span data-ttu-id="5a5b8-111">Nom</span><span class="sxs-lookup"><span data-stu-id="5a5b8-111">Name</span></span>                       |                                              |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="5a5b8-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="5a5b8-112">Element Type</span></span> <br/>   | <span data-ttu-id="5a5b8-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5a5b8-113">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="5a5b8-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="5a5b8-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a5b8-115">Document</span><span class="sxs-lookup"><span data-stu-id="5a5b8-115">Document</span></span><br/>                          |
| <span data-ttu-id="5a5b8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5a5b8-116">Notes</span></span> <br/>          | <span data-ttu-id="5a5b8-117">Lié à l’élément DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="5a5b8-117">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5a5b8-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="5a5b8-118">Structure Content</span></span>

<span data-ttu-id="5a5b8-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="5a5b8-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5a5b8-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="5a5b8-120">Structure Properties</span></span>

<span data-ttu-id="5a5b8-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="5a5b8-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a5b8-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="5a5b8-122">Property</span></span>                | <span data-ttu-id="5a5b8-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5a5b8-123">xsi:type</span></span>           | <span data-ttu-id="5a5b8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a5b8-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5a5b8-125">DataType</span><span class="sxs-lookup"><span data-stu-id="5a5b8-125">DataType</span></span><br/>     | <span data-ttu-id="5a5b8-126">string</span><span class="sxs-lookup"><span data-stu-id="5a5b8-126">string</span></span><br/>  | <span data-ttu-id="5a5b8-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a5b8-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="5a5b8-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5a5b8-128">DefaultValue</span></span><br/> | <span data-ttu-id="5a5b8-129">entier</span><span class="sxs-lookup"><span data-stu-id="5a5b8-129">integer</span></span><br/> | <span data-ttu-id="5a5b8-130">non défini</span><span class="sxs-lookup"><span data-stu-id="5a5b8-130">undefined</span></span><br/>       |
| <span data-ttu-id="5a5b8-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5a5b8-131">MaxValue</span></span><br/>     | <span data-ttu-id="5a5b8-132">entier</span><span class="sxs-lookup"><span data-stu-id="5a5b8-132">integer</span></span><br/> | <span data-ttu-id="5a5b8-133">non défini</span><span class="sxs-lookup"><span data-stu-id="5a5b8-133">undefined</span></span><br/>       |
| <span data-ttu-id="5a5b8-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="5a5b8-134">MinValue</span></span><br/>     | <span data-ttu-id="5a5b8-135">entier</span><span class="sxs-lookup"><span data-stu-id="5a5b8-135">integer</span></span><br/> | <span data-ttu-id="5a5b8-136">non défini</span><span class="sxs-lookup"><span data-stu-id="5a5b8-136">undefined</span></span><br/>       |
| <span data-ttu-id="5a5b8-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5a5b8-137">Mandatory</span></span><br/>    | <span data-ttu-id="5a5b8-138">String</span><span class="sxs-lookup"><span data-stu-id="5a5b8-138">String</span></span><br/>  | <span data-ttu-id="5a5b8-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="5a5b8-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5a5b8-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="5a5b8-140">Multiple</span></span><br/>     | <span data-ttu-id="5a5b8-141">integer</span><span class="sxs-lookup"><span data-stu-id="5a5b8-141">integer</span></span><br/> | <span data-ttu-id="5a5b8-142">1</span><span class="sxs-lookup"><span data-stu-id="5a5b8-142">1</span></span><br/>               |
| <span data-ttu-id="5a5b8-143">Unité</span><span class="sxs-lookup"><span data-stu-id="5a5b8-143">UnitType</span></span><br/>     | <span data-ttu-id="5a5b8-144">string</span><span class="sxs-lookup"><span data-stu-id="5a5b8-144">string</span></span><br/>  | <span data-ttu-id="5a5b8-145">microns</span><span class="sxs-lookup"><span data-stu-id="5a5b8-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5a5b8-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a5b8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a5b8-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="5a5b8-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




