---
description: Recherchez des informations sur le paramètre DocumentBindingGutter. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118464"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="09933-105">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="09933-105">DocumentBindingGutter</span></span>

<span data-ttu-id="09933-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="09933-106">This topic is not current.</span></span> <span data-ttu-id="09933-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="09933-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="09933-108">Spécifie la largeur de la marge de liaison.</span><span class="sxs-lookup"><span data-stu-id="09933-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="09933-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="09933-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="09933-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="09933-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="09933-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="09933-111">Element Information</span></span>



| <span data-ttu-id="09933-112">Nom</span><span class="sxs-lookup"><span data-stu-id="09933-112">Name</span></span> | <span data-ttu-id="09933-113">Value</span><span class="sxs-lookup"><span data-stu-id="09933-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="09933-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="09933-114">Element Type</span></span> <br/>   | <span data-ttu-id="09933-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="09933-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="09933-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="09933-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="09933-117">Document</span><span class="sxs-lookup"><span data-stu-id="09933-117">Document</span></span><br/>                          |
| <span data-ttu-id="09933-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="09933-118">Notes</span></span> <br/>          | <span data-ttu-id="09933-119">Lié à l’élément DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="09933-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="09933-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="09933-120">Structure Content</span></span>

<span data-ttu-id="09933-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="09933-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="09933-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="09933-122">Structure Properties</span></span>

<span data-ttu-id="09933-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="09933-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="09933-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="09933-124">Property</span></span>                | <span data-ttu-id="09933-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="09933-125">xsi:type</span></span>           | <span data-ttu-id="09933-126">Value</span><span class="sxs-lookup"><span data-stu-id="09933-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="09933-127">DataType</span><span class="sxs-lookup"><span data-stu-id="09933-127">DataType</span></span><br/>     | <span data-ttu-id="09933-128">string</span><span class="sxs-lookup"><span data-stu-id="09933-128">string</span></span><br/>  | <span data-ttu-id="09933-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="09933-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="09933-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="09933-130">DefaultValue</span></span><br/> | <span data-ttu-id="09933-131">entier</span><span class="sxs-lookup"><span data-stu-id="09933-131">integer</span></span><br/> | <span data-ttu-id="09933-132">non défini</span><span class="sxs-lookup"><span data-stu-id="09933-132">undefined</span></span><br/>       |
| <span data-ttu-id="09933-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="09933-133">MaxValue</span></span><br/>     | <span data-ttu-id="09933-134">entier</span><span class="sxs-lookup"><span data-stu-id="09933-134">integer</span></span><br/> | <span data-ttu-id="09933-135">non défini</span><span class="sxs-lookup"><span data-stu-id="09933-135">undefined</span></span><br/>       |
| <span data-ttu-id="09933-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="09933-136">MinValue</span></span><br/>     | <span data-ttu-id="09933-137">entier</span><span class="sxs-lookup"><span data-stu-id="09933-137">integer</span></span><br/> | <span data-ttu-id="09933-138">non défini</span><span class="sxs-lookup"><span data-stu-id="09933-138">undefined</span></span><br/>       |
| <span data-ttu-id="09933-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="09933-139">Mandatory</span></span><br/>    | <span data-ttu-id="09933-140">String</span><span class="sxs-lookup"><span data-stu-id="09933-140">String</span></span><br/>  | <span data-ttu-id="09933-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="09933-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="09933-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="09933-142">Multiple</span></span><br/>     | <span data-ttu-id="09933-143">integer</span><span class="sxs-lookup"><span data-stu-id="09933-143">integer</span></span><br/> | <span data-ttu-id="09933-144">1</span><span class="sxs-lookup"><span data-stu-id="09933-144">1</span></span><br/>               |
| <span data-ttu-id="09933-145">Unité</span><span class="sxs-lookup"><span data-stu-id="09933-145">UnitType</span></span><br/>     | <span data-ttu-id="09933-146">string</span><span class="sxs-lookup"><span data-stu-id="09933-146">string</span></span><br/>  | <span data-ttu-id="09933-147">microns</span><span class="sxs-lookup"><span data-stu-id="09933-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="09933-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09933-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09933-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="09933-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




