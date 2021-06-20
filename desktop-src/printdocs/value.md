---
description: En savoir plus sur l’élément Value, qui associe un littéral à un type. Le type de données de la valeur doit être String, Integer, Decimal ou QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272bee4d7a5f88899f83e439d8e1630b4026713d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405982"
---
# <a name="value"></a><span data-ttu-id="1170d-104">Valeur</span><span class="sxs-lookup"><span data-stu-id="1170d-104">Value</span></span>

<span data-ttu-id="1170d-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1170d-105">This topic is not current.</span></span> <span data-ttu-id="1170d-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1170d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1170d-107">Un élément de valeur associe un littéral à un type.</span><span class="sxs-lookup"><span data-stu-id="1170d-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="1170d-108">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="1170d-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="1170d-109">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="1170d-109">XML Attributes</span></span>

<span data-ttu-id="1170d-110">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="1170d-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="1170d-111">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="1170d-111">XML Attribute</span></span>       | <span data-ttu-id="1170d-112">Détails</span><span class="sxs-lookup"><span data-stu-id="1170d-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1170d-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1170d-113">xsi:type</span></span><br/> | <span data-ttu-id="1170d-114">Spécifie le type de données de la valeur, qui doit être l’un des types définis par XSD suivants : String, Integer, Decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="1170d-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="1170d-115">Si elle est manquante, le type de données par défaut est String.</span><span class="sxs-lookup"><span data-stu-id="1170d-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="1170d-116">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="1170d-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="1170d-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1170d-117">Element Information</span></span>

<span data-ttu-id="1170d-118">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="1170d-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="1170d-119">Category</span><span class="sxs-lookup"><span data-stu-id="1170d-119">Category</span></span>                   | <span data-ttu-id="1170d-120">Détails</span><span class="sxs-lookup"><span data-stu-id="1170d-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1170d-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1170d-121">Parent elements</span></span><br/> | <span data-ttu-id="1170d-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="1170d-122">ParameterInit</span></span> <br/> <span data-ttu-id="1170d-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="1170d-123">Property</span></span><br/> <span data-ttu-id="1170d-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="1170d-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="1170d-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1170d-125">Child elements</span></span><br/>  | <span data-ttu-id="1170d-126">Seul le contenu d’un caractère ou d’un entier est autorisé.</span><span class="sxs-lookup"><span data-stu-id="1170d-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="1170d-127">Élément This</span><span class="sxs-lookup"><span data-stu-id="1170d-127">This element</span></span><br/>    | <span data-ttu-id="1170d-128">Le contenu null est autorisé.</span><span class="sxs-lookup"><span data-stu-id="1170d-128">Null content is allowed.</span></span> <span data-ttu-id="1170d-129">Le contenu des caractères doit être conforme à la syntaxe définie par le type de données.</span><span class="sxs-lookup"><span data-stu-id="1170d-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="1170d-130">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="1170d-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="1170d-131">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="1170d-131">Configuration Dependencies</span></span>

<span data-ttu-id="1170d-132">Les éléments de valeur qui apparaissent dans l’élément ScoredProperty ne peuvent pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="1170d-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="1170d-133">Les éléments de valeur qui apparaissent dans les éléments de propriété peuvent avoir des dépendances arbitraires sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="1170d-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="1170d-134">Utilisation des éléments</span><span class="sxs-lookup"><span data-stu-id="1170d-134">Element Usage</span></span>

<span data-ttu-id="1170d-135">Un élément de valeur peut apparaître dans une propriété ou un élément ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="1170d-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="1170d-136">L’objectif de l’élément value est de représenter une valeur comme un type de données XML standard.</span><span class="sxs-lookup"><span data-stu-id="1170d-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="1170d-137">Le type de données est spécifié en tant qu’attribut XML de l’élément Value, xsi : type.</span><span class="sxs-lookup"><span data-stu-id="1170d-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="1170d-138">Notez que tous les types définis par XSD ou XML ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1170d-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="1170d-139">Pour obtenir la liste des types pris en charge, consultez [Résumé des types d’éléments](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="1170d-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="1170d-140">Un élément de valeur ne peut contenir que du contenu de caractères.</span><span class="sxs-lookup"><span data-stu-id="1170d-140">A Value element can contain only character content.</span></span> <span data-ttu-id="1170d-141">Rien d’autre ne peut apparaître en tant que contenu dans un élément de valeur.</span><span class="sxs-lookup"><span data-stu-id="1170d-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="1170d-142">Certaines propriétés définies par le schéma d’impression et les éléments ScoredProperty ne contiennent pas d’élément Value, car leur objectif est simplement d’être des parents des sous-propriétés.</span><span class="sxs-lookup"><span data-stu-id="1170d-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="1170d-143">Vous ne devez pas ajouter un élément de valeur à ces propriétés, comme celles-ci, les propriétés qui ne contiennent pas d’élément de valeur.</span><span class="sxs-lookup"><span data-stu-id="1170d-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="1170d-144">Pour se conformer à l’infrastructure du schéma d’impression, qui nécessite la présence d’un ou de plusieurs éléments de valeur dans les éléments qui prennent en charge des valeurs, une valeur absente ou non définie doit être représentée en présentant l’élément de valeur comme élément vide ; autrement dit, comme</span><span class="sxs-lookup"><span data-stu-id="1170d-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="1170d-145">.</span><span class="sxs-lookup"><span data-stu-id="1170d-145">.</span></span>

## <a name="example"></a><span data-ttu-id="1170d-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="1170d-146">Example</span></span>

<span data-ttu-id="1170d-147">Définissez une valeur de type Decimal et initialisez-la sur « 128,5 ».</span><span class="sxs-lookup"><span data-stu-id="1170d-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="1170d-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1170d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1170d-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1170d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




