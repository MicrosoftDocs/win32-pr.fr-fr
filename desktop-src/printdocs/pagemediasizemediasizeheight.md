---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305f67179343fa4acb2fa784113d63d5d2333b0b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993706"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="bc871-104">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="bc871-104">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="bc871-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="bc871-105">This topic is not current.</span></span> <span data-ttu-id="bc871-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bc871-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc871-107">Spécifie la direction MediaSizeHeight de la dimension pour l’option MediaSize personnalisée.</span><span class="sxs-lookup"><span data-stu-id="bc871-107">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="bc871-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bc871-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bc871-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="bc871-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bc871-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="bc871-110">Element Information</span></span>



| <span data-ttu-id="bc871-111">Nom</span><span class="sxs-lookup"><span data-stu-id="bc871-111">Name</span></span> | <span data-ttu-id="bc871-112">Value</span><span class="sxs-lookup"><span data-stu-id="bc871-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="bc871-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="bc871-113">Element Type</span></span> <br/>   | <span data-ttu-id="bc871-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bc871-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="bc871-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="bc871-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bc871-116">Page</span><span class="sxs-lookup"><span data-stu-id="bc871-116">Page</span></span><br/>                                           |
| <span data-ttu-id="bc871-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bc871-117">Notes</span></span> <br/>          | <span data-ttu-id="bc871-118">Lié à l’élément PageMediaSize, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="bc871-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="bc871-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="bc871-119">Structure Content</span></span>

<span data-ttu-id="bc871-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="bc871-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="bc871-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="bc871-121">Structure Properties</span></span>

<span data-ttu-id="bc871-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="bc871-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bc871-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="bc871-123">Property</span></span>                | <span data-ttu-id="bc871-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bc871-124">xsi:type</span></span>           | <span data-ttu-id="bc871-125">Value</span><span class="sxs-lookup"><span data-stu-id="bc871-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="bc871-126">DataType</span><span class="sxs-lookup"><span data-stu-id="bc871-126">DataType</span></span><br/>     | <span data-ttu-id="bc871-127">string</span><span class="sxs-lookup"><span data-stu-id="bc871-127">string</span></span><br/>  | <span data-ttu-id="bc871-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bc871-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="bc871-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bc871-129">DefaultValue</span></span><br/> | <span data-ttu-id="bc871-130">entier</span><span class="sxs-lookup"><span data-stu-id="bc871-130">integer</span></span><br/> | <span data-ttu-id="bc871-131">non défini</span><span class="sxs-lookup"><span data-stu-id="bc871-131">undefined</span></span><br/>       |
| <span data-ttu-id="bc871-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bc871-132">MaxValue</span></span><br/>     | <span data-ttu-id="bc871-133">entier</span><span class="sxs-lookup"><span data-stu-id="bc871-133">integer</span></span><br/> | <span data-ttu-id="bc871-134">non défini</span><span class="sxs-lookup"><span data-stu-id="bc871-134">undefined</span></span><br/>       |
| <span data-ttu-id="bc871-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="bc871-135">MinValue</span></span><br/>     | <span data-ttu-id="bc871-136">entier</span><span class="sxs-lookup"><span data-stu-id="bc871-136">integer</span></span><br/> | <span data-ttu-id="bc871-137">non défini</span><span class="sxs-lookup"><span data-stu-id="bc871-137">undefined</span></span><br/>       |
| <span data-ttu-id="bc871-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bc871-138">Mandatory</span></span><br/>    | <span data-ttu-id="bc871-139">string</span><span class="sxs-lookup"><span data-stu-id="bc871-139">string</span></span><br/>  | <span data-ttu-id="bc871-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="bc871-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="bc871-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="bc871-141">Multiple</span></span><br/>     | <span data-ttu-id="bc871-142">integer</span><span class="sxs-lookup"><span data-stu-id="bc871-142">integer</span></span><br/> | <span data-ttu-id="bc871-143">1</span><span class="sxs-lookup"><span data-stu-id="bc871-143">1</span></span><br/>               |
| <span data-ttu-id="bc871-144">Unité</span><span class="sxs-lookup"><span data-stu-id="bc871-144">UnitType</span></span><br/>     | <span data-ttu-id="bc871-145">string</span><span class="sxs-lookup"><span data-stu-id="bc871-145">string</span></span><br/>  | <span data-ttu-id="bc871-146">microns</span><span class="sxs-lookup"><span data-stu-id="bc871-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="bc871-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc871-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc871-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="bc871-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




