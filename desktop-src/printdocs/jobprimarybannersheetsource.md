---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: JobPrimaryBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c86e840c3507fce80bda0f4c31efe8b0d714242
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321726"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="a2d6a-104">JobPrimaryBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="a2d6a-104">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="a2d6a-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-105">This topic is not current.</span></span> <span data-ttu-id="a2d6a-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a2d6a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a2d6a-107">Spécifie la source d’une feuille de bannière personnalisée principale pour le travail.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-107">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="a2d6a-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a2d6a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a2d6a-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a2d6a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a2d6a-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a2d6a-110">Element Information</span></span>



| <span data-ttu-id="a2d6a-111">Nom</span><span class="sxs-lookup"><span data-stu-id="a2d6a-111">Name</span></span>                       |                                             |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="a2d6a-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a2d6a-112">Element Type</span></span> <br/>   | <span data-ttu-id="a2d6a-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a2d6a-113">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="a2d6a-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a2d6a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a2d6a-115">Travail</span><span class="sxs-lookup"><span data-stu-id="a2d6a-115">Job</span></span><br/>                              |
| <span data-ttu-id="a2d6a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a2d6a-116">Notes</span></span> <br/>          | <span data-ttu-id="a2d6a-117">Lié à l’élément JobBannerSheet</span><span class="sxs-lookup"><span data-stu-id="a2d6a-117">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a2d6a-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a2d6a-118">Structure Content</span></span>

<span data-ttu-id="a2d6a-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a2d6a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryBannerSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="a2d6a-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="a2d6a-120">Structure Properties</span></span>

<span data-ttu-id="a2d6a-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a2d6a-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="a2d6a-122">Property</span></span>                | <span data-ttu-id="a2d6a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a2d6a-123">xsi:type</span></span>           | <span data-ttu-id="a2d6a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2d6a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a2d6a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a2d6a-125">DataType</span></span><br/>     | <span data-ttu-id="a2d6a-126">string</span><span class="sxs-lookup"><span data-stu-id="a2d6a-126">string</span></span><br/>  | <span data-ttu-id="a2d6a-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2d6a-127">xs:string</span></span><br/>       |
| <span data-ttu-id="a2d6a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a2d6a-128">DefaultValue</span></span><br/> | <span data-ttu-id="a2d6a-129">string</span><span class="sxs-lookup"><span data-stu-id="a2d6a-129">string</span></span><br/>  | <span data-ttu-id="a2d6a-130">non défini</span><span class="sxs-lookup"><span data-stu-id="a2d6a-130">undefined</span></span><br/>       |
| <span data-ttu-id="a2d6a-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a2d6a-131">MaxLength</span></span><br/>    | <span data-ttu-id="a2d6a-132">entier</span><span class="sxs-lookup"><span data-stu-id="a2d6a-132">integer</span></span><br/> | <span data-ttu-id="a2d6a-133">non défini</span><span class="sxs-lookup"><span data-stu-id="a2d6a-133">undefined</span></span><br/>       |
| <span data-ttu-id="a2d6a-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="a2d6a-134">MinLength</span></span><br/>    | <span data-ttu-id="a2d6a-135">integer</span><span class="sxs-lookup"><span data-stu-id="a2d6a-135">integer</span></span><br/> | <span data-ttu-id="a2d6a-136">1</span><span class="sxs-lookup"><span data-stu-id="a2d6a-136">1</span></span><br/>               |
| <span data-ttu-id="a2d6a-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2d6a-137">Mandatory</span></span><br/>    | <span data-ttu-id="a2d6a-138">string</span><span class="sxs-lookup"><span data-stu-id="a2d6a-138">string</span></span><br/>  | <span data-ttu-id="a2d6a-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="a2d6a-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a2d6a-140">Unité</span><span class="sxs-lookup"><span data-stu-id="a2d6a-140">UnitType</span></span><br/>     | <span data-ttu-id="a2d6a-141">string</span><span class="sxs-lookup"><span data-stu-id="a2d6a-141">string</span></span><br/>  | <span data-ttu-id="a2d6a-142">caractères</span><span class="sxs-lookup"><span data-stu-id="a2d6a-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a2d6a-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2d6a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d6a-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a2d6a-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




