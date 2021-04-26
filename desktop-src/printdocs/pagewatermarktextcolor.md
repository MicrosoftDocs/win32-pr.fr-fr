---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996886"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="5ee16-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="5ee16-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="5ee16-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5ee16-105">This topic is not current.</span></span> <span data-ttu-id="5ee16-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5ee16-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ee16-107">Définit la couleur sRVB pour le texte de filigrane.</span><span class="sxs-lookup"><span data-stu-id="5ee16-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="5ee16-108">Le format est ARGB : \# AARRVVBB.</span><span class="sxs-lookup"><span data-stu-id="5ee16-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="5ee16-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5ee16-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5ee16-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="5ee16-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5ee16-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5ee16-111">Element Information</span></span>



| <span data-ttu-id="5ee16-112">Nom</span><span class="sxs-lookup"><span data-stu-id="5ee16-112">Name</span></span> | <span data-ttu-id="5ee16-113">Value</span><span class="sxs-lookup"><span data-stu-id="5ee16-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="5ee16-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="5ee16-114">Element Type</span></span> <br/>   | <span data-ttu-id="5ee16-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5ee16-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="5ee16-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="5ee16-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5ee16-117">Page</span><span class="sxs-lookup"><span data-stu-id="5ee16-117">Page</span></span><br/>                            |
| <span data-ttu-id="5ee16-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5ee16-118">Notes</span></span> <br/>          | <span data-ttu-id="5ee16-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="5ee16-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5ee16-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="5ee16-120">Structure Content</span></span>

<span data-ttu-id="5ee16-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="5ee16-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5ee16-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="5ee16-122">Structure Properties</span></span>

<span data-ttu-id="5ee16-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="5ee16-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5ee16-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="5ee16-124">Property</span></span>                | <span data-ttu-id="5ee16-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5ee16-125">xsi:type</span></span>           | <span data-ttu-id="5ee16-126">Value</span><span class="sxs-lookup"><span data-stu-id="5ee16-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5ee16-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5ee16-127">DataType</span></span><br/>     | <span data-ttu-id="5ee16-128">string</span><span class="sxs-lookup"><span data-stu-id="5ee16-128">string</span></span><br/>  | <span data-ttu-id="5ee16-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="5ee16-129">xs:string</span></span><br/>       |
| <span data-ttu-id="5ee16-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5ee16-130">DefaultValue</span></span><br/> | <span data-ttu-id="5ee16-131">entier</span><span class="sxs-lookup"><span data-stu-id="5ee16-131">integer</span></span><br/> | <span data-ttu-id="5ee16-132">non défini</span><span class="sxs-lookup"><span data-stu-id="5ee16-132">undefined</span></span><br/>       |
| <span data-ttu-id="5ee16-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5ee16-133">MaxValue</span></span><br/>     | <span data-ttu-id="5ee16-134">entier</span><span class="sxs-lookup"><span data-stu-id="5ee16-134">integer</span></span><br/> | <span data-ttu-id="5ee16-135">non défini</span><span class="sxs-lookup"><span data-stu-id="5ee16-135">undefined</span></span><br/>       |
| <span data-ttu-id="5ee16-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="5ee16-136">MinValue</span></span><br/>     | <span data-ttu-id="5ee16-137">entier</span><span class="sxs-lookup"><span data-stu-id="5ee16-137">integer</span></span><br/> | <span data-ttu-id="5ee16-138">non défini</span><span class="sxs-lookup"><span data-stu-id="5ee16-138">undefined</span></span><br/>       |
| <span data-ttu-id="5ee16-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5ee16-139">Mandatory</span></span><br/>    | <span data-ttu-id="5ee16-140">string</span><span class="sxs-lookup"><span data-stu-id="5ee16-140">string</span></span><br/>  | <span data-ttu-id="5ee16-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="5ee16-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5ee16-142">Unité</span><span class="sxs-lookup"><span data-stu-id="5ee16-142">UnitType</span></span><br/>     | <span data-ttu-id="5ee16-143">string</span><span class="sxs-lookup"><span data-stu-id="5ee16-143">string</span></span><br/>  | <span data-ttu-id="5ee16-144">sRVB</span><span class="sxs-lookup"><span data-stu-id="5ee16-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="5ee16-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ee16-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee16-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="5ee16-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




