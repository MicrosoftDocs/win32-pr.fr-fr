---
description: Lisez les informations de référence sur le paramètre PageCopies. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396684"
---
# <a name="pagecopies"></a><span data-ttu-id="1a9ad-105">PageCopies</span><span class="sxs-lookup"><span data-stu-id="1a9ad-105">PageCopies</span></span>

<span data-ttu-id="1a9ad-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-106">This topic is not current.</span></span> <span data-ttu-id="1a9ad-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1a9ad-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1a9ad-108">Spécifie le nombre de copies d’une page.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="1a9ad-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1a9ad-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a9ad-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1a9ad-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1a9ad-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1a9ad-111">Element Information</span></span>



| <span data-ttu-id="1a9ad-112">Nom</span><span class="sxs-lookup"><span data-stu-id="1a9ad-112">Name</span></span> | <span data-ttu-id="1a9ad-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a9ad-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="1a9ad-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="1a9ad-114">Element Type</span></span> <br/>   | <span data-ttu-id="1a9ad-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1a9ad-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="1a9ad-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="1a9ad-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1a9ad-117">Page</span><span class="sxs-lookup"><span data-stu-id="1a9ad-117">Page</span></span><br/>         |
| <span data-ttu-id="1a9ad-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1a9ad-118">Notes</span></span> <br/>          | <span data-ttu-id="1a9ad-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="1a9ad-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="1a9ad-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="1a9ad-120">Structure Content</span></span>

<span data-ttu-id="1a9ad-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="1a9ad-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1a9ad-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="1a9ad-122">Structure Properties</span></span>

<span data-ttu-id="1a9ad-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1a9ad-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="1a9ad-124">Property</span></span>                | <span data-ttu-id="1a9ad-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1a9ad-125">xsi:type</span></span>           | <span data-ttu-id="1a9ad-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a9ad-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="1a9ad-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1a9ad-127">DataType</span></span><br/>     | <span data-ttu-id="1a9ad-128">string</span><span class="sxs-lookup"><span data-stu-id="1a9ad-128">string</span></span><br/>  | <span data-ttu-id="1a9ad-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1a9ad-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="1a9ad-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1a9ad-130">DefaultValue</span></span><br/> | <span data-ttu-id="1a9ad-131">integer</span><span class="sxs-lookup"><span data-stu-id="1a9ad-131">integer</span></span><br/> | <span data-ttu-id="1a9ad-132">1</span><span class="sxs-lookup"><span data-stu-id="1a9ad-132">1</span></span><br/>                 |
| <span data-ttu-id="1a9ad-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1a9ad-133">MaxValue</span></span><br/>     | <span data-ttu-id="1a9ad-134">entier</span><span class="sxs-lookup"><span data-stu-id="1a9ad-134">integer</span></span><br/> | <span data-ttu-id="1a9ad-135">non défini</span><span class="sxs-lookup"><span data-stu-id="1a9ad-135">undefined</span></span><br/>         |
| <span data-ttu-id="1a9ad-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="1a9ad-136">MinValue</span></span><br/>     | <span data-ttu-id="1a9ad-137">integer</span><span class="sxs-lookup"><span data-stu-id="1a9ad-137">integer</span></span><br/> | <span data-ttu-id="1a9ad-138">1</span><span class="sxs-lookup"><span data-stu-id="1a9ad-138">1</span></span><br/>                 |
| <span data-ttu-id="1a9ad-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1a9ad-139">Mandatory</span></span><br/>    | <span data-ttu-id="1a9ad-140">string</span><span class="sxs-lookup"><span data-stu-id="1a9ad-140">string</span></span><br/>  | <span data-ttu-id="1a9ad-141">PSK : sans condition</span><span class="sxs-lookup"><span data-stu-id="1a9ad-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="1a9ad-142">Multiple</span><span class="sxs-lookup"><span data-stu-id="1a9ad-142">Multiple</span></span><br/>     | <span data-ttu-id="1a9ad-143">integer</span><span class="sxs-lookup"><span data-stu-id="1a9ad-143">integer</span></span><br/> | <span data-ttu-id="1a9ad-144">1</span><span class="sxs-lookup"><span data-stu-id="1a9ad-144">1</span></span><br/>                 |
| <span data-ttu-id="1a9ad-145">Unité</span><span class="sxs-lookup"><span data-stu-id="1a9ad-145">UnitType</span></span><br/>     | <span data-ttu-id="1a9ad-146">string</span><span class="sxs-lookup"><span data-stu-id="1a9ad-146">string</span></span><br/>  | <span data-ttu-id="1a9ad-147">copie</span><span class="sxs-lookup"><span data-stu-id="1a9ad-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="1a9ad-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a9ad-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a9ad-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1a9ad-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




