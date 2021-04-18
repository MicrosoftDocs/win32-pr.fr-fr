---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104530579"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="872b2-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="872b2-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="872b2-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="872b2-105">This topic is not current.</span></span> <span data-ttu-id="872b2-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="872b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="872b2-107">Définit la couleur sRVB pour le texte de filigrane.</span><span class="sxs-lookup"><span data-stu-id="872b2-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="872b2-108">Le format est ARGB : \# AARRVVBB.</span><span class="sxs-lookup"><span data-stu-id="872b2-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="872b2-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="872b2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="872b2-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="872b2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="872b2-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="872b2-111">Element Information</span></span>



| <span data-ttu-id="872b2-112">Nom</span><span class="sxs-lookup"><span data-stu-id="872b2-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="872b2-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="872b2-113">Element Type</span></span> <br/>   | <span data-ttu-id="872b2-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="872b2-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="872b2-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="872b2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="872b2-116">Page</span><span class="sxs-lookup"><span data-stu-id="872b2-116">Page</span></span><br/>                            |
| <span data-ttu-id="872b2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="872b2-117">Notes</span></span> <br/>          | <span data-ttu-id="872b2-118">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="872b2-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="872b2-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="872b2-119">Structure Content</span></span>

<span data-ttu-id="872b2-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="872b2-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="872b2-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="872b2-121">Structure Properties</span></span>

<span data-ttu-id="872b2-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="872b2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="872b2-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="872b2-123">Property</span></span>                | <span data-ttu-id="872b2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="872b2-124">xsi:type</span></span>           | <span data-ttu-id="872b2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="872b2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="872b2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="872b2-126">DataType</span></span><br/>     | <span data-ttu-id="872b2-127">string</span><span class="sxs-lookup"><span data-stu-id="872b2-127">string</span></span><br/>  | <span data-ttu-id="872b2-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="872b2-128">xs:string</span></span><br/>       |
| <span data-ttu-id="872b2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="872b2-129">DefaultValue</span></span><br/> | <span data-ttu-id="872b2-130">entier</span><span class="sxs-lookup"><span data-stu-id="872b2-130">integer</span></span><br/> | <span data-ttu-id="872b2-131">non défini</span><span class="sxs-lookup"><span data-stu-id="872b2-131">undefined</span></span><br/>       |
| <span data-ttu-id="872b2-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="872b2-132">MaxValue</span></span><br/>     | <span data-ttu-id="872b2-133">entier</span><span class="sxs-lookup"><span data-stu-id="872b2-133">integer</span></span><br/> | <span data-ttu-id="872b2-134">non défini</span><span class="sxs-lookup"><span data-stu-id="872b2-134">undefined</span></span><br/>       |
| <span data-ttu-id="872b2-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="872b2-135">MinValue</span></span><br/>     | <span data-ttu-id="872b2-136">entier</span><span class="sxs-lookup"><span data-stu-id="872b2-136">integer</span></span><br/> | <span data-ttu-id="872b2-137">non défini</span><span class="sxs-lookup"><span data-stu-id="872b2-137">undefined</span></span><br/>       |
| <span data-ttu-id="872b2-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="872b2-138">Mandatory</span></span><br/>    | <span data-ttu-id="872b2-139">string</span><span class="sxs-lookup"><span data-stu-id="872b2-139">string</span></span><br/>  | <span data-ttu-id="872b2-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="872b2-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="872b2-141">Unité</span><span class="sxs-lookup"><span data-stu-id="872b2-141">UnitType</span></span><br/>     | <span data-ttu-id="872b2-142">string</span><span class="sxs-lookup"><span data-stu-id="872b2-142">string</span></span><br/>  | <span data-ttu-id="872b2-143">sRVB</span><span class="sxs-lookup"><span data-stu-id="872b2-143">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="872b2-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="872b2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872b2-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="872b2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




