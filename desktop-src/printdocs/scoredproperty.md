---
description: Recherche des informations sur l’élément ScoredProperty. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119114"
---
# <a name="scoredproperty"></a><span data-ttu-id="314e3-105">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="314e3-105">ScoredProperty</span></span>

<span data-ttu-id="314e3-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="314e3-106">This topic is not current.</span></span> <span data-ttu-id="314e3-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="314e3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="314e3-108">Un élément ScoredProperty déclare une propriété qui est intrinsèque à une définition d’option.</span><span class="sxs-lookup"><span data-stu-id="314e3-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="314e3-109">Ces propriétés doivent être comparées lors de l’évaluation de la précision qu’une option demandée correspond à une option prise en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="314e3-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="314e3-110">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="314e3-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="314e3-111">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="314e3-111">XML Attributes</span></span>

<span data-ttu-id="314e3-112">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="314e3-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="314e3-113">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="314e3-113">XML Attribute</span></span>   | <span data-ttu-id="314e3-114">Détails</span><span class="sxs-lookup"><span data-stu-id="314e3-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314e3-115">name</span><span class="sxs-lookup"><span data-stu-id="314e3-115">name</span></span><br/> | <span data-ttu-id="314e3-116">Contient l’attribut Name de ScoredProperty, soit une propriété standard, soit une propriété définie en privé.</span><span class="sxs-lookup"><span data-stu-id="314e3-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="314e3-117">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="314e3-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="314e3-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="314e3-118">Element Information</span></span>

<span data-ttu-id="314e3-119">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="314e3-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="314e3-120">Category</span><span class="sxs-lookup"><span data-stu-id="314e3-120">Category</span></span>                   | <span data-ttu-id="314e3-121">Détails</span><span class="sxs-lookup"><span data-stu-id="314e3-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314e3-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="314e3-122">Parent elements</span></span><br/> | <span data-ttu-id="314e3-123">*Option*</span><span class="sxs-lookup"><span data-stu-id="314e3-123">*Option*</span></span><br/> <span data-ttu-id="314e3-124">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="314e3-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="314e3-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="314e3-125">Child elements</span></span><br/>  | <span data-ttu-id="314e3-126">Vous pouvez soit utiliser</span><span class="sxs-lookup"><span data-stu-id="314e3-126">Either</span></span><br/> <span data-ttu-id="314e3-127">*ParameterRef* (un)</span><span class="sxs-lookup"><span data-stu-id="314e3-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="314e3-128">ou</span><span class="sxs-lookup"><span data-stu-id="314e3-128">or</span></span><br/> <span data-ttu-id="314e3-129">*Valeur* (un)</span><span class="sxs-lookup"><span data-stu-id="314e3-129">*Value* (one)</span></span><br/> <span data-ttu-id="314e3-130">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="314e3-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="314e3-131">*ScoredProperty* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="314e3-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="314e3-132">Élément This</span><span class="sxs-lookup"><span data-stu-id="314e3-132">This element</span></span><br/>    | <span data-ttu-id="314e3-133">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="314e3-133">No character data is permitted.</span></span><br/> <span data-ttu-id="314e3-134">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="314e3-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="314e3-135">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="314e3-135">Configuration Dependencies</span></span>

<span data-ttu-id="314e3-136">Un élément ScoredProperty ne peut pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="314e3-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="314e3-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="314e3-137">Example</span></span>

<span data-ttu-id="314e3-138">Déclarez un élément ScoredProperty nommé MediaSizeWidth avec la valeur 11.</span><span class="sxs-lookup"><span data-stu-id="314e3-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="314e3-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="314e3-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="314e3-140">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="314e3-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




