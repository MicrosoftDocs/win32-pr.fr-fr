---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104042984"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="6ac37-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="6ac37-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="6ac37-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="6ac37-105">This topic is not current.</span></span> <span data-ttu-id="6ac37-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6ac37-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ac37-107">Définit les tailles de police disponibles pour le texte de filigrane.</span><span class="sxs-lookup"><span data-stu-id="6ac37-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="6ac37-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6ac37-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6ac37-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="6ac37-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6ac37-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6ac37-110">Element Information</span></span>



| <span data-ttu-id="6ac37-111">Nom</span><span class="sxs-lookup"><span data-stu-id="6ac37-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="6ac37-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="6ac37-112">Element Type</span></span> <br/>   | <span data-ttu-id="6ac37-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6ac37-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="6ac37-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="6ac37-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6ac37-115">Page</span><span class="sxs-lookup"><span data-stu-id="6ac37-115">Page</span></span><br/>                            |
| <span data-ttu-id="6ac37-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6ac37-116">Notes</span></span> <br/>          | <span data-ttu-id="6ac37-117">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="6ac37-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6ac37-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="6ac37-118">Structure Content</span></span>

<span data-ttu-id="6ac37-119">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6ac37-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="6ac37-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="6ac37-120">Structure Properties</span></span>

<span data-ttu-id="6ac37-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="6ac37-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6ac37-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="6ac37-122">Property</span></span>                | <span data-ttu-id="6ac37-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6ac37-123">xsi:type</span></span>           | <span data-ttu-id="6ac37-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ac37-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6ac37-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6ac37-125">DataType</span></span><br/>     | <span data-ttu-id="6ac37-126">string</span><span class="sxs-lookup"><span data-stu-id="6ac37-126">string</span></span><br/>  | <span data-ttu-id="6ac37-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6ac37-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="6ac37-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6ac37-128">DefaultValue</span></span><br/> | <span data-ttu-id="6ac37-129">entier</span><span class="sxs-lookup"><span data-stu-id="6ac37-129">integer</span></span><br/> | <span data-ttu-id="6ac37-130">non défini</span><span class="sxs-lookup"><span data-stu-id="6ac37-130">undefined</span></span><br/>       |
| <span data-ttu-id="6ac37-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6ac37-131">MaxValue</span></span><br/>     | <span data-ttu-id="6ac37-132">entier</span><span class="sxs-lookup"><span data-stu-id="6ac37-132">integer</span></span><br/> | <span data-ttu-id="6ac37-133">non défini</span><span class="sxs-lookup"><span data-stu-id="6ac37-133">undefined</span></span><br/>       |
| <span data-ttu-id="6ac37-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="6ac37-134">MinValue</span></span><br/>     | <span data-ttu-id="6ac37-135">entier</span><span class="sxs-lookup"><span data-stu-id="6ac37-135">integer</span></span><br/> | <span data-ttu-id="6ac37-136">non défini</span><span class="sxs-lookup"><span data-stu-id="6ac37-136">undefined</span></span><br/>       |
| <span data-ttu-id="6ac37-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="6ac37-137">Multiple</span></span><br/>     | <span data-ttu-id="6ac37-138">entier</span><span class="sxs-lookup"><span data-stu-id="6ac37-138">integer</span></span><br/> | <span data-ttu-id="6ac37-139">non défini</span><span class="sxs-lookup"><span data-stu-id="6ac37-139">undefined</span></span><br/>       |
| <span data-ttu-id="6ac37-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6ac37-140">Mandatory</span></span><br/>    | <span data-ttu-id="6ac37-141">string</span><span class="sxs-lookup"><span data-stu-id="6ac37-141">string</span></span><br/>  | <span data-ttu-id="6ac37-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="6ac37-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6ac37-143">Unité</span><span class="sxs-lookup"><span data-stu-id="6ac37-143">UnitType</span></span><br/>     | <span data-ttu-id="6ac37-144">string</span><span class="sxs-lookup"><span data-stu-id="6ac37-144">string</span></span><br/>  | <span data-ttu-id="6ac37-145">points</span><span class="sxs-lookup"><span data-stu-id="6ac37-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="6ac37-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ac37-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ac37-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="6ac37-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




