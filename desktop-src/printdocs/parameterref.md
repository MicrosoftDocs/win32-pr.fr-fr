---
description: Découvrez l’élément ParameterRef, qui définit une référence à un élément ParameterInit et comment il fonctionne avec ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407182"
---
# <a name="parameterref"></a><span data-ttu-id="89bce-103">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="89bce-103">ParameterRef</span></span>

<span data-ttu-id="89bce-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="89bce-104">This topic is not current.</span></span> <span data-ttu-id="89bce-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="89bce-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="89bce-106">Un élément ParameterRef définit une référence à un élément ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="89bce-106">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="89bce-107">Un élément ScoredProperty qui contient un élément ParameterRef n’a pas d’élément de valeur explicitement défini.</span><span class="sxs-lookup"><span data-stu-id="89bce-107">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="89bce-108">Au lieu de cela, l’élément ScoredProperty reçoit sa valeur de l’élément ParameterInit référencé par un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="89bce-108">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="89bce-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="89bce-109">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="89bce-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="89bce-110">XML Attributes</span></span>

<span data-ttu-id="89bce-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="89bce-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="89bce-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="89bce-112">XML Attribute</span></span>   | <span data-ttu-id="89bce-113">Détails</span><span class="sxs-lookup"><span data-stu-id="89bce-113">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89bce-114">name</span><span class="sxs-lookup"><span data-stu-id="89bce-114">name</span></span><br/> | <span data-ttu-id="89bce-115">Contient l’attribut Name de l’élément ParameterDef référencé dans le contexte du document actif.</span><span class="sxs-lookup"><span data-stu-id="89bce-115">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="89bce-116">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="89bce-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="89bce-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="89bce-117">Element Information</span></span>

<span data-ttu-id="89bce-118">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="89bce-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="89bce-119">Category</span><span class="sxs-lookup"><span data-stu-id="89bce-119">Category</span></span>                   | <span data-ttu-id="89bce-120">Détails</span><span class="sxs-lookup"><span data-stu-id="89bce-120">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89bce-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="89bce-121">Parent elements</span></span><br/> | <span data-ttu-id="89bce-122">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="89bce-122">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="89bce-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="89bce-123">Child elements</span></span><br/>  | <span data-ttu-id="89bce-124">Aucun autorisé.</span><span class="sxs-lookup"><span data-stu-id="89bce-124">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="89bce-125">Élément This</span><span class="sxs-lookup"><span data-stu-id="89bce-125">This element</span></span><br/>    | <span data-ttu-id="89bce-126">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="89bce-126">No character data is permitted.</span></span><br/> <span data-ttu-id="89bce-127">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="89bce-127">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="89bce-128">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="89bce-128">Configuration Dependencies</span></span>

<span data-ttu-id="89bce-129">Les éléments ParameterRef ne peuvent pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="89bce-129">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="89bce-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="89bce-130">Example</span></span>

<span data-ttu-id="89bce-131">L’exemple suivant illustre l’utilisation d’éléments ParameterRef pour permettre aux utilisateurs d’entrer des paramètres de taille de média personnalisés.</span><span class="sxs-lookup"><span data-stu-id="89bce-131">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="89bce-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89bce-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89bce-133">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="89bce-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




