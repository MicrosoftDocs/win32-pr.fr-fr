---
description: En savoir plus sur les attributs XML dans l’infrastructure du schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Attributs XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548817"
---
# <a name="xml-attributes"></a><span data-ttu-id="01dc2-105">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="01dc2-105">XML Attributes</span></span>

<span data-ttu-id="01dc2-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="01dc2-106">This topic is not current.</span></span> <span data-ttu-id="01dc2-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="01dc2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01dc2-108">Il existe un certain nombre d’attributs XML qui apparaissent dans plusieurs types d’éléments définis dans l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="01dc2-108">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="01dc2-109">Les attributs XML portant le même nom ont généralement la même signification et obéissent aux mêmes règles quel que soit le type d’élément dans lequel elles résident.</span><span class="sxs-lookup"><span data-stu-id="01dc2-109">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="01dc2-110">Par conséquent, les attributs XML sont répertoriés ici par nom et non par leur type d’élément hôte.</span><span class="sxs-lookup"><span data-stu-id="01dc2-110">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="01dc2-111">Les attributs XML définis de manière privée ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="01dc2-111">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="01dc2-112">Seuls les attributs XML définis ici peuvent être utilisés dans un document PrintCapabilities ou un PrintTicket, puis uniquement dans le contexte défini.</span><span class="sxs-lookup"><span data-stu-id="01dc2-112">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="01dc2-113">Bien que les parties privées ne soient pas autorisées à introduire de nouvelles définitions dans l’espace de noms d’un autre tiers, elles sont autorisées à utiliser des noms existants à partir d’un autre espace de noms privé, à condition que leur utilisation soit cohérente avec l’utilisation établie par l’autre partie.</span><span class="sxs-lookup"><span data-stu-id="01dc2-113">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="01dc2-114">Par conséquent, une option peut contenir des éléments ScoredProperty définis par plusieurs tiers, chacun résidant dans des espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="01dc2-114">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01dc2-115">Nom d’attribut</span><span class="sxs-lookup"><span data-stu-id="01dc2-115">Attribute Name</span></span></th>
<th><span data-ttu-id="01dc2-116">Types de données et valeurs</span><span class="sxs-lookup"><span data-stu-id="01dc2-116">Data Types and Values</span></span></th>
<th><span data-ttu-id="01dc2-117">Objectif</span><span class="sxs-lookup"><span data-stu-id="01dc2-117">Purpose</span></span></th>
<th><span data-ttu-id="01dc2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="01dc2-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01dc2-119">name</span><span class="sxs-lookup"><span data-stu-id="01dc2-119">name</span></span> <br/></td>
<td><span data-ttu-id="01dc2-120">QName XML</span><span class="sxs-lookup"><span data-stu-id="01dc2-120">XML QName</span></span><br/></td>
<td><span data-ttu-id="01dc2-121">Cet attribut XML identifie l’instance de l’élément.</span><span class="sxs-lookup"><span data-stu-id="01dc2-121">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="01dc2-122">Elle distingue un élément d’un autre type d’élément.</span><span class="sxs-lookup"><span data-stu-id="01dc2-122">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="01dc2-123">Cet attribut XML est si largement utilisé. il est appelé attribut de nom.</span><span class="sxs-lookup"><span data-stu-id="01dc2-123">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="01dc2-124">Les restrictions suivantes s’appliquent à l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="01dc2-124">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="01dc2-125">L’attribut name doit se présenter sous la forme d’un QName défini par XML valide.</span><span class="sxs-lookup"><span data-stu-id="01dc2-125">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="01dc2-126">Autrement dit, il doit être qualifié par un espace de noms XML valide.</span><span class="sxs-lookup"><span data-stu-id="01dc2-126">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="01dc2-127">Les QNames qui apparaissent en tant que valeurs des attributs de nom doivent être explicitement qualifiés par un espace de noms, même si un espace de noms par défaut est défini.</span><span class="sxs-lookup"><span data-stu-id="01dc2-127">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="01dc2-128">Le contenu des caractères doit être celui d’un QName défini en XML valide.</span><span class="sxs-lookup"><span data-stu-id="01dc2-128">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="01dc2-129">Les noms définis en privé doivent être qualifiés avec un espace de noms qui est associé de manière unique au tiers qui a introduit l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="01dc2-129">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="01dc2-130">Exigence d’unicité frères : deux éléments frères appartenant au même type d’élément peuvent avoir le même attribut Name.</span><span class="sxs-lookup"><span data-stu-id="01dc2-130">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="01dc2-131">La seule exception concerne les éléments option, où l’attribut Name peut être utilisé pour définir une option.</span><span class="sxs-lookup"><span data-stu-id="01dc2-131">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="01dc2-132">Par conséquent, les éléments d’option à plusieurs frères peuvent avoir le même attribut Name.</span><span class="sxs-lookup"><span data-stu-id="01dc2-132">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="01dc2-133">Les types d’éléments suivants peuvent contenir des attributs de nom : Property, ScoredProperty, ParameterDef, option et Feature.</span><span class="sxs-lookup"><span data-stu-id="01dc2-133">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="01dc2-134">les attributs de nom doivent apparaître dans chacun des types d’éléments qui les contiennent, sauf dans le cas de certains éléments d’option de schéma d’impression publics précédemment définis, tels que DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="01dc2-134">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="01dc2-135">L’exemple suivant montre comment identifier une instance d’option à l’aide d’un attribut’name'.</span><span class="sxs-lookup"><span data-stu-id="01dc2-135">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="01dc2-136">Il s’agit de la méthode correcte pour définir des éléments d’option.</span><span class="sxs-lookup"><span data-stu-id="01dc2-136">This is the correct way to define Option elements.</span></span> <span data-ttu-id="01dc2-137">Un fournisseur ne doit pas avoir d’options sans nom, sauf s’il est défini publiquement dans le schéma d’impression, par exemple DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="01dc2-137">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01dc2-138">propager</span><span class="sxs-lookup"><span data-stu-id="01dc2-138">propagate</span></span> <br/></td>
<td><span data-ttu-id="01dc2-139">Énumération</span><span class="sxs-lookup"><span data-stu-id="01dc2-139">Enumeration</span></span><br/> <span data-ttu-id="01dc2-140">Aucune valeur n’est actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="01dc2-140">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="01dc2-141">L’attribut Propagate n’est pas utilisé dans la version initiale de l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="01dc2-141">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="01dc2-142">Il est documenté ici afin que le code de validation PrintCapabilities ou PrintTicket implémenté pour la version initiale de l’infrastructure du schéma d’impression puisse traiter toutes les versions de schéma suivantes sans erreur.</span><span class="sxs-lookup"><span data-stu-id="01dc2-142">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="01dc2-143">la</span><span class="sxs-lookup"><span data-stu-id="01dc2-143">constrained</span></span> <br/></td>
<td><span data-ttu-id="01dc2-144">Énumération</span><span class="sxs-lookup"><span data-stu-id="01dc2-144">Enumeration</span></span><br/> <span data-ttu-id="01dc2-145">Valeurs autorisées :</span><span class="sxs-lookup"><span data-stu-id="01dc2-145">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="01dc2-146">None</span><span class="sxs-lookup"><span data-stu-id="01dc2-146">None</span></span> <br/></li>
<li><span data-ttu-id="01dc2-147">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="01dc2-147">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="01dc2-148">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="01dc2-148">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="01dc2-149">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="01dc2-149">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="01dc2-150">Indique si l’option est disponible pour la sélection ou pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="01dc2-150">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="01dc2-151">Les valeurs autorisées de l’attribut contraction ont les significations suivantes.</span><span class="sxs-lookup"><span data-stu-id="01dc2-151">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="01dc2-152">Notez que ces valeurs sont répertoriées dans l’ordre, de la moins restrictive (aucune) à la plus restrictive (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="01dc2-152">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="01dc2-153">None</span><span class="sxs-lookup"><span data-stu-id="01dc2-153">None</span></span> <br/>
<ul>
<li><span data-ttu-id="01dc2-154">L’option n’est pas restreinte.</span><span class="sxs-lookup"><span data-stu-id="01dc2-154">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="01dc2-155">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="01dc2-155">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="01dc2-156">L’option est restreinte par les paramètres PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="01dc2-156">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="01dc2-157">Cela implique que la modification de la configuration peut supprimer la contrainte.</span><span class="sxs-lookup"><span data-stu-id="01dc2-157">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="01dc2-158">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="01dc2-158">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="01dc2-159">L’option est restreinte par les paramètres de l’administrateur ; l’option ne peut pas être activée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="01dc2-159">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="01dc2-160">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="01dc2-160">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="01dc2-161">L’option est restreinte par les paramètres de l’appareil ou les options de l’appareil physiquement installées ; l’option ne peut pas être activée par l’utilisateur ou par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="01dc2-161">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="01dc2-162">Lorsque le fournisseur PrintCapabilities signale les valeurs de l’attribut Constrained, la contrainte la plus restrictive trouvée doit être signalée.</span><span class="sxs-lookup"><span data-stu-id="01dc2-162">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="01dc2-163">Par exemple, si une option est restreinte à la fois par un paramètre d’administrateur et un paramètre d’appareil, le fournisseur PrintCapabilities doit signaler DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="01dc2-163">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01dc2-164">xmlns</span><span class="sxs-lookup"><span data-stu-id="01dc2-164">xmlns</span></span> <br/></td>
<td><span data-ttu-id="01dc2-165">URI</span><span class="sxs-lookup"><span data-stu-id="01dc2-165">URI</span></span><br/></td>
<td><span data-ttu-id="01dc2-166">Cet attribut XML établit un lien entre un URI (Uniform Resource Identifier) d’espace de noms et le préfixe d’espace de noms qui apparaît dans le QName XML.</span><span class="sxs-lookup"><span data-stu-id="01dc2-166">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="01dc2-167">Vous devez établir un lien de ce type vers l’URI d’espace de noms défini pour l’infrastructure du schéma d’impression avant de pouvoir utiliser l’une des balises d’élément, attributs, attributs de nom définis par le Framework, etc.</span><span class="sxs-lookup"><span data-stu-id="01dc2-167">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="01dc2-168">Vous pouvez déclarer cet espace de noms comme étant la valeur par défaut pour éviter de qualifier réellement les balises d’élément avec un préfixe d’espace de noms, bien que tous les autres QNames doivent être qualifiés de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="01dc2-168">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="01dc2-169">L’espace de noms standard doit être défini dans l’élément racine approprié.</span><span class="sxs-lookup"><span data-stu-id="01dc2-169">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="01dc2-170">Observez toutes les règles et conventions XML relatives à l’utilisation de l’attribut xmlns.</span><span class="sxs-lookup"><span data-stu-id="01dc2-170">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="01dc2-171">L’URI de l’infrastructure du schéma d’impression est http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="01dc2-171">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="01dc2-172">L’URI pour les mots clés du schéma d’impression est https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="01dc2-172">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="01dc2-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01dc2-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01dc2-174">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="01dc2-174">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




