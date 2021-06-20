---
description: En savoir plus sur l’élément DocumentCoverBackSource, qui spécifie la source d’une feuille de couverture principale personnalisée.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be16ab26a4aa3dd7109fee7d630ed354b9b686d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409352"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="64a50-103">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="64a50-103">DocumentCoverBackSource</span></span>

<span data-ttu-id="64a50-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="64a50-104">This topic is not current.</span></span> <span data-ttu-id="64a50-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="64a50-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="64a50-106">Spécifie la source d’une feuille de couverture principale personnalisée.</span><span class="sxs-lookup"><span data-stu-id="64a50-106">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="64a50-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="64a50-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="64a50-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="64a50-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="64a50-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="64a50-109">Element Information</span></span>



| <span data-ttu-id="64a50-110">Nom</span><span class="sxs-lookup"><span data-stu-id="64a50-110">Name</span></span> | <span data-ttu-id="64a50-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a50-111">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="64a50-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="64a50-112">Element Type</span></span> <br/>   | <span data-ttu-id="64a50-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="64a50-113">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="64a50-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="64a50-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="64a50-115">Document</span><span class="sxs-lookup"><span data-stu-id="64a50-115">Document</span></span><br/>                            |
| <span data-ttu-id="64a50-116">Notes</span><span class="sxs-lookup"><span data-stu-id="64a50-116">Notes</span></span> <br/>          | <span data-ttu-id="64a50-117">Lié à l’élément DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="64a50-117">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="64a50-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="64a50-118">Structure Content</span></span>

<span data-ttu-id="64a50-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="64a50-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="64a50-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="64a50-120">Structure Properties</span></span>

<span data-ttu-id="64a50-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="64a50-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="64a50-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="64a50-122">Property</span></span>                | <span data-ttu-id="64a50-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="64a50-123">xsi:type</span></span>           | <span data-ttu-id="64a50-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a50-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="64a50-125">DataType</span><span class="sxs-lookup"><span data-stu-id="64a50-125">DataType</span></span><br/>     | <span data-ttu-id="64a50-126">string</span><span class="sxs-lookup"><span data-stu-id="64a50-126">string</span></span><br/>  | <span data-ttu-id="64a50-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="64a50-127">xs:string</span></span><br/>       |
| <span data-ttu-id="64a50-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="64a50-128">DefaultValue</span></span><br/> | <span data-ttu-id="64a50-129">string</span><span class="sxs-lookup"><span data-stu-id="64a50-129">string</span></span><br/>  | <span data-ttu-id="64a50-130">non défini</span><span class="sxs-lookup"><span data-stu-id="64a50-130">undefined</span></span><br/>       |
| <span data-ttu-id="64a50-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="64a50-131">MaxLength</span></span><br/>    | <span data-ttu-id="64a50-132">entier</span><span class="sxs-lookup"><span data-stu-id="64a50-132">integer</span></span><br/> | <span data-ttu-id="64a50-133">non défini</span><span class="sxs-lookup"><span data-stu-id="64a50-133">undefined</span></span><br/>       |
| <span data-ttu-id="64a50-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="64a50-134">MinLength</span></span><br/>    | <span data-ttu-id="64a50-135">integer</span><span class="sxs-lookup"><span data-stu-id="64a50-135">integer</span></span><br/> | <span data-ttu-id="64a50-136">1</span><span class="sxs-lookup"><span data-stu-id="64a50-136">1</span></span><br/>               |
| <span data-ttu-id="64a50-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="64a50-137">Mandatory</span></span><br/>    | <span data-ttu-id="64a50-138">string</span><span class="sxs-lookup"><span data-stu-id="64a50-138">string</span></span><br/>  | <span data-ttu-id="64a50-139">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="64a50-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="64a50-140">Unité</span><span class="sxs-lookup"><span data-stu-id="64a50-140">UnitType</span></span><br/>     | <span data-ttu-id="64a50-141">string</span><span class="sxs-lookup"><span data-stu-id="64a50-141">string</span></span><br/>  | <span data-ttu-id="64a50-142">caractères</span><span class="sxs-lookup"><span data-stu-id="64a50-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="64a50-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64a50-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64a50-144">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="64a50-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




