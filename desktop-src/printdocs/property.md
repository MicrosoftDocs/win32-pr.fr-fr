---
description: En savoir plus sur l’élément Property dans les documents et l’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriété (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120294"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="abc8a-105">Propriété (documents et impression)</span><span class="sxs-lookup"><span data-stu-id="abc8a-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="abc8a-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="abc8a-106">This topic is not current.</span></span> <span data-ttu-id="abc8a-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="abc8a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="abc8a-108">Un élément de propriété déclare un appareil, une mise en forme de travail ou une autre propriété pertinente dont le nom est donné par son attribut de nom.</span><span class="sxs-lookup"><span data-stu-id="abc8a-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="abc8a-109">Un élément de valeur est utilisé pour assigner une valeur à la propriété.</span><span class="sxs-lookup"><span data-stu-id="abc8a-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="abc8a-110">Une propriété peut être complexe, contenant éventuellement plusieurs sous-propriétés.</span><span class="sxs-lookup"><span data-stu-id="abc8a-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="abc8a-111">Les sous-propriétés sont également représentées par des éléments de propriété.</span><span class="sxs-lookup"><span data-stu-id="abc8a-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="abc8a-112">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="abc8a-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="abc8a-113">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="abc8a-113">XML Attributes</span></span>

<span data-ttu-id="abc8a-114">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="abc8a-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="abc8a-115">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="abc8a-115">XML Attribute</span></span>   | <span data-ttu-id="abc8a-116">Détails</span><span class="sxs-lookup"><span data-stu-id="abc8a-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc8a-117">name</span><span class="sxs-lookup"><span data-stu-id="abc8a-117">name</span></span><br/> | <span data-ttu-id="abc8a-118">Contient l’attribut Name de la propriété, qui est soit une propriété standard, soit une propriété définie en privé.</span><span class="sxs-lookup"><span data-stu-id="abc8a-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="abc8a-119">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="abc8a-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="abc8a-120">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="abc8a-120">Element Information</span></span>

<span data-ttu-id="abc8a-121">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="abc8a-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="abc8a-122">Category</span><span class="sxs-lookup"><span data-stu-id="abc8a-122">Category</span></span>                   | <span data-ttu-id="abc8a-123">Détails</span><span class="sxs-lookup"><span data-stu-id="abc8a-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc8a-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="abc8a-124">Parent elements</span></span><br/> | <span data-ttu-id="abc8a-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="abc8a-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="abc8a-126">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="abc8a-126">Feature</span></span><br/> <span data-ttu-id="abc8a-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="abc8a-127">PrintTicket</span></span><br/> <span data-ttu-id="abc8a-128">Option</span><span class="sxs-lookup"><span data-stu-id="abc8a-128">Option</span></span><br/> <span data-ttu-id="abc8a-129">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="abc8a-129">ParameterDef</span></span><br/> <span data-ttu-id="abc8a-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="abc8a-130">Property</span></span><br/> <span data-ttu-id="abc8a-131">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="abc8a-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="abc8a-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="abc8a-132">Child elements</span></span><br/>  | <span data-ttu-id="abc8a-133">Le système n’affecte pas l’importance à l’ordre des éléments.</span><span class="sxs-lookup"><span data-stu-id="abc8a-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="abc8a-134">Si les clients choisissent d’ascriber une certaine importance dans l’ordre des éléments, ils sont libres de le faire.</span><span class="sxs-lookup"><span data-stu-id="abc8a-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="abc8a-135">*Property* (une ou plusieurs) *valeur* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="abc8a-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="abc8a-136">ou</span><span class="sxs-lookup"><span data-stu-id="abc8a-136">or</span></span> <br/> <span data-ttu-id="abc8a-137">*Valeur* de la *propriété* (zéro ou plus) (un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="abc8a-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="abc8a-138">Élément This</span><span class="sxs-lookup"><span data-stu-id="abc8a-138">This element</span></span><br/>    | <span data-ttu-id="abc8a-139">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="abc8a-139">No character data is permitted.</span></span><br/> <span data-ttu-id="abc8a-140">Les éléments de valeur enfants dupliqués qui sont des frères sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="abc8a-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="abc8a-141">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="abc8a-141">Configuration Dependencies</span></span>

<span data-ttu-id="abc8a-142">Une propriété peut avoir des dépendances de configuration, sauf lorsqu’elle apparaît dans un élément ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="abc8a-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="abc8a-143">Utilisation des éléments</span><span class="sxs-lookup"><span data-stu-id="abc8a-143">Element Usage</span></span>

<span data-ttu-id="abc8a-144">En plus d’apparaître dans les éléments de fonctionnalité et d’option, les éléments de propriété peuvent apparaître au niveau racine des technologies sous-jacentes respectives.</span><span class="sxs-lookup"><span data-stu-id="abc8a-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="abc8a-145">Le schéma d’impression définit un ensemble d’éléments de propriété qui peuvent être utilisés pour décrire un appareil de manière portable.</span><span class="sxs-lookup"><span data-stu-id="abc8a-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="abc8a-146">Toutefois, si ces propriétés sont insuffisantes pour vos besoins en tant que fournisseur PrintCapabilities (généralement parce que l’appareil pris en charge a de nouveaux aspects non anticipés par le schéma d’impression), vous pouvez introduire vos propres éléments de propriété privés.</span><span class="sxs-lookup"><span data-stu-id="abc8a-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="abc8a-147">Vous pouvez améliorer ou développer les informations fournies par une propriété publique en ajoutant une ou plusieurs sous-propriétés privées en tant que contenu d’élément de la propriété publique.</span><span class="sxs-lookup"><span data-stu-id="abc8a-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="abc8a-148">Les éléments de propriété sont définis à l’aide d’une balise d’élément XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="abc8a-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="abc8a-149">Un nom est attribué à chaque propriété au moyen de son attribut Name.</span><span class="sxs-lookup"><span data-stu-id="abc8a-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="abc8a-150">Le nom doit être un QName XML et doit être conforme à la Convention d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="abc8a-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="abc8a-151">Pour plus d’informations, consultez [attributs XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="abc8a-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="abc8a-152">L’attribut de nom de propriété et son emplacement dans la hiérarchie des éléments de propriété parents (s’il s’agit d’une sous-propriété) identifient de façon unique la propriété dans le document PrintCapabilities ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="abc8a-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="abc8a-153">Une propriété peut contenir un ou plusieurs éléments de valeur, ou un ou plusieurs éléments de propriété enfants (appelés sous-propriétés), ou une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="abc8a-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="abc8a-154">Les sous-propriétés sont utiles lorsque la propriété elle-même est composée de plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="abc8a-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="abc8a-155">Par exemple, une propriété « ConsumableColor » peut avoir des composants « C », « M » et « Y ».</span><span class="sxs-lookup"><span data-stu-id="abc8a-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="abc8a-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="abc8a-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="abc8a-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abc8a-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abc8a-158">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="abc8a-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




