---
description: Obtenir plus d’informations sur le paramètre PageWatermarkTextAngle. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395974"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="48bda-105">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="48bda-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="48bda-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="48bda-106">This topic is not current.</span></span> <span data-ttu-id="48bda-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="48bda-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="48bda-108">Spécifie l’angle du texte de filigrane par rapport à la direction PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="48bda-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="48bda-109">L’angle est mesuré dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="48bda-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="48bda-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="48bda-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="48bda-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="48bda-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="48bda-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="48bda-112">Element Information</span></span>



| <span data-ttu-id="48bda-113">Nom</span><span class="sxs-lookup"><span data-stu-id="48bda-113">Name</span></span> | <span data-ttu-id="48bda-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="48bda-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="48bda-115">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="48bda-115">Element Type</span></span> <br/>   | <span data-ttu-id="48bda-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="48bda-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="48bda-117">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="48bda-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="48bda-118">Page</span><span class="sxs-lookup"><span data-stu-id="48bda-118">Page</span></span><br/>                            |
| <span data-ttu-id="48bda-119">Notes</span><span class="sxs-lookup"><span data-stu-id="48bda-119">Notes</span></span> <br/>          | <span data-ttu-id="48bda-120">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="48bda-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="48bda-121">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="48bda-121">Structure Content</span></span>

<span data-ttu-id="48bda-122">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="48bda-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="48bda-123">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="48bda-123">Structure Properties</span></span>

<span data-ttu-id="48bda-124">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="48bda-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="48bda-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="48bda-125">Property</span></span>                | <span data-ttu-id="48bda-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="48bda-126">xsi:type</span></span>           | <span data-ttu-id="48bda-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="48bda-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="48bda-128">DataType</span><span class="sxs-lookup"><span data-stu-id="48bda-128">DataType</span></span><br/>     | <span data-ttu-id="48bda-129">string</span><span class="sxs-lookup"><span data-stu-id="48bda-129">string</span></span><br/>  | <span data-ttu-id="48bda-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="48bda-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="48bda-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="48bda-131">DefaultValue</span></span><br/> | <span data-ttu-id="48bda-132">entier</span><span class="sxs-lookup"><span data-stu-id="48bda-132">integer</span></span><br/> | <span data-ttu-id="48bda-133">0</span><span class="sxs-lookup"><span data-stu-id="48bda-133">0</span></span><br/>               |
| <span data-ttu-id="48bda-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="48bda-134">MaxValue</span></span><br/>     | <span data-ttu-id="48bda-135">entier</span><span class="sxs-lookup"><span data-stu-id="48bda-135">integer</span></span><br/> | <span data-ttu-id="48bda-136">359</span><span class="sxs-lookup"><span data-stu-id="48bda-136">359</span></span><br/>             |
| <span data-ttu-id="48bda-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="48bda-137">MinValue</span></span><br/>     | <span data-ttu-id="48bda-138">entier</span><span class="sxs-lookup"><span data-stu-id="48bda-138">integer</span></span><br/> | <span data-ttu-id="48bda-139">0</span><span class="sxs-lookup"><span data-stu-id="48bda-139">0</span></span><br/>               |
| <span data-ttu-id="48bda-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="48bda-140">Multiple</span></span><br/>     | <span data-ttu-id="48bda-141">integer</span><span class="sxs-lookup"><span data-stu-id="48bda-141">integer</span></span><br/> | <span data-ttu-id="48bda-142">1</span><span class="sxs-lookup"><span data-stu-id="48bda-142">1</span></span><br/>               |
| <span data-ttu-id="48bda-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="48bda-143">Mandatory</span></span><br/>    | <span data-ttu-id="48bda-144">string</span><span class="sxs-lookup"><span data-stu-id="48bda-144">string</span></span><br/>  | <span data-ttu-id="48bda-145">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="48bda-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="48bda-146">Unité</span><span class="sxs-lookup"><span data-stu-id="48bda-146">UnitType</span></span><br/>     | <span data-ttu-id="48bda-147">string</span><span class="sxs-lookup"><span data-stu-id="48bda-147">string</span></span><br/>  | <span data-ttu-id="48bda-148">degrés</span><span class="sxs-lookup"><span data-stu-id="48bda-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="48bda-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="48bda-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48bda-150">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="48bda-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




