---
description: En savoir plus sur l’élément JobCopiesAllDocuments, qui spécifie le nombre de copies d’un travail.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409032"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="b97ae-103">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="b97ae-103">JobCopiesAllDocuments</span></span>

<span data-ttu-id="b97ae-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b97ae-104">This topic is not current.</span></span> <span data-ttu-id="b97ae-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b97ae-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b97ae-106">Spécifie le nombre de copies d’un travail.</span><span class="sxs-lookup"><span data-stu-id="b97ae-106">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="b97ae-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b97ae-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b97ae-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b97ae-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b97ae-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b97ae-109">Element Information</span></span>



| <span data-ttu-id="b97ae-110">Nom</span><span class="sxs-lookup"><span data-stu-id="b97ae-110">Name</span></span> | <span data-ttu-id="b97ae-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97ae-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="b97ae-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="b97ae-112">Element Type</span></span> <br/>   | <span data-ttu-id="b97ae-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b97ae-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="b97ae-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="b97ae-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b97ae-115">Travail</span><span class="sxs-lookup"><span data-stu-id="b97ae-115">Job</span></span><br/>          |
| <span data-ttu-id="b97ae-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b97ae-116">Notes</span></span> <br/>          | <span data-ttu-id="b97ae-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="b97ae-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="b97ae-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="b97ae-118">Structure Content</span></span>

<span data-ttu-id="b97ae-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="b97ae-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b97ae-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="b97ae-120">Structure Properties</span></span>

<span data-ttu-id="b97ae-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="b97ae-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b97ae-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="b97ae-122">Property</span></span>                | <span data-ttu-id="b97ae-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b97ae-123">xsi:type</span></span>           | <span data-ttu-id="b97ae-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97ae-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="b97ae-125">DataType</span><span class="sxs-lookup"><span data-stu-id="b97ae-125">DataType</span></span><br/>     | <span data-ttu-id="b97ae-126">string</span><span class="sxs-lookup"><span data-stu-id="b97ae-126">string</span></span><br/>  | <span data-ttu-id="b97ae-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b97ae-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="b97ae-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b97ae-128">DefaultValue</span></span><br/> | <span data-ttu-id="b97ae-129">integer</span><span class="sxs-lookup"><span data-stu-id="b97ae-129">integer</span></span><br/> | <span data-ttu-id="b97ae-130">1</span><span class="sxs-lookup"><span data-stu-id="b97ae-130">1</span></span><br/>                 |
| <span data-ttu-id="b97ae-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="b97ae-131">MaxValue</span></span><br/>     | <span data-ttu-id="b97ae-132">entier</span><span class="sxs-lookup"><span data-stu-id="b97ae-132">integer</span></span><br/> | <span data-ttu-id="b97ae-133">non défini</span><span class="sxs-lookup"><span data-stu-id="b97ae-133">undefined</span></span><br/>         |
| <span data-ttu-id="b97ae-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="b97ae-134">MinValue</span></span><br/>     | <span data-ttu-id="b97ae-135">integer</span><span class="sxs-lookup"><span data-stu-id="b97ae-135">integer</span></span><br/> | <span data-ttu-id="b97ae-136">1</span><span class="sxs-lookup"><span data-stu-id="b97ae-136">1</span></span><br/>                 |
| <span data-ttu-id="b97ae-137">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b97ae-137">Mandatory</span></span><br/>    | <span data-ttu-id="b97ae-138">string</span><span class="sxs-lookup"><span data-stu-id="b97ae-138">string</span></span><br/>  | <span data-ttu-id="b97ae-139">PSK : sans condition</span><span class="sxs-lookup"><span data-stu-id="b97ae-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="b97ae-140">Multiple</span><span class="sxs-lookup"><span data-stu-id="b97ae-140">Multiple</span></span><br/>     | <span data-ttu-id="b97ae-141">integer</span><span class="sxs-lookup"><span data-stu-id="b97ae-141">integer</span></span><br/> | <span data-ttu-id="b97ae-142">1</span><span class="sxs-lookup"><span data-stu-id="b97ae-142">1</span></span><br/>                 |
| <span data-ttu-id="b97ae-143">Unité</span><span class="sxs-lookup"><span data-stu-id="b97ae-143">UnitType</span></span><br/>     | <span data-ttu-id="b97ae-144">string</span><span class="sxs-lookup"><span data-stu-id="b97ae-144">string</span></span><br/>  | <span data-ttu-id="b97ae-145">copie</span><span class="sxs-lookup"><span data-stu-id="b97ae-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="b97ae-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b97ae-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b97ae-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b97ae-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




