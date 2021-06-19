---
description: Obtenir des informations sur le paramètre PageWatermarkTextColor. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396014"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="29748-105">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="29748-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="29748-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="29748-106">This topic is not current.</span></span> <span data-ttu-id="29748-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="29748-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="29748-108">Définit la couleur sRVB pour le texte de filigrane.</span><span class="sxs-lookup"><span data-stu-id="29748-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="29748-109">Le format est ARGB : \# AARRVVBB.</span><span class="sxs-lookup"><span data-stu-id="29748-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="29748-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="29748-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="29748-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="29748-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="29748-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="29748-112">Element Information</span></span>



| <span data-ttu-id="29748-113">Nom</span><span class="sxs-lookup"><span data-stu-id="29748-113">Name</span></span> | <span data-ttu-id="29748-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="29748-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="29748-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="29748-115">Element Type</span></span> <br/>   | <span data-ttu-id="29748-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="29748-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="29748-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="29748-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="29748-118">Page</span><span class="sxs-lookup"><span data-stu-id="29748-118">Page</span></span><br/>                            |
| <span data-ttu-id="29748-119">Notes</span><span class="sxs-lookup"><span data-stu-id="29748-119">Notes</span></span> <br/>          | <span data-ttu-id="29748-120">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="29748-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="29748-121">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="29748-121">Structure Content</span></span>

<span data-ttu-id="29748-122">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="29748-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="29748-123">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="29748-123">Structure Properties</span></span>

<span data-ttu-id="29748-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="29748-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="29748-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="29748-125">Property</span></span>                | <span data-ttu-id="29748-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="29748-126">xsi:type</span></span>           | <span data-ttu-id="29748-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="29748-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="29748-128">DataType</span><span class="sxs-lookup"><span data-stu-id="29748-128">DataType</span></span><br/>     | <span data-ttu-id="29748-129">string</span><span class="sxs-lookup"><span data-stu-id="29748-129">string</span></span><br/>  | <span data-ttu-id="29748-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="29748-130">xs:string</span></span><br/>       |
| <span data-ttu-id="29748-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="29748-131">DefaultValue</span></span><br/> | <span data-ttu-id="29748-132">entier</span><span class="sxs-lookup"><span data-stu-id="29748-132">integer</span></span><br/> | <span data-ttu-id="29748-133">non défini</span><span class="sxs-lookup"><span data-stu-id="29748-133">undefined</span></span><br/>       |
| <span data-ttu-id="29748-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="29748-134">MaxValue</span></span><br/>     | <span data-ttu-id="29748-135">entier</span><span class="sxs-lookup"><span data-stu-id="29748-135">integer</span></span><br/> | <span data-ttu-id="29748-136">non défini</span><span class="sxs-lookup"><span data-stu-id="29748-136">undefined</span></span><br/>       |
| <span data-ttu-id="29748-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="29748-137">MinValue</span></span><br/>     | <span data-ttu-id="29748-138">entier</span><span class="sxs-lookup"><span data-stu-id="29748-138">integer</span></span><br/> | <span data-ttu-id="29748-139">non défini</span><span class="sxs-lookup"><span data-stu-id="29748-139">undefined</span></span><br/>       |
| <span data-ttu-id="29748-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="29748-140">Mandatory</span></span><br/>    | <span data-ttu-id="29748-141">string</span><span class="sxs-lookup"><span data-stu-id="29748-141">string</span></span><br/>  | <span data-ttu-id="29748-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="29748-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="29748-143">Unité</span><span class="sxs-lookup"><span data-stu-id="29748-143">UnitType</span></span><br/>     | <span data-ttu-id="29748-144">string</span><span class="sxs-lookup"><span data-stu-id="29748-144">string</span></span><br/>  | <span data-ttu-id="29748-145">sRVB</span><span class="sxs-lookup"><span data-stu-id="29748-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="29748-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29748-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29748-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="29748-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




