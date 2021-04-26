---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c87a31e645b9ea5eedb22b48000991a99bc7e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998156"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="1e872-104">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="1e872-104">JobErrorSheetSource</span></span>

<span data-ttu-id="1e872-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1e872-105">This topic is not current.</span></span> <span data-ttu-id="1e872-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1e872-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1e872-107">Spécifie la source d’une feuille d’erreur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1e872-107">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="1e872-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1e872-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1e872-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1e872-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1e872-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1e872-110">Element Information</span></span>



| <span data-ttu-id="1e872-111">Nom</span><span class="sxs-lookup"><span data-stu-id="1e872-111">Name</span></span> | <span data-ttu-id="1e872-112">Value</span><span class="sxs-lookup"><span data-stu-id="1e872-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="1e872-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1e872-113">Element Type</span></span> <br/>   | <span data-ttu-id="1e872-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1e872-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="1e872-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1e872-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1e872-116">Document</span><span class="sxs-lookup"><span data-stu-id="1e872-116">Document</span></span><br/>                        |
| <span data-ttu-id="1e872-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1e872-117">Notes</span></span> <br/>          | <span data-ttu-id="1e872-118">Lié à l’élément JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="1e872-118">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1e872-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1e872-119">Structure Content</span></span>

<span data-ttu-id="1e872-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1e872-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobErrorSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="1e872-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="1e872-121">Structure Properties</span></span>

<span data-ttu-id="1e872-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1e872-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1e872-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="1e872-123">Property</span></span>                | <span data-ttu-id="1e872-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1e872-124">xsi:type</span></span>           | <span data-ttu-id="1e872-125">Value</span><span class="sxs-lookup"><span data-stu-id="1e872-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1e872-126">DataType</span><span class="sxs-lookup"><span data-stu-id="1e872-126">DataType</span></span><br/>     | <span data-ttu-id="1e872-127">string</span><span class="sxs-lookup"><span data-stu-id="1e872-127">string</span></span><br/>  | <span data-ttu-id="1e872-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e872-128">xs:string</span></span><br/>       |
| <span data-ttu-id="1e872-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1e872-129">DefaultValue</span></span><br/> | <span data-ttu-id="1e872-130">string</span><span class="sxs-lookup"><span data-stu-id="1e872-130">string</span></span><br/>  | <span data-ttu-id="1e872-131">non défini</span><span class="sxs-lookup"><span data-stu-id="1e872-131">undefined</span></span><br/>       |
| <span data-ttu-id="1e872-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1e872-132">MaxLength</span></span><br/>    | <span data-ttu-id="1e872-133">entier</span><span class="sxs-lookup"><span data-stu-id="1e872-133">integer</span></span><br/> | <span data-ttu-id="1e872-134">non défini</span><span class="sxs-lookup"><span data-stu-id="1e872-134">undefined</span></span><br/>       |
| <span data-ttu-id="1e872-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="1e872-135">MinLength</span></span><br/>    | <span data-ttu-id="1e872-136">integer</span><span class="sxs-lookup"><span data-stu-id="1e872-136">integer</span></span><br/> | <span data-ttu-id="1e872-137">1</span><span class="sxs-lookup"><span data-stu-id="1e872-137">1</span></span><br/>               |
| <span data-ttu-id="1e872-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1e872-138">Mandatory</span></span><br/>    | <span data-ttu-id="1e872-139">string</span><span class="sxs-lookup"><span data-stu-id="1e872-139">string</span></span><br/>  | <span data-ttu-id="1e872-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="1e872-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1e872-141">Unité</span><span class="sxs-lookup"><span data-stu-id="1e872-141">UnitType</span></span><br/>     | <span data-ttu-id="1e872-142">string</span><span class="sxs-lookup"><span data-stu-id="1e872-142">string</span></span><br/>  | <span data-ttu-id="1e872-143">caractères</span><span class="sxs-lookup"><span data-stu-id="1e872-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1e872-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e872-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e872-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1e872-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




