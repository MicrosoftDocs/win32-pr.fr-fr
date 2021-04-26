---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6547ac2dc2c3f91ea4d0ebeea87622c790ae7d4d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996276"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="a4fbd-104">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="a4fbd-104">DocumentCoverBackSource</span></span>

<span data-ttu-id="a4fbd-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a4fbd-105">This topic is not current.</span></span> <span data-ttu-id="a4fbd-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a4fbd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4fbd-107">Spécifie la source d’une feuille de couverture principale personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a4fbd-107">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="a4fbd-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a4fbd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4fbd-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a4fbd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a4fbd-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a4fbd-110">Element Information</span></span>



| <span data-ttu-id="a4fbd-111">Nom</span><span class="sxs-lookup"><span data-stu-id="a4fbd-111">Name</span></span> | <span data-ttu-id="a4fbd-112">Value</span><span class="sxs-lookup"><span data-stu-id="a4fbd-112">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="a4fbd-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="a4fbd-113">Element Type</span></span> <br/>   | <span data-ttu-id="a4fbd-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a4fbd-114">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="a4fbd-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="a4fbd-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4fbd-116">Document</span><span class="sxs-lookup"><span data-stu-id="a4fbd-116">Document</span></span><br/>                            |
| <span data-ttu-id="a4fbd-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a4fbd-117">Notes</span></span> <br/>          | <span data-ttu-id="a4fbd-118">Lié à l’élément DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="a4fbd-118">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a4fbd-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="a4fbd-119">Structure Content</span></span>

<span data-ttu-id="a4fbd-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="a4fbd-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a4fbd-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="a4fbd-121">Structure Properties</span></span>

<span data-ttu-id="a4fbd-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="a4fbd-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4fbd-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="a4fbd-123">Property</span></span>                | <span data-ttu-id="a4fbd-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a4fbd-124">xsi:type</span></span>           | <span data-ttu-id="a4fbd-125">Value</span><span class="sxs-lookup"><span data-stu-id="a4fbd-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a4fbd-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a4fbd-126">DataType</span></span><br/>     | <span data-ttu-id="a4fbd-127">string</span><span class="sxs-lookup"><span data-stu-id="a4fbd-127">string</span></span><br/>  | <span data-ttu-id="a4fbd-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4fbd-128">xs:string</span></span><br/>       |
| <span data-ttu-id="a4fbd-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a4fbd-129">DefaultValue</span></span><br/> | <span data-ttu-id="a4fbd-130">string</span><span class="sxs-lookup"><span data-stu-id="a4fbd-130">string</span></span><br/>  | <span data-ttu-id="a4fbd-131">non défini</span><span class="sxs-lookup"><span data-stu-id="a4fbd-131">undefined</span></span><br/>       |
| <span data-ttu-id="a4fbd-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a4fbd-132">MaxLength</span></span><br/>    | <span data-ttu-id="a4fbd-133">entier</span><span class="sxs-lookup"><span data-stu-id="a4fbd-133">integer</span></span><br/> | <span data-ttu-id="a4fbd-134">non défini</span><span class="sxs-lookup"><span data-stu-id="a4fbd-134">undefined</span></span><br/>       |
| <span data-ttu-id="a4fbd-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="a4fbd-135">MinLength</span></span><br/>    | <span data-ttu-id="a4fbd-136">integer</span><span class="sxs-lookup"><span data-stu-id="a4fbd-136">integer</span></span><br/> | <span data-ttu-id="a4fbd-137">1</span><span class="sxs-lookup"><span data-stu-id="a4fbd-137">1</span></span><br/>               |
| <span data-ttu-id="a4fbd-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a4fbd-138">Mandatory</span></span><br/>    | <span data-ttu-id="a4fbd-139">string</span><span class="sxs-lookup"><span data-stu-id="a4fbd-139">string</span></span><br/>  | <span data-ttu-id="a4fbd-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="a4fbd-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a4fbd-141">Unité</span><span class="sxs-lookup"><span data-stu-id="a4fbd-141">UnitType</span></span><br/>     | <span data-ttu-id="a4fbd-142">string</span><span class="sxs-lookup"><span data-stu-id="a4fbd-142">string</span></span><br/>  | <span data-ttu-id="a4fbd-143">caractères</span><span class="sxs-lookup"><span data-stu-id="a4fbd-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a4fbd-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4fbd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4fbd-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a4fbd-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




