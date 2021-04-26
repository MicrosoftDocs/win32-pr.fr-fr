---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995546"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="605a3-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="605a3-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="605a3-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="605a3-105">This topic is not current.</span></span> <span data-ttu-id="605a3-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="605a3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="605a3-107">Spécifie l’angle du texte de filigrane par rapport à la direction PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="605a3-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="605a3-108">L’angle est mesuré dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="605a3-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="605a3-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="605a3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="605a3-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="605a3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="605a3-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="605a3-111">Element Information</span></span>



| <span data-ttu-id="605a3-112">Nom</span><span class="sxs-lookup"><span data-stu-id="605a3-112">Name</span></span> | <span data-ttu-id="605a3-113">Value</span><span class="sxs-lookup"><span data-stu-id="605a3-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="605a3-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="605a3-114">Element Type</span></span> <br/>   | <span data-ttu-id="605a3-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="605a3-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="605a3-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="605a3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="605a3-117">Page</span><span class="sxs-lookup"><span data-stu-id="605a3-117">Page</span></span><br/>                            |
| <span data-ttu-id="605a3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="605a3-118">Notes</span></span> <br/>          | <span data-ttu-id="605a3-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="605a3-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="605a3-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="605a3-120">Structure Content</span></span>

<span data-ttu-id="605a3-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="605a3-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="605a3-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="605a3-122">Structure Properties</span></span>

<span data-ttu-id="605a3-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="605a3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="605a3-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="605a3-124">Property</span></span>                | <span data-ttu-id="605a3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="605a3-125">xsi:type</span></span>           | <span data-ttu-id="605a3-126">Value</span><span class="sxs-lookup"><span data-stu-id="605a3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="605a3-127">DataType</span><span class="sxs-lookup"><span data-stu-id="605a3-127">DataType</span></span><br/>     | <span data-ttu-id="605a3-128">string</span><span class="sxs-lookup"><span data-stu-id="605a3-128">string</span></span><br/>  | <span data-ttu-id="605a3-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="605a3-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="605a3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="605a3-130">DefaultValue</span></span><br/> | <span data-ttu-id="605a3-131">entier</span><span class="sxs-lookup"><span data-stu-id="605a3-131">integer</span></span><br/> | <span data-ttu-id="605a3-132">0</span><span class="sxs-lookup"><span data-stu-id="605a3-132">0</span></span><br/>               |
| <span data-ttu-id="605a3-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="605a3-133">MaxValue</span></span><br/>     | <span data-ttu-id="605a3-134">entier</span><span class="sxs-lookup"><span data-stu-id="605a3-134">integer</span></span><br/> | <span data-ttu-id="605a3-135">359</span><span class="sxs-lookup"><span data-stu-id="605a3-135">359</span></span><br/>             |
| <span data-ttu-id="605a3-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="605a3-136">MinValue</span></span><br/>     | <span data-ttu-id="605a3-137">entier</span><span class="sxs-lookup"><span data-stu-id="605a3-137">integer</span></span><br/> | <span data-ttu-id="605a3-138">0</span><span class="sxs-lookup"><span data-stu-id="605a3-138">0</span></span><br/>               |
| <span data-ttu-id="605a3-139">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="605a3-139">Multiple</span></span><br/>     | <span data-ttu-id="605a3-140">integer</span><span class="sxs-lookup"><span data-stu-id="605a3-140">integer</span></span><br/> | <span data-ttu-id="605a3-141">1</span><span class="sxs-lookup"><span data-stu-id="605a3-141">1</span></span><br/>               |
| <span data-ttu-id="605a3-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="605a3-142">Mandatory</span></span><br/>    | <span data-ttu-id="605a3-143">string</span><span class="sxs-lookup"><span data-stu-id="605a3-143">string</span></span><br/>  | <span data-ttu-id="605a3-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="605a3-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="605a3-145">Unité</span><span class="sxs-lookup"><span data-stu-id="605a3-145">UnitType</span></span><br/>     | <span data-ttu-id="605a3-146">string</span><span class="sxs-lookup"><span data-stu-id="605a3-146">string</span></span><br/>  | <span data-ttu-id="605a3-147">degrés</span><span class="sxs-lookup"><span data-stu-id="605a3-147">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="605a3-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="605a3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="605a3-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="605a3-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




