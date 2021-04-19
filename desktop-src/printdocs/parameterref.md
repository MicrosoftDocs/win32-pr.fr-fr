---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106539395"
---
# <a name="parameterref"></a><span data-ttu-id="3d830-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="3d830-104">ParameterRef</span></span>

<span data-ttu-id="3d830-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="3d830-105">This topic is not current.</span></span> <span data-ttu-id="3d830-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3d830-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3d830-107">Un élément ParameterRef définit une référence à un élément ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="3d830-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="3d830-108">Un élément ScoredProperty qui contient un élément ParameterRef n’a pas d’élément de valeur explicitement défini.</span><span class="sxs-lookup"><span data-stu-id="3d830-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="3d830-109">Au lieu de cela, l’élément ScoredProperty reçoit sa valeur de l’élément ParameterInit référencé par un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="3d830-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="3d830-110">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="3d830-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="3d830-111">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="3d830-111">XML Attributes</span></span>

<span data-ttu-id="3d830-112">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="3d830-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="3d830-113">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="3d830-113">XML Attribute</span></span>   | <span data-ttu-id="3d830-114">Détails</span><span class="sxs-lookup"><span data-stu-id="3d830-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d830-115">name</span><span class="sxs-lookup"><span data-stu-id="3d830-115">name</span></span><br/> | <span data-ttu-id="3d830-116">Contient l’attribut Name de l’élément ParameterDef référencé dans le contexte du document actif.</span><span class="sxs-lookup"><span data-stu-id="3d830-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="3d830-117">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="3d830-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="3d830-118">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3d830-118">Element Information</span></span>

<span data-ttu-id="3d830-119">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="3d830-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="3d830-120">Category</span><span class="sxs-lookup"><span data-stu-id="3d830-120">Category</span></span>                   | <span data-ttu-id="3d830-121">Détails</span><span class="sxs-lookup"><span data-stu-id="3d830-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d830-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3d830-122">Parent elements</span></span><br/> | <span data-ttu-id="3d830-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="3d830-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="3d830-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3d830-124">Child elements</span></span><br/>  | <span data-ttu-id="3d830-125">Aucun autorisé.</span><span class="sxs-lookup"><span data-stu-id="3d830-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="3d830-126">Élément This</span><span class="sxs-lookup"><span data-stu-id="3d830-126">This element</span></span><br/>    | <span data-ttu-id="3d830-127">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="3d830-127">No character data is permitted.</span></span><br/> <span data-ttu-id="3d830-128">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="3d830-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="3d830-129">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="3d830-129">Configuration Dependencies</span></span>

<span data-ttu-id="3d830-130">Les éléments ParameterRef ne peuvent pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="3d830-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="3d830-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="3d830-131">Example</span></span>

<span data-ttu-id="3d830-132">L’exemple suivant illustre l’utilisation d’éléments ParameterRef pour permettre aux utilisateurs d’entrer des paramètres de taille de média personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3d830-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="3d830-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d830-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d830-134">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3d830-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




