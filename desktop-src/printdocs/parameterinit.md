---
description: En savoir plus sur l’élément ParameterInit, qui définit une valeur pour une instance d’un élément ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e0cadbf26d6ff516ab0ace90165e11420a9b7
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118974"
---
# <a name="parameterinit"></a><span data-ttu-id="d9594-103">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="d9594-103">ParameterInit</span></span>

<span data-ttu-id="d9594-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d9594-104">This topic is not current.</span></span> <span data-ttu-id="d9594-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d9594-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d9594-106">Définit une valeur pour une instance d’un élément ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="d9594-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="d9594-107">Un élément ParameterInit est la cible de la référence effectuée par un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="d9594-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="d9594-108">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="d9594-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="d9594-109">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="d9594-109">XML Attributes</span></span>

<span data-ttu-id="d9594-110">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="d9594-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="d9594-111">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="d9594-111">XML Attribute</span></span>   | <span data-ttu-id="d9594-112">Détails</span><span class="sxs-lookup"><span data-stu-id="d9594-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9594-113">name</span><span class="sxs-lookup"><span data-stu-id="d9594-113">name</span></span><br/> | <span data-ttu-id="d9594-114">Contient l’attribut Name de l’élément ParameterDef qui doit être initialisé dans le contexte du document actif.</span><span class="sxs-lookup"><span data-stu-id="d9594-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="d9594-115">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d9594-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="d9594-116">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d9594-116">Element Information</span></span>

<span data-ttu-id="d9594-117">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="d9594-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="d9594-118">Category</span><span class="sxs-lookup"><span data-stu-id="d9594-118">Category</span></span>                   | <span data-ttu-id="d9594-119">Nom ou restriction</span><span class="sxs-lookup"><span data-stu-id="d9594-119">Name or restriction</span></span>                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9594-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d9594-120">Parent elements</span></span><br/> | <span data-ttu-id="d9594-121">PrintTicket (racine PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="d9594-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="d9594-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d9594-122">Child elements</span></span><br/>  | <span data-ttu-id="d9594-123">Valeur (un)</span><span class="sxs-lookup"><span data-stu-id="d9594-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="d9594-124">Élément This</span><span class="sxs-lookup"><span data-stu-id="d9594-124">This element</span></span><br/>    | <span data-ttu-id="d9594-125">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="d9594-125">No character data is permitted.</span></span><br/> <span data-ttu-id="d9594-126">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="d9594-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="d9594-127">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="d9594-127">Configuration Dependencies</span></span>

<span data-ttu-id="d9594-128">None</span><span class="sxs-lookup"><span data-stu-id="d9594-128">None</span></span>

## <a name="example"></a><span data-ttu-id="d9594-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9594-129">Example</span></span>

<span data-ttu-id="d9594-130">L’exemple suivant initialise un paramètre avec la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="d9594-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="d9594-131">L’exemple de [ParameterDef](parameterdef.md) montre comment définir tous les éléments de propriété requis pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d9594-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="d9594-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9594-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9594-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d9594-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




