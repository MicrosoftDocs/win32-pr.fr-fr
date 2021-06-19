---
description: En savoir plus sur l’élément PageBlackGenerationProcessingGrayComponentReplacementLevel, qui spécifie le pourcentage de remplacement des composants en gris.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8499c8521b974d01657c171a99e86e738c82b4e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408482"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="1fa95-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="1fa95-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="1fa95-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1fa95-104">This topic is not current.</span></span> <span data-ttu-id="1fa95-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1fa95-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1fa95-106">Spécifie le pourcentage de remplacement des composants en gris à effectuer.</span><span class="sxs-lookup"><span data-stu-id="1fa95-106">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="1fa95-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1fa95-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1fa95-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1fa95-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1fa95-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1fa95-109">Element Information</span></span>



| <span data-ttu-id="1fa95-110">Nom</span><span class="sxs-lookup"><span data-stu-id="1fa95-110">Name</span></span> | <span data-ttu-id="1fa95-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa95-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1fa95-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1fa95-112">Element Type</span></span> <br/>   | <span data-ttu-id="1fa95-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1fa95-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1fa95-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1fa95-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1fa95-115">Page</span><span class="sxs-lookup"><span data-stu-id="1fa95-115">Page</span></span><br/>                                            |
| <span data-ttu-id="1fa95-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1fa95-116">Notes</span></span> <br/>          | <span data-ttu-id="1fa95-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="1fa95-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1fa95-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1fa95-118">Structure Content</span></span>

<span data-ttu-id="1fa95-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1fa95-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="1fa95-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="1fa95-120">Structure Properties</span></span>

<span data-ttu-id="1fa95-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1fa95-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1fa95-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="1fa95-122">Property</span></span>                | <span data-ttu-id="1fa95-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1fa95-123">xsi:type</span></span>           | <span data-ttu-id="1fa95-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa95-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1fa95-125">DataType</span><span class="sxs-lookup"><span data-stu-id="1fa95-125">DataType</span></span><br/>     | <span data-ttu-id="1fa95-126">string</span><span class="sxs-lookup"><span data-stu-id="1fa95-126">string</span></span><br/>  | <span data-ttu-id="1fa95-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1fa95-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="1fa95-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1fa95-128">DefaultValue</span></span><br/> | <span data-ttu-id="1fa95-129">string</span><span class="sxs-lookup"><span data-stu-id="1fa95-129">string</span></span><br/>  | <span data-ttu-id="1fa95-130">non défini</span><span class="sxs-lookup"><span data-stu-id="1fa95-130">undefined</span></span><br/>       |
| <span data-ttu-id="1fa95-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1fa95-131">MaxValue</span></span><br/>     | <span data-ttu-id="1fa95-132">entier</span><span class="sxs-lookup"><span data-stu-id="1fa95-132">integer</span></span><br/> | <span data-ttu-id="1fa95-133">100</span><span class="sxs-lookup"><span data-stu-id="1fa95-133">100</span></span><br/>             |
| <span data-ttu-id="1fa95-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="1fa95-134">MinValue</span></span><br/>     | <span data-ttu-id="1fa95-135">entier</span><span class="sxs-lookup"><span data-stu-id="1fa95-135">integer</span></span><br/> | <span data-ttu-id="1fa95-136">0</span><span class="sxs-lookup"><span data-stu-id="1fa95-136">0</span></span><br/>               |
| <span data-ttu-id="1fa95-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="1fa95-137">Multiple</span></span><br/>     | <span data-ttu-id="1fa95-138">integer</span><span class="sxs-lookup"><span data-stu-id="1fa95-138">integer</span></span><br/> | <span data-ttu-id="1fa95-139">1</span><span class="sxs-lookup"><span data-stu-id="1fa95-139">1</span></span><br/>               |
| <span data-ttu-id="1fa95-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1fa95-140">Mandatory</span></span><br/>    | <span data-ttu-id="1fa95-141">string</span><span class="sxs-lookup"><span data-stu-id="1fa95-141">string</span></span><br/>  | <span data-ttu-id="1fa95-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="1fa95-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1fa95-143">Unité</span><span class="sxs-lookup"><span data-stu-id="1fa95-143">UnitType</span></span><br/>     | <span data-ttu-id="1fa95-144">string</span><span class="sxs-lookup"><span data-stu-id="1fa95-144">string</span></span><br/>  | <span data-ttu-id="1fa95-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="1fa95-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1fa95-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fa95-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa95-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1fa95-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




