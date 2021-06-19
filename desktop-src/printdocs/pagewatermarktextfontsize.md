---
description: Obtenir des informations sur le paramètre PageWatermarkTextFontSize. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395994"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="59f28-105">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="59f28-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="59f28-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="59f28-106">This topic is not current.</span></span> <span data-ttu-id="59f28-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="59f28-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="59f28-108">Définit les tailles de police disponibles pour le texte de filigrane.</span><span class="sxs-lookup"><span data-stu-id="59f28-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="59f28-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="59f28-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="59f28-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="59f28-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="59f28-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="59f28-111">Element Information</span></span>



| <span data-ttu-id="59f28-112">Nom</span><span class="sxs-lookup"><span data-stu-id="59f28-112">Name</span></span> | <span data-ttu-id="59f28-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="59f28-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="59f28-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="59f28-114">Element Type</span></span> <br/>   | <span data-ttu-id="59f28-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="59f28-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="59f28-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="59f28-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="59f28-117">Page</span><span class="sxs-lookup"><span data-stu-id="59f28-117">Page</span></span><br/>                            |
| <span data-ttu-id="59f28-118">Notes</span><span class="sxs-lookup"><span data-stu-id="59f28-118">Notes</span></span> <br/>          | <span data-ttu-id="59f28-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="59f28-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="59f28-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="59f28-120">Structure Content</span></span>

<span data-ttu-id="59f28-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="59f28-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="59f28-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="59f28-122">Structure Properties</span></span>

<span data-ttu-id="59f28-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="59f28-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="59f28-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="59f28-124">Property</span></span>                | <span data-ttu-id="59f28-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="59f28-125">xsi:type</span></span>           | <span data-ttu-id="59f28-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="59f28-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="59f28-127">DataType</span><span class="sxs-lookup"><span data-stu-id="59f28-127">DataType</span></span><br/>     | <span data-ttu-id="59f28-128">string</span><span class="sxs-lookup"><span data-stu-id="59f28-128">string</span></span><br/>  | <span data-ttu-id="59f28-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="59f28-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="59f28-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="59f28-130">DefaultValue</span></span><br/> | <span data-ttu-id="59f28-131">entier</span><span class="sxs-lookup"><span data-stu-id="59f28-131">integer</span></span><br/> | <span data-ttu-id="59f28-132">non défini</span><span class="sxs-lookup"><span data-stu-id="59f28-132">undefined</span></span><br/>       |
| <span data-ttu-id="59f28-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="59f28-133">MaxValue</span></span><br/>     | <span data-ttu-id="59f28-134">entier</span><span class="sxs-lookup"><span data-stu-id="59f28-134">integer</span></span><br/> | <span data-ttu-id="59f28-135">non défini</span><span class="sxs-lookup"><span data-stu-id="59f28-135">undefined</span></span><br/>       |
| <span data-ttu-id="59f28-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="59f28-136">MinValue</span></span><br/>     | <span data-ttu-id="59f28-137">entier</span><span class="sxs-lookup"><span data-stu-id="59f28-137">integer</span></span><br/> | <span data-ttu-id="59f28-138">non défini</span><span class="sxs-lookup"><span data-stu-id="59f28-138">undefined</span></span><br/>       |
| <span data-ttu-id="59f28-139">Multiple</span><span class="sxs-lookup"><span data-stu-id="59f28-139">Multiple</span></span><br/>     | <span data-ttu-id="59f28-140">entier</span><span class="sxs-lookup"><span data-stu-id="59f28-140">integer</span></span><br/> | <span data-ttu-id="59f28-141">non défini</span><span class="sxs-lookup"><span data-stu-id="59f28-141">undefined</span></span><br/>       |
| <span data-ttu-id="59f28-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="59f28-142">Mandatory</span></span><br/>    | <span data-ttu-id="59f28-143">string</span><span class="sxs-lookup"><span data-stu-id="59f28-143">string</span></span><br/>  | <span data-ttu-id="59f28-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="59f28-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="59f28-145">Unité</span><span class="sxs-lookup"><span data-stu-id="59f28-145">UnitType</span></span><br/>     | <span data-ttu-id="59f28-146">string</span><span class="sxs-lookup"><span data-stu-id="59f28-146">string</span></span><br/>  | <span data-ttu-id="59f28-147">points</span><span class="sxs-lookup"><span data-stu-id="59f28-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="59f28-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59f28-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59f28-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="59f28-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




