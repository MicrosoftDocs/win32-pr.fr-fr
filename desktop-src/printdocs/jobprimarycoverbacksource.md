---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2145bae0843323928d8a7d016fc61f10c0e388ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993976"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="f6a50-104">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="f6a50-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="f6a50-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="f6a50-105">This topic is not current.</span></span> <span data-ttu-id="f6a50-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f6a50-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f6a50-107">Spécifie la source d’une feuille principale personnalisée de couverture pour le travail.</span><span class="sxs-lookup"><span data-stu-id="f6a50-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="f6a50-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f6a50-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f6a50-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f6a50-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f6a50-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f6a50-110">Element Information</span></span>



| <span data-ttu-id="f6a50-111">Nom</span><span class="sxs-lookup"><span data-stu-id="f6a50-111">Name</span></span> | <span data-ttu-id="f6a50-112">Value</span><span class="sxs-lookup"><span data-stu-id="f6a50-112">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="f6a50-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="f6a50-113">Element Type</span></span> <br/>   | <span data-ttu-id="f6a50-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f6a50-114">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="f6a50-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="f6a50-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f6a50-116">Travail</span><span class="sxs-lookup"><span data-stu-id="f6a50-116">Job</span></span><br/>                            |
| <span data-ttu-id="f6a50-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f6a50-117">Notes</span></span> <br/>          | <span data-ttu-id="f6a50-118">Lié à l’élément JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="f6a50-118">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f6a50-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="f6a50-119">Structure Content</span></span>

<span data-ttu-id="f6a50-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="f6a50-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="f6a50-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="f6a50-121">Structure Properties</span></span>

<span data-ttu-id="f6a50-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="f6a50-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f6a50-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="f6a50-123">Property</span></span>                | <span data-ttu-id="f6a50-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f6a50-124">xsi:type</span></span>           | <span data-ttu-id="f6a50-125">Value</span><span class="sxs-lookup"><span data-stu-id="f6a50-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f6a50-126">DataType</span><span class="sxs-lookup"><span data-stu-id="f6a50-126">DataType</span></span><br/>     | <span data-ttu-id="f6a50-127">string</span><span class="sxs-lookup"><span data-stu-id="f6a50-127">string</span></span><br/>  | <span data-ttu-id="f6a50-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="f6a50-128">xs:string</span></span><br/>       |
| <span data-ttu-id="f6a50-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f6a50-129">DefaultValue</span></span><br/> | <span data-ttu-id="f6a50-130">string</span><span class="sxs-lookup"><span data-stu-id="f6a50-130">string</span></span><br/>  | <span data-ttu-id="f6a50-131">non défini</span><span class="sxs-lookup"><span data-stu-id="f6a50-131">undefined</span></span><br/>       |
| <span data-ttu-id="f6a50-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f6a50-132">MaxLength</span></span><br/>    | <span data-ttu-id="f6a50-133">entier</span><span class="sxs-lookup"><span data-stu-id="f6a50-133">integer</span></span><br/> | <span data-ttu-id="f6a50-134">non défini</span><span class="sxs-lookup"><span data-stu-id="f6a50-134">undefined</span></span><br/>       |
| <span data-ttu-id="f6a50-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="f6a50-135">MinLength</span></span><br/>    | <span data-ttu-id="f6a50-136">integer</span><span class="sxs-lookup"><span data-stu-id="f6a50-136">integer</span></span><br/> | <span data-ttu-id="f6a50-137">1</span><span class="sxs-lookup"><span data-stu-id="f6a50-137">1</span></span><br/>               |
| <span data-ttu-id="f6a50-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f6a50-138">Mandatory</span></span><br/>    | <span data-ttu-id="f6a50-139">string</span><span class="sxs-lookup"><span data-stu-id="f6a50-139">string</span></span><br/>  | <span data-ttu-id="f6a50-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="f6a50-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f6a50-141">Unité</span><span class="sxs-lookup"><span data-stu-id="f6a50-141">UnitType</span></span><br/>     | <span data-ttu-id="f6a50-142">string</span><span class="sxs-lookup"><span data-stu-id="f6a50-142">string</span></span><br/>  | <span data-ttu-id="f6a50-143">caractères</span><span class="sxs-lookup"><span data-stu-id="f6a50-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f6a50-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6a50-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a50-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="f6a50-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




