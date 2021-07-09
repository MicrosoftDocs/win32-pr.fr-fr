---
description: Obtenir des informations sur le paramètre DocumentCoverFrontSource. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb6ecb089eb271e0b8fff136e73a20194f0c8f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548757"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="f6584-105">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="f6584-105">DocumentCoverFrontSource</span></span>

<span data-ttu-id="f6584-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="f6584-106">This topic is not current.</span></span> <span data-ttu-id="f6584-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f6584-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f6584-108">Spécifie la source d’une feuille de couverture avant personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f6584-108">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="f6584-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f6584-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f6584-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f6584-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f6584-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f6584-111">Element Information</span></span>



| <span data-ttu-id="f6584-112">Nom</span><span class="sxs-lookup"><span data-stu-id="f6584-112">Name</span></span> | <span data-ttu-id="f6584-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6584-113">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="f6584-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="f6584-114">Element Type</span></span> <br/>   | <span data-ttu-id="f6584-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f6584-115">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="f6584-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="f6584-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f6584-117">Document</span><span class="sxs-lookup"><span data-stu-id="f6584-117">Document</span></span><br/>                             |
| <span data-ttu-id="f6584-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="f6584-118">Notes</span></span> <br/>          | <span data-ttu-id="f6584-119">Lié à l’élément DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="f6584-119">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f6584-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f6584-120">Structure Content</span></span>

<span data-ttu-id="f6584-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="f6584-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
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
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="f6584-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="f6584-122">Structure Properties</span></span>

<span data-ttu-id="f6584-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="f6584-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f6584-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="f6584-124">Property</span></span>                | <span data-ttu-id="f6584-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f6584-125">xsi:type</span></span>           | <span data-ttu-id="f6584-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6584-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f6584-127">DataType</span><span class="sxs-lookup"><span data-stu-id="f6584-127">DataType</span></span><br/>     | <span data-ttu-id="f6584-128">string</span><span class="sxs-lookup"><span data-stu-id="f6584-128">string</span></span><br/>  | <span data-ttu-id="f6584-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="f6584-129">xs:string</span></span><br/>       |
| <span data-ttu-id="f6584-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f6584-130">DefaultValue</span></span><br/> | <span data-ttu-id="f6584-131">string</span><span class="sxs-lookup"><span data-stu-id="f6584-131">string</span></span><br/>  | <span data-ttu-id="f6584-132">non défini</span><span class="sxs-lookup"><span data-stu-id="f6584-132">undefined</span></span><br/>       |
| <span data-ttu-id="f6584-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f6584-133">MaxLength</span></span><br/>    | <span data-ttu-id="f6584-134">entier</span><span class="sxs-lookup"><span data-stu-id="f6584-134">integer</span></span><br/> | <span data-ttu-id="f6584-135">non défini</span><span class="sxs-lookup"><span data-stu-id="f6584-135">undefined</span></span><br/>       |
| <span data-ttu-id="f6584-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="f6584-136">MinLength</span></span><br/>    | <span data-ttu-id="f6584-137">integer</span><span class="sxs-lookup"><span data-stu-id="f6584-137">integer</span></span><br/> | <span data-ttu-id="f6584-138">1</span><span class="sxs-lookup"><span data-stu-id="f6584-138">1</span></span><br/>               |
| <span data-ttu-id="f6584-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f6584-139">Mandatory</span></span><br/>    | <span data-ttu-id="f6584-140">string</span><span class="sxs-lookup"><span data-stu-id="f6584-140">string</span></span><br/>  | <span data-ttu-id="f6584-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="f6584-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f6584-142">Unité</span><span class="sxs-lookup"><span data-stu-id="f6584-142">UnitType</span></span><br/>     | <span data-ttu-id="f6584-143">string</span><span class="sxs-lookup"><span data-stu-id="f6584-143">string</span></span><br/>  | <span data-ttu-id="f6584-144">caractères</span><span class="sxs-lookup"><span data-stu-id="f6584-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f6584-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6584-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6584-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f6584-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




