---
description: Obtenir des informations sur le paramètre JobErrorSheetSource. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656d71422c46800d6155c1dea1e221f9c6dfe021
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549387"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="d1b47-105">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="d1b47-105">JobErrorSheetSource</span></span>

<span data-ttu-id="d1b47-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d1b47-106">This topic is not current.</span></span> <span data-ttu-id="d1b47-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d1b47-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d1b47-108">Spécifie la source d’une feuille d’erreur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d1b47-108">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="d1b47-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d1b47-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d1b47-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="d1b47-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d1b47-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d1b47-111">Element Information</span></span>



| <span data-ttu-id="d1b47-112">Nom</span><span class="sxs-lookup"><span data-stu-id="d1b47-112">Name</span></span> | <span data-ttu-id="d1b47-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1b47-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="d1b47-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d1b47-114">Element Type</span></span> <br/>   | <span data-ttu-id="d1b47-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d1b47-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="d1b47-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d1b47-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d1b47-117">Document</span><span class="sxs-lookup"><span data-stu-id="d1b47-117">Document</span></span><br/>                        |
| <span data-ttu-id="d1b47-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1b47-118">Notes</span></span> <br/>          | <span data-ttu-id="d1b47-119">Lié à l’élément JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="d1b47-119">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d1b47-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="d1b47-120">Structure Content</span></span>

<span data-ttu-id="d1b47-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="d1b47-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d1b47-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="d1b47-122">Structure Properties</span></span>

<span data-ttu-id="d1b47-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d1b47-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d1b47-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="d1b47-124">Property</span></span>                | <span data-ttu-id="d1b47-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d1b47-125">xsi:type</span></span>           | <span data-ttu-id="d1b47-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1b47-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d1b47-127">DataType</span><span class="sxs-lookup"><span data-stu-id="d1b47-127">DataType</span></span><br/>     | <span data-ttu-id="d1b47-128">string</span><span class="sxs-lookup"><span data-stu-id="d1b47-128">string</span></span><br/>  | <span data-ttu-id="d1b47-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1b47-129">xs:string</span></span><br/>       |
| <span data-ttu-id="d1b47-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d1b47-130">DefaultValue</span></span><br/> | <span data-ttu-id="d1b47-131">string</span><span class="sxs-lookup"><span data-stu-id="d1b47-131">string</span></span><br/>  | <span data-ttu-id="d1b47-132">non défini</span><span class="sxs-lookup"><span data-stu-id="d1b47-132">undefined</span></span><br/>       |
| <span data-ttu-id="d1b47-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="d1b47-133">MaxLength</span></span><br/>    | <span data-ttu-id="d1b47-134">entier</span><span class="sxs-lookup"><span data-stu-id="d1b47-134">integer</span></span><br/> | <span data-ttu-id="d1b47-135">non défini</span><span class="sxs-lookup"><span data-stu-id="d1b47-135">undefined</span></span><br/>       |
| <span data-ttu-id="d1b47-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="d1b47-136">MinLength</span></span><br/>    | <span data-ttu-id="d1b47-137">integer</span><span class="sxs-lookup"><span data-stu-id="d1b47-137">integer</span></span><br/> | <span data-ttu-id="d1b47-138">1</span><span class="sxs-lookup"><span data-stu-id="d1b47-138">1</span></span><br/>               |
| <span data-ttu-id="d1b47-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d1b47-139">Mandatory</span></span><br/>    | <span data-ttu-id="d1b47-140">string</span><span class="sxs-lookup"><span data-stu-id="d1b47-140">string</span></span><br/>  | <span data-ttu-id="d1b47-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="d1b47-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d1b47-142">Unité</span><span class="sxs-lookup"><span data-stu-id="d1b47-142">UnitType</span></span><br/>     | <span data-ttu-id="d1b47-143">string</span><span class="sxs-lookup"><span data-stu-id="d1b47-143">string</span></span><br/>  | <span data-ttu-id="d1b47-144">caractères</span><span class="sxs-lookup"><span data-stu-id="d1b47-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="d1b47-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1b47-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1b47-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d1b47-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




