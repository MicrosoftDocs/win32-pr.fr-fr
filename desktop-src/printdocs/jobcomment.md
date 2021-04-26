---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998346"
---
# <a name="jobcomment"></a><span data-ttu-id="63849-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="63849-104">JobComment</span></span>

<span data-ttu-id="63849-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="63849-105">This topic is not current.</span></span> <span data-ttu-id="63849-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63849-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63849-107">Spécifie un commentaire associé au travail.</span><span class="sxs-lookup"><span data-stu-id="63849-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="63849-108">Exemple : « Veuillez remettre à la salle 1234 une fois terminé ».</span><span class="sxs-lookup"><span data-stu-id="63849-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="63849-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="63849-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63849-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="63849-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="63849-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="63849-111">Element Information</span></span>



| <span data-ttu-id="63849-112">Nom</span><span class="sxs-lookup"><span data-stu-id="63849-112">Name</span></span> | <span data-ttu-id="63849-113">Value</span><span class="sxs-lookup"><span data-stu-id="63849-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="63849-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="63849-114">Element Type</span></span> <br/>   | <span data-ttu-id="63849-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="63849-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="63849-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="63849-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63849-117">Travail</span><span class="sxs-lookup"><span data-stu-id="63849-117">Job</span></span><br/>          |
| <span data-ttu-id="63849-118">Notes</span><span class="sxs-lookup"><span data-stu-id="63849-118">Notes</span></span> <br/>          | <span data-ttu-id="63849-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="63849-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="63849-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="63849-120">Structure Content</span></span>

<span data-ttu-id="63849-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="63849-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="63849-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="63849-122">Structure Properties</span></span>

<span data-ttu-id="63849-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="63849-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63849-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="63849-124">Property</span></span>                | <span data-ttu-id="63849-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="63849-125">xsi:type</span></span>           | <span data-ttu-id="63849-126">Value</span><span class="sxs-lookup"><span data-stu-id="63849-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="63849-127">DataType</span><span class="sxs-lookup"><span data-stu-id="63849-127">DataType</span></span><br/>     | <span data-ttu-id="63849-128">string</span><span class="sxs-lookup"><span data-stu-id="63849-128">string</span></span><br/>  | <span data-ttu-id="63849-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="63849-129">xs:string</span></span><br/>       |
| <span data-ttu-id="63849-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="63849-130">DefaultValue</span></span><br/> | <span data-ttu-id="63849-131">string</span><span class="sxs-lookup"><span data-stu-id="63849-131">string</span></span><br/>  | <span data-ttu-id="63849-132">non défini</span><span class="sxs-lookup"><span data-stu-id="63849-132">undefined</span></span><br/>       |
| <span data-ttu-id="63849-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="63849-133">MaxLength</span></span><br/>    | <span data-ttu-id="63849-134">entier</span><span class="sxs-lookup"><span data-stu-id="63849-134">integer</span></span><br/> | <span data-ttu-id="63849-135">non défini</span><span class="sxs-lookup"><span data-stu-id="63849-135">undefined</span></span><br/>       |
| <span data-ttu-id="63849-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="63849-136">MinLength</span></span><br/>    | <span data-ttu-id="63849-137">integer</span><span class="sxs-lookup"><span data-stu-id="63849-137">integer</span></span><br/> | <span data-ttu-id="63849-138">1</span><span class="sxs-lookup"><span data-stu-id="63849-138">1</span></span><br/>               |
| <span data-ttu-id="63849-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="63849-139">Mandatory</span></span><br/>    | <span data-ttu-id="63849-140">string</span><span class="sxs-lookup"><span data-stu-id="63849-140">string</span></span><br/>  | <span data-ttu-id="63849-141">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="63849-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="63849-142">Unité</span><span class="sxs-lookup"><span data-stu-id="63849-142">UnitType</span></span><br/>     | <span data-ttu-id="63849-143">string</span><span class="sxs-lookup"><span data-stu-id="63849-143">string</span></span><br/>  | <span data-ttu-id="63849-144">caractères</span><span class="sxs-lookup"><span data-stu-id="63849-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="63849-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63849-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63849-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="63849-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




