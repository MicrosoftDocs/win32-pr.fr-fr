---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriété (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321722"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="41e47-104">Propriété (documents et impression)</span><span class="sxs-lookup"><span data-stu-id="41e47-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="41e47-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="41e47-105">This topic is not current.</span></span> <span data-ttu-id="41e47-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="41e47-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="41e47-107">Un élément de propriété déclare un appareil, une mise en forme de travail ou une autre propriété pertinente dont le nom est donné par son attribut de nom.</span><span class="sxs-lookup"><span data-stu-id="41e47-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="41e47-108">Un élément de valeur est utilisé pour assigner une valeur à la propriété.</span><span class="sxs-lookup"><span data-stu-id="41e47-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="41e47-109">Une propriété peut être complexe, contenant éventuellement plusieurs sous-propriétés.</span><span class="sxs-lookup"><span data-stu-id="41e47-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="41e47-110">Les sous-propriétés sont également représentées par des éléments de propriété.</span><span class="sxs-lookup"><span data-stu-id="41e47-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="41e47-111">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="41e47-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="41e47-112">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="41e47-112">XML Attributes</span></span>

<span data-ttu-id="41e47-113">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="41e47-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="41e47-114">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="41e47-114">XML Attribute</span></span>   | <span data-ttu-id="41e47-115">Détails</span><span class="sxs-lookup"><span data-stu-id="41e47-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e47-116">name</span><span class="sxs-lookup"><span data-stu-id="41e47-116">name</span></span><br/> | <span data-ttu-id="41e47-117">Contient l’attribut Name de la propriété, qui est soit une propriété standard, soit une propriété définie en privé.</span><span class="sxs-lookup"><span data-stu-id="41e47-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="41e47-118">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="41e47-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="41e47-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="41e47-119">Element Information</span></span>

<span data-ttu-id="41e47-120">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="41e47-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="41e47-121">Category</span><span class="sxs-lookup"><span data-stu-id="41e47-121">Category</span></span>                   | <span data-ttu-id="41e47-122">Détails</span><span class="sxs-lookup"><span data-stu-id="41e47-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e47-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="41e47-123">Parent elements</span></span><br/> | <span data-ttu-id="41e47-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="41e47-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="41e47-125">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="41e47-125">Feature</span></span><br/> <span data-ttu-id="41e47-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="41e47-126">PrintTicket</span></span><br/> <span data-ttu-id="41e47-127">Option</span><span class="sxs-lookup"><span data-stu-id="41e47-127">Option</span></span><br/> <span data-ttu-id="41e47-128">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="41e47-128">ParameterDef</span></span><br/> <span data-ttu-id="41e47-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="41e47-129">Property</span></span><br/> <span data-ttu-id="41e47-130">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="41e47-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="41e47-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="41e47-131">Child elements</span></span><br/>  | <span data-ttu-id="41e47-132">Le système n’affecte pas l’importance à l’ordre des éléments.</span><span class="sxs-lookup"><span data-stu-id="41e47-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="41e47-133">Si les clients choisissent d’ascriber une certaine importance dans l’ordre des éléments, ils sont libres de le faire.</span><span class="sxs-lookup"><span data-stu-id="41e47-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="41e47-134">*Property* (une ou plusieurs) *valeur* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="41e47-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="41e47-135">ou</span><span class="sxs-lookup"><span data-stu-id="41e47-135">or</span></span> <br/> <span data-ttu-id="41e47-136">*Valeur* de la *propriété* (zéro ou plus) (un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="41e47-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="41e47-137">Élément This</span><span class="sxs-lookup"><span data-stu-id="41e47-137">This element</span></span><br/>    | <span data-ttu-id="41e47-138">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="41e47-138">No character data is permitted.</span></span><br/> <span data-ttu-id="41e47-139">Les éléments de valeur enfants dupliqués qui sont des frères sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="41e47-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="41e47-140">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="41e47-140">Configuration Dependencies</span></span>

<span data-ttu-id="41e47-141">Une propriété peut avoir des dépendances de configuration, sauf lorsqu’elle apparaît dans un élément ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="41e47-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="41e47-142">Utilisation des éléments</span><span class="sxs-lookup"><span data-stu-id="41e47-142">Element Usage</span></span>

<span data-ttu-id="41e47-143">En plus d’apparaître dans les éléments de fonctionnalité et d’option, les éléments de propriété peuvent apparaître au niveau racine des technologies sous-jacentes respectives.</span><span class="sxs-lookup"><span data-stu-id="41e47-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="41e47-144">Le schéma d’impression définit un ensemble d’éléments de propriété qui peuvent être utilisés pour décrire un appareil de manière portable.</span><span class="sxs-lookup"><span data-stu-id="41e47-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="41e47-145">Toutefois, si ces propriétés sont insuffisantes pour vos besoins en tant que fournisseur PrintCapabilities (généralement parce que l’appareil pris en charge a de nouveaux aspects non anticipés par le schéma d’impression), vous pouvez introduire vos propres éléments de propriété privés.</span><span class="sxs-lookup"><span data-stu-id="41e47-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="41e47-146">Vous pouvez améliorer ou développer les informations fournies par une propriété publique en ajoutant une ou plusieurs sous-propriétés privées en tant que contenu d’élément de la propriété publique.</span><span class="sxs-lookup"><span data-stu-id="41e47-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="41e47-147">Les éléments de propriété sont définis à l’aide d’une balise d’élément XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="41e47-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="41e47-148">Un nom est attribué à chaque propriété au moyen de son attribut Name.</span><span class="sxs-lookup"><span data-stu-id="41e47-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="41e47-149">Le nom doit être un QName XML et doit être conforme à la Convention d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="41e47-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="41e47-150">Pour plus d’informations, consultez [attributs XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="41e47-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="41e47-151">L’attribut de nom de propriété et son emplacement dans la hiérarchie des éléments de propriété parents (s’il s’agit d’une sous-propriété) identifient de façon unique la propriété dans le document PrintCapabilities ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="41e47-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="41e47-152">Une propriété peut contenir un ou plusieurs éléments de valeur, ou un ou plusieurs éléments de propriété enfants (appelés sous-propriétés), ou une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="41e47-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="41e47-153">Les sous-propriétés sont utiles lorsque la propriété elle-même est composée de plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="41e47-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="41e47-154">Par exemple, une propriété « ConsumableColor » peut avoir des composants « C », « M » et « Y ».</span><span class="sxs-lookup"><span data-stu-id="41e47-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="41e47-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="41e47-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="41e47-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41e47-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41e47-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="41e47-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




