---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cc8c7f3c9a692ffbe180c253d448d7c4e320d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999126"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="55c94-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="55c94-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="55c94-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="55c94-105">This topic is not current.</span></span> <span data-ttu-id="55c94-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="55c94-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="55c94-107">Définit les tailles de police disponibles pour le texte de filigrane.</span><span class="sxs-lookup"><span data-stu-id="55c94-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="55c94-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="55c94-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="55c94-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="55c94-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="55c94-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="55c94-110">Element Information</span></span>



| <span data-ttu-id="55c94-111">Nom</span><span class="sxs-lookup"><span data-stu-id="55c94-111">Name</span></span> | <span data-ttu-id="55c94-112">Value</span><span class="sxs-lookup"><span data-stu-id="55c94-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="55c94-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="55c94-113">Element Type</span></span> <br/>   | <span data-ttu-id="55c94-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="55c94-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="55c94-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="55c94-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="55c94-116">Page</span><span class="sxs-lookup"><span data-stu-id="55c94-116">Page</span></span><br/>                            |
| <span data-ttu-id="55c94-117">Notes</span><span class="sxs-lookup"><span data-stu-id="55c94-117">Notes</span></span> <br/>          | <span data-ttu-id="55c94-118">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="55c94-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="55c94-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="55c94-119">Structure Content</span></span>

<span data-ttu-id="55c94-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="55c94-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="55c94-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="55c94-121">Structure Properties</span></span>

<span data-ttu-id="55c94-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="55c94-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="55c94-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="55c94-123">Property</span></span>                | <span data-ttu-id="55c94-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="55c94-124">xsi:type</span></span>           | <span data-ttu-id="55c94-125">Value</span><span class="sxs-lookup"><span data-stu-id="55c94-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="55c94-126">DataType</span><span class="sxs-lookup"><span data-stu-id="55c94-126">DataType</span></span><br/>     | <span data-ttu-id="55c94-127">string</span><span class="sxs-lookup"><span data-stu-id="55c94-127">string</span></span><br/>  | <span data-ttu-id="55c94-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="55c94-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="55c94-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="55c94-129">DefaultValue</span></span><br/> | <span data-ttu-id="55c94-130">entier</span><span class="sxs-lookup"><span data-stu-id="55c94-130">integer</span></span><br/> | <span data-ttu-id="55c94-131">non défini</span><span class="sxs-lookup"><span data-stu-id="55c94-131">undefined</span></span><br/>       |
| <span data-ttu-id="55c94-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="55c94-132">MaxValue</span></span><br/>     | <span data-ttu-id="55c94-133">entier</span><span class="sxs-lookup"><span data-stu-id="55c94-133">integer</span></span><br/> | <span data-ttu-id="55c94-134">non défini</span><span class="sxs-lookup"><span data-stu-id="55c94-134">undefined</span></span><br/>       |
| <span data-ttu-id="55c94-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="55c94-135">MinValue</span></span><br/>     | <span data-ttu-id="55c94-136">entier</span><span class="sxs-lookup"><span data-stu-id="55c94-136">integer</span></span><br/> | <span data-ttu-id="55c94-137">non défini</span><span class="sxs-lookup"><span data-stu-id="55c94-137">undefined</span></span><br/>       |
| <span data-ttu-id="55c94-138">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="55c94-138">Multiple</span></span><br/>     | <span data-ttu-id="55c94-139">entier</span><span class="sxs-lookup"><span data-stu-id="55c94-139">integer</span></span><br/> | <span data-ttu-id="55c94-140">non défini</span><span class="sxs-lookup"><span data-stu-id="55c94-140">undefined</span></span><br/>       |
| <span data-ttu-id="55c94-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="55c94-141">Mandatory</span></span><br/>    | <span data-ttu-id="55c94-142">string</span><span class="sxs-lookup"><span data-stu-id="55c94-142">string</span></span><br/>  | <span data-ttu-id="55c94-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="55c94-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="55c94-144">Unité</span><span class="sxs-lookup"><span data-stu-id="55c94-144">UnitType</span></span><br/>     | <span data-ttu-id="55c94-145">string</span><span class="sxs-lookup"><span data-stu-id="55c94-145">string</span></span><br/>  | <span data-ttu-id="55c94-146">points</span><span class="sxs-lookup"><span data-stu-id="55c94-146">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="55c94-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55c94-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55c94-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="55c94-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




