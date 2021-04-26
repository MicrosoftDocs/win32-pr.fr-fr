---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b1fc822d27d104364c2414ca89cf1fdf30c7d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997666"
---
# <a name="pagecopies"></a><span data-ttu-id="4e082-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="4e082-104">PageCopies</span></span>

<span data-ttu-id="4e082-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="4e082-105">This topic is not current.</span></span> <span data-ttu-id="4e082-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4e082-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4e082-107">Spécifie le nombre de copies d’une page.</span><span class="sxs-lookup"><span data-stu-id="4e082-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="4e082-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4e082-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4e082-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4e082-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4e082-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4e082-110">Element Information</span></span>



| <span data-ttu-id="4e082-111">Nom</span><span class="sxs-lookup"><span data-stu-id="4e082-111">Name</span></span> | <span data-ttu-id="4e082-112">Value</span><span class="sxs-lookup"><span data-stu-id="4e082-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="4e082-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="4e082-113">Element Type</span></span> <br/>   | <span data-ttu-id="4e082-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4e082-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="4e082-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="4e082-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4e082-116">Page</span><span class="sxs-lookup"><span data-stu-id="4e082-116">Page</span></span><br/>         |
| <span data-ttu-id="4e082-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4e082-117">Notes</span></span> <br/>          | <span data-ttu-id="4e082-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="4e082-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="4e082-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4e082-119">Structure Content</span></span>

<span data-ttu-id="4e082-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="4e082-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
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

## <a name="structure-properties"></a><span data-ttu-id="4e082-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="4e082-121">Structure Properties</span></span>

<span data-ttu-id="4e082-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="4e082-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4e082-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="4e082-123">Property</span></span>                | <span data-ttu-id="4e082-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4e082-124">xsi:type</span></span>           | <span data-ttu-id="4e082-125">Value</span><span class="sxs-lookup"><span data-stu-id="4e082-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="4e082-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4e082-126">DataType</span></span><br/>     | <span data-ttu-id="4e082-127">string</span><span class="sxs-lookup"><span data-stu-id="4e082-127">string</span></span><br/>  | <span data-ttu-id="4e082-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4e082-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="4e082-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4e082-129">DefaultValue</span></span><br/> | <span data-ttu-id="4e082-130">integer</span><span class="sxs-lookup"><span data-stu-id="4e082-130">integer</span></span><br/> | <span data-ttu-id="4e082-131">1</span><span class="sxs-lookup"><span data-stu-id="4e082-131">1</span></span><br/>                 |
| <span data-ttu-id="4e082-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4e082-132">MaxValue</span></span><br/>     | <span data-ttu-id="4e082-133">entier</span><span class="sxs-lookup"><span data-stu-id="4e082-133">integer</span></span><br/> | <span data-ttu-id="4e082-134">non défini</span><span class="sxs-lookup"><span data-stu-id="4e082-134">undefined</span></span><br/>         |
| <span data-ttu-id="4e082-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="4e082-135">MinValue</span></span><br/>     | <span data-ttu-id="4e082-136">integer</span><span class="sxs-lookup"><span data-stu-id="4e082-136">integer</span></span><br/> | <span data-ttu-id="4e082-137">1</span><span class="sxs-lookup"><span data-stu-id="4e082-137">1</span></span><br/>                 |
| <span data-ttu-id="4e082-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4e082-138">Mandatory</span></span><br/>    | <span data-ttu-id="4e082-139">string</span><span class="sxs-lookup"><span data-stu-id="4e082-139">string</span></span><br/>  | <span data-ttu-id="4e082-140">PSK : sans condition</span><span class="sxs-lookup"><span data-stu-id="4e082-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="4e082-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="4e082-141">Multiple</span></span><br/>     | <span data-ttu-id="4e082-142">integer</span><span class="sxs-lookup"><span data-stu-id="4e082-142">integer</span></span><br/> | <span data-ttu-id="4e082-143">1</span><span class="sxs-lookup"><span data-stu-id="4e082-143">1</span></span><br/>                 |
| <span data-ttu-id="4e082-144">Unité</span><span class="sxs-lookup"><span data-stu-id="4e082-144">UnitType</span></span><br/>     | <span data-ttu-id="4e082-145">string</span><span class="sxs-lookup"><span data-stu-id="4e082-145">string</span></span><br/>  | <span data-ttu-id="4e082-146">copie</span><span class="sxs-lookup"><span data-stu-id="4e082-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="4e082-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e082-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e082-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="4e082-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




