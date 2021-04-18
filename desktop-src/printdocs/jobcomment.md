---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522901"
---
# <a name="jobcomment"></a><span data-ttu-id="95003-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="95003-104">JobComment</span></span>

<span data-ttu-id="95003-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="95003-105">This topic is not current.</span></span> <span data-ttu-id="95003-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="95003-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="95003-107">Spécifie un commentaire associé au travail.</span><span class="sxs-lookup"><span data-stu-id="95003-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="95003-108">Exemple : « Veuillez remettre à la salle 1234 une fois terminé ».</span><span class="sxs-lookup"><span data-stu-id="95003-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="95003-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="95003-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="95003-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="95003-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="95003-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="95003-111">Element Information</span></span>



| <span data-ttu-id="95003-112">Nom</span><span class="sxs-lookup"><span data-stu-id="95003-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="95003-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="95003-113">Element Type</span></span> <br/>   | <span data-ttu-id="95003-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="95003-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="95003-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="95003-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="95003-116">Travail</span><span class="sxs-lookup"><span data-stu-id="95003-116">Job</span></span><br/>          |
| <span data-ttu-id="95003-117">Notes</span><span class="sxs-lookup"><span data-stu-id="95003-117">Notes</span></span> <br/>          | <span data-ttu-id="95003-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="95003-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="95003-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="95003-119">Structure Content</span></span>

<span data-ttu-id="95003-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="95003-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="95003-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="95003-121">Structure Properties</span></span>

<span data-ttu-id="95003-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="95003-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="95003-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="95003-123">Property</span></span>                | <span data-ttu-id="95003-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="95003-124">xsi:type</span></span>           | <span data-ttu-id="95003-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="95003-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="95003-126">DataType</span><span class="sxs-lookup"><span data-stu-id="95003-126">DataType</span></span><br/>     | <span data-ttu-id="95003-127">string</span><span class="sxs-lookup"><span data-stu-id="95003-127">string</span></span><br/>  | <span data-ttu-id="95003-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="95003-128">xs:string</span></span><br/>       |
| <span data-ttu-id="95003-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="95003-129">DefaultValue</span></span><br/> | <span data-ttu-id="95003-130">string</span><span class="sxs-lookup"><span data-stu-id="95003-130">string</span></span><br/>  | <span data-ttu-id="95003-131">non défini</span><span class="sxs-lookup"><span data-stu-id="95003-131">undefined</span></span><br/>       |
| <span data-ttu-id="95003-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="95003-132">MaxLength</span></span><br/>    | <span data-ttu-id="95003-133">entier</span><span class="sxs-lookup"><span data-stu-id="95003-133">integer</span></span><br/> | <span data-ttu-id="95003-134">non défini</span><span class="sxs-lookup"><span data-stu-id="95003-134">undefined</span></span><br/>       |
| <span data-ttu-id="95003-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="95003-135">MinLength</span></span><br/>    | <span data-ttu-id="95003-136">integer</span><span class="sxs-lookup"><span data-stu-id="95003-136">integer</span></span><br/> | <span data-ttu-id="95003-137">1</span><span class="sxs-lookup"><span data-stu-id="95003-137">1</span></span><br/>               |
| <span data-ttu-id="95003-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="95003-138">Mandatory</span></span><br/>    | <span data-ttu-id="95003-139">string</span><span class="sxs-lookup"><span data-stu-id="95003-139">string</span></span><br/>  | <span data-ttu-id="95003-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="95003-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="95003-141">Unité</span><span class="sxs-lookup"><span data-stu-id="95003-141">UnitType</span></span><br/>     | <span data-ttu-id="95003-142">string</span><span class="sxs-lookup"><span data-stu-id="95003-142">string</span></span><br/>  | <span data-ttu-id="95003-143">caractères</span><span class="sxs-lookup"><span data-stu-id="95003-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="95003-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95003-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95003-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="95003-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




