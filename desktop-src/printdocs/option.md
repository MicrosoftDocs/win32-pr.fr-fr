---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106525815"
---
# <a name="option"></a><span data-ttu-id="9ca84-104">Option</span><span class="sxs-lookup"><span data-stu-id="9ca84-104">Option</span></span>

<span data-ttu-id="9ca84-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9ca84-105">This topic is not current.</span></span> <span data-ttu-id="9ca84-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9ca84-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9ca84-107">Un élément option contient tous les éléments Property et ScoredProperty associés à cette option.</span><span class="sxs-lookup"><span data-stu-id="9ca84-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="9ca84-108">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="9ca84-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="9ca84-109">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="9ca84-109">XML Attributes</span></span>

<span data-ttu-id="9ca84-110">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="9ca84-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="9ca84-111">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="9ca84-111">XML Attribute</span></span>          | <span data-ttu-id="9ca84-112">Détails</span><span class="sxs-lookup"><span data-stu-id="9ca84-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca84-113">la</span><span class="sxs-lookup"><span data-stu-id="9ca84-113">constrained</span></span><br/> | <span data-ttu-id="9ca84-114">Cet attribut est facultatif pour un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9ca84-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="9ca84-115">Cet attribut indique si l’option est disponible pour la sélection ou l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9ca84-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="9ca84-116">Cet attribut XML peut être défini sur l’une des valeurs suivantes : None, PrintTicketSettings, AdminSetting ou DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="9ca84-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="9ca84-117">Voir [attributs XML](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="9ca84-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="9ca84-118">name</span><span class="sxs-lookup"><span data-stu-id="9ca84-118">name</span></span><br/>        | <span data-ttu-id="9ca84-119">Contient le nom de l’option, soit une option standard, soit une option définie en privé.</span><span class="sxs-lookup"><span data-stu-id="9ca84-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="9ca84-120">L’attribut XML est utilisé de cette façon afin de faire la différence entre les instances d’option.</span><span class="sxs-lookup"><span data-stu-id="9ca84-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="9ca84-121">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca84-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="9ca84-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9ca84-122">Element Information</span></span>

<span data-ttu-id="9ca84-123">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="9ca84-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="9ca84-124">Category</span><span class="sxs-lookup"><span data-stu-id="9ca84-124">Category</span></span>                   | <span data-ttu-id="9ca84-125">Détails</span><span class="sxs-lookup"><span data-stu-id="9ca84-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca84-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9ca84-126">Parent elements</span></span><br/> | <span data-ttu-id="9ca84-127">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="9ca84-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9ca84-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9ca84-128">Child elements</span></span><br/>  | <span data-ttu-id="9ca84-129">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="9ca84-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="9ca84-130">*ScoredProperty* (zéro ou plus pour les options avec l’attribut XML’name'; une ou plusieurs options pour les options qui n’utilisent pas l’attribut XML’name' \* )</span><span class="sxs-lookup"><span data-stu-id="9ca84-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="9ca84-131">\* seules les options publiques définies dans le schéma d’impression ne peuvent pas avoir d’attribut’name', tel que DocumentNUp)</span><span class="sxs-lookup"><span data-stu-id="9ca84-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="9ca84-132">Élément This</span><span class="sxs-lookup"><span data-stu-id="9ca84-132">This element</span></span><br/>    | <span data-ttu-id="9ca84-133">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="9ca84-133">No character data is permitted.</span></span><br/> <span data-ttu-id="9ca84-134">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="9ca84-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="9ca84-135">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="9ca84-135">Configuration Dependencies</span></span>

<span data-ttu-id="9ca84-136">Un élément de définition d’option ne peut pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="9ca84-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="9ca84-137">Utilisation des éléments</span><span class="sxs-lookup"><span data-stu-id="9ca84-137">Element Usage</span></span>

<span data-ttu-id="9ca84-138">L’objectif de l’élément option consiste à caractériser l’un des États qu’un attribut de configuration d’appareil, représenté par un élément de fonctionnalité, peut supposer.</span><span class="sxs-lookup"><span data-stu-id="9ca84-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="9ca84-139">Chaque définition d’élément option contient un ou plusieurs éléments ScoredProperty qui décrivent une caractéristique intrinsèque ou essentielle de cette option.</span><span class="sxs-lookup"><span data-stu-id="9ca84-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="9ca84-140">Pour faciliter la portabilité et la préservation de l’intention, le schéma d’impression définit de nombreux éléments de fonctionnalités courants et divers éléments d’option pour chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9ca84-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="9ca84-141">Il est donc important d’utiliser des éléments d’option d’impression définis par schéma, si possible, avant de créer vos propres définitions d’options.</span><span class="sxs-lookup"><span data-stu-id="9ca84-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="9ca84-142">La compréhension du processus de définition des éléments d’option fournit des informations utiles sur la façon dont le document PrintCapabilities et les des PrintTicket sont utilisés dans le Microsoft .NET Framework version 3,0 et l’architecture d’impression Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9ca84-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="9ca84-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ca84-143">Example</span></span>

<span data-ttu-id="9ca84-144">L’exemple suivant définit un nom pour l’option.</span><span class="sxs-lookup"><span data-stu-id="9ca84-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="9ca84-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ca84-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ca84-146">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9ca84-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




