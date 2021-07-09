---
description: Obtenir des informations sur l’élément option. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549377"
---
# <a name="option"></a><span data-ttu-id="3604c-105">Option</span><span class="sxs-lookup"><span data-stu-id="3604c-105">Option</span></span>

<span data-ttu-id="3604c-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="3604c-106">This topic is not current.</span></span> <span data-ttu-id="3604c-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3604c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3604c-108">Un élément option contient tous les éléments Property et ScoredProperty associés à cette option.</span><span class="sxs-lookup"><span data-stu-id="3604c-108">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="3604c-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="3604c-109">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="3604c-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="3604c-110">XML Attributes</span></span>

<span data-ttu-id="3604c-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="3604c-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="3604c-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="3604c-112">XML Attribute</span></span>          | <span data-ttu-id="3604c-113">Détails</span><span class="sxs-lookup"><span data-stu-id="3604c-113">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3604c-114">la</span><span class="sxs-lookup"><span data-stu-id="3604c-114">constrained</span></span><br/> | <span data-ttu-id="3604c-115">Cet attribut est facultatif pour un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3604c-115">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="3604c-116">Cet attribut indique si l’option est disponible pour la sélection ou l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3604c-116">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="3604c-117">Cet attribut XML peut être défini sur l’une des valeurs suivantes : None, PrintTicketSettings, AdminSetting ou DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="3604c-117">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="3604c-118">Voir [attributs XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="3604c-118">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="3604c-119">name</span><span class="sxs-lookup"><span data-stu-id="3604c-119">name</span></span><br/>        | <span data-ttu-id="3604c-120">Contient le nom de l’option, soit une option standard, soit une option définie en privé.</span><span class="sxs-lookup"><span data-stu-id="3604c-120">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="3604c-121">L’attribut XML est utilisé de cette façon afin de faire la différence entre les instances d’option.</span><span class="sxs-lookup"><span data-stu-id="3604c-121">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="3604c-122">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="3604c-122">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="3604c-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3604c-123">Element Information</span></span>

<span data-ttu-id="3604c-124">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="3604c-124">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="3604c-125">Category</span><span class="sxs-lookup"><span data-stu-id="3604c-125">Category</span></span>                   | <span data-ttu-id="3604c-126">Détails</span><span class="sxs-lookup"><span data-stu-id="3604c-126">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3604c-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3604c-127">Parent elements</span></span><br/> | <span data-ttu-id="3604c-128">Composant</span><span class="sxs-lookup"><span data-stu-id="3604c-128">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3604c-129">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3604c-129">Child elements</span></span><br/>  | <span data-ttu-id="3604c-130">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="3604c-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="3604c-131">*ScoredProperty* (zéro ou plus pour les options avec l’attribut XML’name'; une ou plusieurs options pour les options qui n’utilisent pas l’attribut XML’name' \* )</span><span class="sxs-lookup"><span data-stu-id="3604c-131">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="3604c-132">\* seules les options publiques définies dans le schéma d’impression ne peuvent pas avoir d’attribut’name', tel que DocumentNUp)</span><span class="sxs-lookup"><span data-stu-id="3604c-132">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="3604c-133">Élément This</span><span class="sxs-lookup"><span data-stu-id="3604c-133">This element</span></span><br/>    | <span data-ttu-id="3604c-134">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="3604c-134">No character data is permitted.</span></span><br/> <span data-ttu-id="3604c-135">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="3604c-135">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="3604c-136">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="3604c-136">Configuration Dependencies</span></span>

<span data-ttu-id="3604c-137">Un élément de définition d’option ne peut pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="3604c-137">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="3604c-138">Utilisation des éléments</span><span class="sxs-lookup"><span data-stu-id="3604c-138">Element Usage</span></span>

<span data-ttu-id="3604c-139">L’objectif de l’élément option consiste à caractériser l’un des États qu’un attribut de configuration d’appareil, représenté par un élément de fonctionnalité, peut supposer.</span><span class="sxs-lookup"><span data-stu-id="3604c-139">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="3604c-140">Chaque définition d’élément option contient un ou plusieurs éléments ScoredProperty qui décrivent une caractéristique intrinsèque ou essentielle de cette option.</span><span class="sxs-lookup"><span data-stu-id="3604c-140">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="3604c-141">Pour faciliter la portabilité et la préservation de l’intention, le schéma d’impression définit de nombreux éléments de fonctionnalités courants et divers éléments d’option pour chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="3604c-141">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="3604c-142">Il est donc important d’utiliser des éléments d’option d’impression définis par schéma, si possible, avant de créer vos propres définitions d’options.</span><span class="sxs-lookup"><span data-stu-id="3604c-142">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="3604c-143">la compréhension du processus de définition des éléments d’Option fournit des insights utiles sur la façon dont le document PrintCapabilities et les des printticket sont utilisés dans les architectures d’impression Microsoft .NET Framework version 3,0 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3604c-143">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="3604c-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="3604c-144">Example</span></span>

<span data-ttu-id="3604c-145">L’exemple suivant définit un nom pour l’option.</span><span class="sxs-lookup"><span data-stu-id="3604c-145">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="3604c-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3604c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3604c-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3604c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




