---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106537178"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="72a74-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="72a74-104">PageWatermarkTextText</span></span>

<span data-ttu-id="72a74-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="72a74-105">This topic is not current.</span></span> <span data-ttu-id="72a74-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="72a74-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="72a74-107">Spécifie le texte du filigrane.</span><span class="sxs-lookup"><span data-stu-id="72a74-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="72a74-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="72a74-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="72a74-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="72a74-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="72a74-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="72a74-110">Element Information</span></span>



| <span data-ttu-id="72a74-111">Nom</span><span class="sxs-lookup"><span data-stu-id="72a74-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="72a74-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="72a74-112">Element Type</span></span> <br/>   | <span data-ttu-id="72a74-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="72a74-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="72a74-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="72a74-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="72a74-115">Page</span><span class="sxs-lookup"><span data-stu-id="72a74-115">Page</span></span><br/>                            |
| <span data-ttu-id="72a74-116">Notes</span><span class="sxs-lookup"><span data-stu-id="72a74-116">Notes</span></span> <br/>          | <span data-ttu-id="72a74-117">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="72a74-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="72a74-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="72a74-118">Structure Content</span></span>

<span data-ttu-id="72a74-119">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="72a74-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="72a74-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="72a74-120">Structure Properties</span></span>

<span data-ttu-id="72a74-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="72a74-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="72a74-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="72a74-122">Property</span></span>                | <span data-ttu-id="72a74-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="72a74-123">xsi:type</span></span>           | <span data-ttu-id="72a74-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="72a74-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="72a74-125">DataType</span><span class="sxs-lookup"><span data-stu-id="72a74-125">DataType</span></span><br/>     | <span data-ttu-id="72a74-126">String</span><span class="sxs-lookup"><span data-stu-id="72a74-126">String</span></span><br/>  | <span data-ttu-id="72a74-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="72a74-127">xs:string</span></span><br/>       |
| <span data-ttu-id="72a74-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="72a74-128">DefaultValue</span></span><br/> | <span data-ttu-id="72a74-129">Integer</span><span class="sxs-lookup"><span data-stu-id="72a74-129">Integer</span></span><br/> | <span data-ttu-id="72a74-130">non défini</span><span class="sxs-lookup"><span data-stu-id="72a74-130">undefined</span></span><br/>       |
| <span data-ttu-id="72a74-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="72a74-131">MaxLength</span></span><br/>    | <span data-ttu-id="72a74-132">Integer</span><span class="sxs-lookup"><span data-stu-id="72a74-132">Integer</span></span><br/> | <span data-ttu-id="72a74-133">non défini</span><span class="sxs-lookup"><span data-stu-id="72a74-133">undefined</span></span><br/>       |
| <span data-ttu-id="72a74-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="72a74-134">MinLength</span></span><br/>    | <span data-ttu-id="72a74-135">Integer</span><span class="sxs-lookup"><span data-stu-id="72a74-135">Integer</span></span><br/> | <span data-ttu-id="72a74-136">1</span><span class="sxs-lookup"><span data-stu-id="72a74-136">1</span></span><br/>               |
| <span data-ttu-id="72a74-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="72a74-137">Mandatory</span></span><br/>    | <span data-ttu-id="72a74-138">String</span><span class="sxs-lookup"><span data-stu-id="72a74-138">String</span></span><br/>  | <span data-ttu-id="72a74-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="72a74-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="72a74-140">Unité</span><span class="sxs-lookup"><span data-stu-id="72a74-140">UnitType</span></span><br/>     | <span data-ttu-id="72a74-141">String</span><span class="sxs-lookup"><span data-stu-id="72a74-141">String</span></span><br/>  | <span data-ttu-id="72a74-142">caractères</span><span class="sxs-lookup"><span data-stu-id="72a74-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="72a74-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72a74-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72a74-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="72a74-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




