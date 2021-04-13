---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211309"
---
# <a name="parameterinit"></a><span data-ttu-id="e471e-104">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="e471e-104">ParameterInit</span></span>

<span data-ttu-id="e471e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e471e-105">This topic is not current.</span></span> <span data-ttu-id="e471e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e471e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e471e-107">Définit une valeur pour une instance d’un élément ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="e471e-107">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="e471e-108">Un élément ParameterInit est la cible de la référence effectuée par un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="e471e-108">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="e471e-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="e471e-109">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="e471e-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="e471e-110">XML Attributes</span></span>

<span data-ttu-id="e471e-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="e471e-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="e471e-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="e471e-112">XML Attribute</span></span>   | <span data-ttu-id="e471e-113">Détails</span><span class="sxs-lookup"><span data-stu-id="e471e-113">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e471e-114">name</span><span class="sxs-lookup"><span data-stu-id="e471e-114">name</span></span><br/> | <span data-ttu-id="e471e-115">Contient l’attribut Name de l’élément ParameterDef qui doit être initialisé dans le contexte du document actif.</span><span class="sxs-lookup"><span data-stu-id="e471e-115">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="e471e-116">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="e471e-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="e471e-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e471e-117">Element Information</span></span>

<span data-ttu-id="e471e-118">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="e471e-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="e471e-119">Category</span><span class="sxs-lookup"><span data-stu-id="e471e-119">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e471e-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e471e-120">Parent elements</span></span><br/> | <span data-ttu-id="e471e-121">PrintTicket (racine PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="e471e-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="e471e-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e471e-122">Child elements</span></span><br/>  | <span data-ttu-id="e471e-123">Valeur (un)</span><span class="sxs-lookup"><span data-stu-id="e471e-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="e471e-124">Élément This</span><span class="sxs-lookup"><span data-stu-id="e471e-124">This element</span></span><br/>    | <span data-ttu-id="e471e-125">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="e471e-125">No character data is permitted.</span></span><br/> <span data-ttu-id="e471e-126">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="e471e-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="e471e-127">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="e471e-127">Configuration Dependencies</span></span>

<span data-ttu-id="e471e-128">None</span><span class="sxs-lookup"><span data-stu-id="e471e-128">None</span></span>

## <a name="example"></a><span data-ttu-id="e471e-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="e471e-129">Example</span></span>

<span data-ttu-id="e471e-130">L’exemple suivant initialise un paramètre avec la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="e471e-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="e471e-131">L’exemple de [ParameterDef](parameterdef.md) montre comment définir tous les éléments de propriété requis pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e471e-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="e471e-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e471e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e471e-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e471e-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




