---
description: En savoir plus sur l’élément JobPrimaryCoverBackSource, qui spécifie la source d’une feuille principale personnalisée de couverture pour le travail.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408692"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="17122-103">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="17122-103">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="17122-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="17122-104">This topic is not current.</span></span> <span data-ttu-id="17122-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="17122-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="17122-106">Spécifie la source d’une feuille principale personnalisée de couverture pour le travail.</span><span class="sxs-lookup"><span data-stu-id="17122-106">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="17122-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="17122-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="17122-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="17122-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="17122-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="17122-109">Element Information</span></span>



| <span data-ttu-id="17122-110">Nom</span><span class="sxs-lookup"><span data-stu-id="17122-110">Name</span></span> | <span data-ttu-id="17122-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="17122-111">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="17122-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="17122-112">Element Type</span></span> <br/>   | <span data-ttu-id="17122-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="17122-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="17122-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="17122-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="17122-115">Travail</span><span class="sxs-lookup"><span data-stu-id="17122-115">Job</span></span><br/>                            |
| <span data-ttu-id="17122-116">Notes</span><span class="sxs-lookup"><span data-stu-id="17122-116">Notes</span></span> <br/>          | <span data-ttu-id="17122-117">Lié à l’élément JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="17122-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="17122-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="17122-118">Structure Content</span></span>

<span data-ttu-id="17122-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="17122-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="17122-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="17122-120">Structure Properties</span></span>

<span data-ttu-id="17122-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="17122-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="17122-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="17122-122">Property</span></span>                | <span data-ttu-id="17122-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="17122-123">xsi:type</span></span>           | <span data-ttu-id="17122-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="17122-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="17122-125">DataType</span><span class="sxs-lookup"><span data-stu-id="17122-125">DataType</span></span><br/>     | <span data-ttu-id="17122-126">string</span><span class="sxs-lookup"><span data-stu-id="17122-126">string</span></span><br/>  | <span data-ttu-id="17122-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="17122-127">xs:string</span></span><br/>       |
| <span data-ttu-id="17122-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="17122-128">DefaultValue</span></span><br/> | <span data-ttu-id="17122-129">string</span><span class="sxs-lookup"><span data-stu-id="17122-129">string</span></span><br/>  | <span data-ttu-id="17122-130">non défini</span><span class="sxs-lookup"><span data-stu-id="17122-130">undefined</span></span><br/>       |
| <span data-ttu-id="17122-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="17122-131">MaxLength</span></span><br/>    | <span data-ttu-id="17122-132">entier</span><span class="sxs-lookup"><span data-stu-id="17122-132">integer</span></span><br/> | <span data-ttu-id="17122-133">non défini</span><span class="sxs-lookup"><span data-stu-id="17122-133">undefined</span></span><br/>       |
| <span data-ttu-id="17122-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="17122-134">MinLength</span></span><br/>    | <span data-ttu-id="17122-135">integer</span><span class="sxs-lookup"><span data-stu-id="17122-135">integer</span></span><br/> | <span data-ttu-id="17122-136">1</span><span class="sxs-lookup"><span data-stu-id="17122-136">1</span></span><br/>               |
| <span data-ttu-id="17122-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="17122-137">Mandatory</span></span><br/>    | <span data-ttu-id="17122-138">string</span><span class="sxs-lookup"><span data-stu-id="17122-138">string</span></span><br/>  | <span data-ttu-id="17122-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="17122-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="17122-140">Unité</span><span class="sxs-lookup"><span data-stu-id="17122-140">UnitType</span></span><br/>     | <span data-ttu-id="17122-141">string</span><span class="sxs-lookup"><span data-stu-id="17122-141">string</span></span><br/>  | <span data-ttu-id="17122-142">caractères</span><span class="sxs-lookup"><span data-stu-id="17122-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="17122-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17122-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17122-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="17122-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




