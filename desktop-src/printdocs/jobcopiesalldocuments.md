---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f8be33f98b540cab56b88df49cfb1e3c067988
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761546"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="0c6bd-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="0c6bd-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="0c6bd-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0c6bd-105">This topic is not current.</span></span> <span data-ttu-id="0c6bd-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0c6bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c6bd-107">Spécifie le nombre de copies d’un travail.</span><span class="sxs-lookup"><span data-stu-id="0c6bd-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="0c6bd-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0c6bd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c6bd-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="0c6bd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0c6bd-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0c6bd-110">Element Information</span></span>



| <span data-ttu-id="0c6bd-111">Nom</span><span class="sxs-lookup"><span data-stu-id="0c6bd-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="0c6bd-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0c6bd-112">Element Type</span></span> <br/>   | <span data-ttu-id="0c6bd-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0c6bd-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="0c6bd-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0c6bd-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c6bd-115">Travail</span><span class="sxs-lookup"><span data-stu-id="0c6bd-115">Job</span></span><br/>          |
| <span data-ttu-id="0c6bd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0c6bd-116">Notes</span></span> <br/>          | <span data-ttu-id="0c6bd-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="0c6bd-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="0c6bd-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="0c6bd-118">Structure Content</span></span>

<span data-ttu-id="0c6bd-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="0c6bd-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="0c6bd-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="0c6bd-120">Structure Properties</span></span>

<span data-ttu-id="0c6bd-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0c6bd-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c6bd-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="0c6bd-122">Property</span></span>                | <span data-ttu-id="0c6bd-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0c6bd-123">xsi:type</span></span>           | <span data-ttu-id="0c6bd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c6bd-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="0c6bd-125">DataType</span><span class="sxs-lookup"><span data-stu-id="0c6bd-125">DataType</span></span><br/>     | <span data-ttu-id="0c6bd-126">string</span><span class="sxs-lookup"><span data-stu-id="0c6bd-126">string</span></span><br/>  | <span data-ttu-id="0c6bd-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0c6bd-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="0c6bd-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0c6bd-128">DefaultValue</span></span><br/> | <span data-ttu-id="0c6bd-129">integer</span><span class="sxs-lookup"><span data-stu-id="0c6bd-129">integer</span></span><br/> | <span data-ttu-id="0c6bd-130">1</span><span class="sxs-lookup"><span data-stu-id="0c6bd-130">1</span></span><br/>                 |
| <span data-ttu-id="0c6bd-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0c6bd-131">MaxValue</span></span><br/>     | <span data-ttu-id="0c6bd-132">entier</span><span class="sxs-lookup"><span data-stu-id="0c6bd-132">integer</span></span><br/> | <span data-ttu-id="0c6bd-133">non défini</span><span class="sxs-lookup"><span data-stu-id="0c6bd-133">undefined</span></span><br/>         |
| <span data-ttu-id="0c6bd-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="0c6bd-134">MinValue</span></span><br/>     | <span data-ttu-id="0c6bd-135">integer</span><span class="sxs-lookup"><span data-stu-id="0c6bd-135">integer</span></span><br/> | <span data-ttu-id="0c6bd-136">1</span><span class="sxs-lookup"><span data-stu-id="0c6bd-136">1</span></span><br/>                 |
| <span data-ttu-id="0c6bd-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0c6bd-137">Mandatory</span></span><br/>    | <span data-ttu-id="0c6bd-138">string</span><span class="sxs-lookup"><span data-stu-id="0c6bd-138">string</span></span><br/>  | <span data-ttu-id="0c6bd-139">PSK : sans condition</span><span class="sxs-lookup"><span data-stu-id="0c6bd-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="0c6bd-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="0c6bd-140">Multiple</span></span><br/>     | <span data-ttu-id="0c6bd-141">integer</span><span class="sxs-lookup"><span data-stu-id="0c6bd-141">integer</span></span><br/> | <span data-ttu-id="0c6bd-142">1</span><span class="sxs-lookup"><span data-stu-id="0c6bd-142">1</span></span><br/>                 |
| <span data-ttu-id="0c6bd-143">Unité</span><span class="sxs-lookup"><span data-stu-id="0c6bd-143">UnitType</span></span><br/>     | <span data-ttu-id="0c6bd-144">string</span><span class="sxs-lookup"><span data-stu-id="0c6bd-144">string</span></span><br/>  | <span data-ttu-id="0c6bd-145">copie</span><span class="sxs-lookup"><span data-stu-id="0c6bd-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="0c6bd-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c6bd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c6bd-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0c6bd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




