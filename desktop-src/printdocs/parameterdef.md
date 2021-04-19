---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106538271"
---
# <a name="parameterdef"></a><span data-ttu-id="b5c71-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="b5c71-104">ParameterDef</span></span>

<span data-ttu-id="b5c71-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b5c71-105">This topic is not current.</span></span> <span data-ttu-id="b5c71-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b5c71-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b5c71-107">Un élément ParameterDef définit les caractéristiques valides de l’entrée de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5c71-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="b5c71-108">La valeur est entrée au moyen d’un élément ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="b5c71-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="b5c71-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="b5c71-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="b5c71-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="b5c71-110">XML Attributes</span></span>

<span data-ttu-id="b5c71-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="b5c71-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="b5c71-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="b5c71-112">XML Attribute</span></span>   | <span data-ttu-id="b5c71-113">Détails</span><span class="sxs-lookup"><span data-stu-id="b5c71-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c71-114">name</span><span class="sxs-lookup"><span data-stu-id="b5c71-114">name</span></span><br/> | <span data-ttu-id="b5c71-115">Définit un nom unique pour le paramètre dans le contexte du document actif.</span><span class="sxs-lookup"><span data-stu-id="b5c71-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="b5c71-116">Les attributs de nom de ParameterDef dupliqués rendent le document PrintCapabilities non valide.</span><span class="sxs-lookup"><span data-stu-id="b5c71-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="b5c71-117">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="b5c71-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="b5c71-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b5c71-118">Element Information</span></span>

<span data-ttu-id="b5c71-119">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="b5c71-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5c71-120">Category</span><span class="sxs-lookup"><span data-stu-id="b5c71-120">Category</span></span></th>
<th><span data-ttu-id="b5c71-121">Détails</span><span class="sxs-lookup"><span data-stu-id="b5c71-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5c71-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b5c71-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="b5c71-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b5c71-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5c71-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b5c71-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="b5c71-125">Property (un ou plusieurs) ;</span><span class="sxs-lookup"><span data-stu-id="b5c71-125">Property (one or more)</span></span><br/> <span data-ttu-id="b5c71-126">Les éléments de propriété standard suivants doivent apparaître en tant que contenu d’un élément ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="b5c71-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="b5c71-127">DataType</span><span class="sxs-lookup"><span data-stu-id="b5c71-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="b5c71-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b5c71-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="b5c71-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b5c71-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="b5c71-130">MaxLength ou MaxValue</span><span class="sxs-lookup"><span data-stu-id="b5c71-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="b5c71-131">MinLength ou MinValue</span><span class="sxs-lookup"><span data-stu-id="b5c71-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="b5c71-132">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="b5c71-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="b5c71-133">Unité</span><span class="sxs-lookup"><span data-stu-id="b5c71-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5c71-134">Élément This</span><span class="sxs-lookup"><span data-stu-id="b5c71-134">This element</span></span><br/></td>
<td><span data-ttu-id="b5c71-135">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="b5c71-135">No character data is permitted.</span></span><br/> <span data-ttu-id="b5c71-136">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="b5c71-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b5c71-137">\*Obligatoire lorsque DataType est un entier ou un nombre décimal.</span><span class="sxs-lookup"><span data-stu-id="b5c71-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="b5c71-138">Facultatif quand DataType est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b5c71-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="b5c71-139">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="b5c71-139">Configuration Dependencies</span></span>

<span data-ttu-id="b5c71-140">Un ParameterDef et son contenu à n’importe quel niveau d’imbrication ne peuvent pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="b5c71-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="b5c71-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="b5c71-141">Example</span></span>

<span data-ttu-id="b5c71-142">L’exemple suivant définit tous les éléments de propriété requis pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5c71-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="b5c71-143">L’exemple de [ParameterInit](parameterinit.md) montre comment initialiser ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5c71-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="b5c71-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5c71-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c71-145">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b5c71-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




