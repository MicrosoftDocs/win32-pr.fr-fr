---
description: En savoir plus sur l’élément JobComment, qui spécifie un commentaire associé au travail, par exemple, veuillez remettre à la salle 1234 une fois l’opération terminée.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409042"
---
# <a name="jobcomment"></a><span data-ttu-id="88713-103">JobComment</span><span class="sxs-lookup"><span data-stu-id="88713-103">JobComment</span></span>

<span data-ttu-id="88713-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="88713-104">This topic is not current.</span></span> <span data-ttu-id="88713-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="88713-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88713-106">Spécifie un commentaire associé au travail.</span><span class="sxs-lookup"><span data-stu-id="88713-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="88713-107">Exemple : « Veuillez remettre à la salle 1234 une fois terminé ».</span><span class="sxs-lookup"><span data-stu-id="88713-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="88713-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="88713-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88713-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="88713-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="88713-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="88713-110">Element Information</span></span>



| <span data-ttu-id="88713-111">Nom</span><span class="sxs-lookup"><span data-stu-id="88713-111">Name</span></span> | <span data-ttu-id="88713-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="88713-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="88713-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="88713-113">Element Type</span></span> <br/>   | <span data-ttu-id="88713-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="88713-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="88713-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="88713-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88713-116">Travail</span><span class="sxs-lookup"><span data-stu-id="88713-116">Job</span></span><br/>          |
| <span data-ttu-id="88713-117">Notes</span><span class="sxs-lookup"><span data-stu-id="88713-117">Notes</span></span> <br/>          | <span data-ttu-id="88713-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="88713-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="88713-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="88713-119">Structure Content</span></span>

<span data-ttu-id="88713-120">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="88713-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="88713-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="88713-121">Structure Properties</span></span>

<span data-ttu-id="88713-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="88713-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88713-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="88713-123">Property</span></span>                | <span data-ttu-id="88713-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="88713-124">xsi:type</span></span>           | <span data-ttu-id="88713-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="88713-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="88713-126">DataType</span><span class="sxs-lookup"><span data-stu-id="88713-126">DataType</span></span><br/>     | <span data-ttu-id="88713-127">string</span><span class="sxs-lookup"><span data-stu-id="88713-127">string</span></span><br/>  | <span data-ttu-id="88713-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="88713-128">xs:string</span></span><br/>       |
| <span data-ttu-id="88713-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="88713-129">DefaultValue</span></span><br/> | <span data-ttu-id="88713-130">string</span><span class="sxs-lookup"><span data-stu-id="88713-130">string</span></span><br/>  | <span data-ttu-id="88713-131">non défini</span><span class="sxs-lookup"><span data-stu-id="88713-131">undefined</span></span><br/>       |
| <span data-ttu-id="88713-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="88713-132">MaxLength</span></span><br/>    | <span data-ttu-id="88713-133">entier</span><span class="sxs-lookup"><span data-stu-id="88713-133">integer</span></span><br/> | <span data-ttu-id="88713-134">non défini</span><span class="sxs-lookup"><span data-stu-id="88713-134">undefined</span></span><br/>       |
| <span data-ttu-id="88713-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="88713-135">MinLength</span></span><br/>    | <span data-ttu-id="88713-136">integer</span><span class="sxs-lookup"><span data-stu-id="88713-136">integer</span></span><br/> | <span data-ttu-id="88713-137">1</span><span class="sxs-lookup"><span data-stu-id="88713-137">1</span></span><br/>               |
| <span data-ttu-id="88713-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="88713-138">Mandatory</span></span><br/>    | <span data-ttu-id="88713-139">string</span><span class="sxs-lookup"><span data-stu-id="88713-139">string</span></span><br/>  | <span data-ttu-id="88713-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="88713-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="88713-141">Unité</span><span class="sxs-lookup"><span data-stu-id="88713-141">UnitType</span></span><br/>     | <span data-ttu-id="88713-142">string</span><span class="sxs-lookup"><span data-stu-id="88713-142">string</span></span><br/>  | <span data-ttu-id="88713-143">caractères</span><span class="sxs-lookup"><span data-stu-id="88713-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="88713-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88713-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88713-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="88713-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




