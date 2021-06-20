---
description: En savoir plus sur l’élément DocumentBannerSheetSource, qui spécifie la source d’une feuille de bannière personnalisée.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33aa949982e98781c42cbf6aa770dbd4e3d1707
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409472"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="adf2b-103">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="adf2b-103">DocumentBannerSheetSource</span></span>

<span data-ttu-id="adf2b-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="adf2b-104">This topic is not current.</span></span> <span data-ttu-id="adf2b-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="adf2b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="adf2b-106">Spécifie la source d’une feuille de bannière personnalisée.</span><span class="sxs-lookup"><span data-stu-id="adf2b-106">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="adf2b-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="adf2b-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="adf2b-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="adf2b-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="adf2b-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="adf2b-109">Element Information</span></span>



| <span data-ttu-id="adf2b-110">Nom</span><span class="sxs-lookup"><span data-stu-id="adf2b-110">Name</span></span> | <span data-ttu-id="adf2b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf2b-111">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="adf2b-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="adf2b-112">Element Type</span></span> <br/>   | <span data-ttu-id="adf2b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="adf2b-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="adf2b-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="adf2b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="adf2b-115">Document</span><span class="sxs-lookup"><span data-stu-id="adf2b-115">Document</span></span><br/>                              |
| <span data-ttu-id="adf2b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="adf2b-116">Notes</span></span> <br/>          | <span data-ttu-id="adf2b-117">Lié à l’élément DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="adf2b-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="adf2b-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="adf2b-118">Structure Content</span></span>

<span data-ttu-id="adf2b-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="adf2b-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="adf2b-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="adf2b-120">Structure Properties</span></span>

<span data-ttu-id="adf2b-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="adf2b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="adf2b-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="adf2b-122">Property</span></span>                | <span data-ttu-id="adf2b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="adf2b-123">xsi:type</span></span>           | <span data-ttu-id="adf2b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf2b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="adf2b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="adf2b-125">DataType</span></span><br/>     | <span data-ttu-id="adf2b-126">string</span><span class="sxs-lookup"><span data-stu-id="adf2b-126">string</span></span><br/>  | <span data-ttu-id="adf2b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="adf2b-127">xs:string</span></span><br/>       |
| <span data-ttu-id="adf2b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="adf2b-128">DefaultValue</span></span><br/> | <span data-ttu-id="adf2b-129">string</span><span class="sxs-lookup"><span data-stu-id="adf2b-129">string</span></span><br/>  | <span data-ttu-id="adf2b-130">non défini</span><span class="sxs-lookup"><span data-stu-id="adf2b-130">undefined</span></span><br/>       |
| <span data-ttu-id="adf2b-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="adf2b-131">MaxLength</span></span><br/>    | <span data-ttu-id="adf2b-132">entier</span><span class="sxs-lookup"><span data-stu-id="adf2b-132">integer</span></span><br/> | <span data-ttu-id="adf2b-133">non défini</span><span class="sxs-lookup"><span data-stu-id="adf2b-133">undefined</span></span><br/>       |
| <span data-ttu-id="adf2b-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="adf2b-134">MinLength</span></span><br/>    | <span data-ttu-id="adf2b-135">integer</span><span class="sxs-lookup"><span data-stu-id="adf2b-135">integer</span></span><br/> | <span data-ttu-id="adf2b-136">1</span><span class="sxs-lookup"><span data-stu-id="adf2b-136">1</span></span><br/>               |
| <span data-ttu-id="adf2b-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="adf2b-137">Mandatory</span></span><br/>    | <span data-ttu-id="adf2b-138">string</span><span class="sxs-lookup"><span data-stu-id="adf2b-138">string</span></span><br/>  | <span data-ttu-id="adf2b-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="adf2b-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="adf2b-140">Unité</span><span class="sxs-lookup"><span data-stu-id="adf2b-140">UnitType</span></span><br/>     | <span data-ttu-id="adf2b-141">string</span><span class="sxs-lookup"><span data-stu-id="adf2b-141">string</span></span><br/>  | <span data-ttu-id="adf2b-142">caractères</span><span class="sxs-lookup"><span data-stu-id="adf2b-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="adf2b-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="adf2b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf2b-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="adf2b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




