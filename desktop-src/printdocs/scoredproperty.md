---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106539397"
---
# <a name="scoredproperty"></a><span data-ttu-id="961e3-104">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="961e3-104">ScoredProperty</span></span>

<span data-ttu-id="961e3-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="961e3-105">This topic is not current.</span></span> <span data-ttu-id="961e3-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="961e3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="961e3-107">Un élément ScoredProperty déclare une propriété qui est intrinsèque à une définition d’option.</span><span class="sxs-lookup"><span data-stu-id="961e3-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="961e3-108">Ces propriétés doivent être comparées lors de l’évaluation de la précision qu’une option demandée correspond à une option prise en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="961e3-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="961e3-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="961e3-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="961e3-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="961e3-110">XML Attributes</span></span>

<span data-ttu-id="961e3-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="961e3-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="961e3-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="961e3-112">XML Attribute</span></span>   | <span data-ttu-id="961e3-113">Détails</span><span class="sxs-lookup"><span data-stu-id="961e3-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961e3-114">name</span><span class="sxs-lookup"><span data-stu-id="961e3-114">name</span></span><br/> | <span data-ttu-id="961e3-115">Contient l’attribut Name de ScoredProperty, soit une propriété standard, soit une propriété définie en privé.</span><span class="sxs-lookup"><span data-stu-id="961e3-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="961e3-116">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="961e3-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="961e3-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="961e3-117">Element Information</span></span>

<span data-ttu-id="961e3-118">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="961e3-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="961e3-119">Category</span><span class="sxs-lookup"><span data-stu-id="961e3-119">Category</span></span>                   | <span data-ttu-id="961e3-120">Détails</span><span class="sxs-lookup"><span data-stu-id="961e3-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961e3-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="961e3-121">Parent elements</span></span><br/> | <span data-ttu-id="961e3-122">*Option*</span><span class="sxs-lookup"><span data-stu-id="961e3-122">*Option*</span></span><br/> <span data-ttu-id="961e3-123">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="961e3-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="961e3-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="961e3-124">Child elements</span></span><br/>  | <span data-ttu-id="961e3-125">Vous pouvez soit utiliser</span><span class="sxs-lookup"><span data-stu-id="961e3-125">Either</span></span><br/> <span data-ttu-id="961e3-126">*ParameterRef* (un)</span><span class="sxs-lookup"><span data-stu-id="961e3-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="961e3-127">ou</span><span class="sxs-lookup"><span data-stu-id="961e3-127">or</span></span><br/> <span data-ttu-id="961e3-128">*Valeur* (un)</span><span class="sxs-lookup"><span data-stu-id="961e3-128">*Value* (one)</span></span><br/> <span data-ttu-id="961e3-129">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="961e3-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="961e3-130">*ScoredProperty* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="961e3-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="961e3-131">Élément This</span><span class="sxs-lookup"><span data-stu-id="961e3-131">This element</span></span><br/>    | <span data-ttu-id="961e3-132">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="961e3-132">No character data is permitted.</span></span><br/> <span data-ttu-id="961e3-133">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="961e3-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="961e3-134">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="961e3-134">Configuration Dependencies</span></span>

<span data-ttu-id="961e3-135">Un élément ScoredProperty ne peut pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="961e3-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="961e3-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="961e3-136">Example</span></span>

<span data-ttu-id="961e3-137">Déclarez un élément ScoredProperty nommé MediaSizeWidth avec la valeur 11.</span><span class="sxs-lookup"><span data-stu-id="961e3-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="961e3-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="961e3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="961e3-139">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="961e3-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




