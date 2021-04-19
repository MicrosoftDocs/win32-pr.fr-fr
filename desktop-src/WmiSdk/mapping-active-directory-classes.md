---
description: Fournit des règles pour le mappage des classes WMI à Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapper des classes Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536736"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="a1f07-103">Mapper des classes Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1f07-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="a1f07-104">Étant donné que Active Directory possède un large éventail d’objets possibles, WMI ne peut pas créer un mappage direct un-à-un.</span><span class="sxs-lookup"><span data-stu-id="a1f07-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="a1f07-105">Au lieu de cela, le fournisseur de services d’annuaire utilise des règles pour mapper les classes entre les deux technologies.</span><span class="sxs-lookup"><span data-stu-id="a1f07-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="a1f07-106">Les sections suivantes sont abordées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="a1f07-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="a1f07-107">Mapper des classes</span><span class="sxs-lookup"><span data-stu-id="a1f07-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="a1f07-108">Mappage d’attributs</span><span class="sxs-lookup"><span data-stu-id="a1f07-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="a1f07-109">Classes d’association</span><span class="sxs-lookup"><span data-stu-id="a1f07-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="a1f07-110">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="a1f07-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="a1f07-111">Mapper des classes</span><span class="sxs-lookup"><span data-stu-id="a1f07-111">Mapping Classes</span></span>

<span data-ttu-id="a1f07-112">La liste suivante décrit les instructions utilisées par le fournisseur de services d’annuaire pour mapper des classes Active Directory à des classes WMI :</span><span class="sxs-lookup"><span data-stu-id="a1f07-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="a1f07-113">Chaque classe abstraite du schéma Active Directory est mappée à une classe abstraite dans le schéma WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="a1f07-114">Dans le schéma WMI, chaque classe abstraite est précédée de DS \_ .</span><span class="sxs-lookup"><span data-stu-id="a1f07-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="a1f07-115">Par exemple, la classe **Person** du schéma Active Directory est mappée à la classe WMI Person de la **\_ personne** .</span><span class="sxs-lookup"><span data-stu-id="a1f07-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="a1f07-116">Chaque classe non abstraite du schéma Active Directory est mappée aux deux classes suivantes dans le schéma WMI :</span><span class="sxs-lookup"><span data-stu-id="a1f07-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="a1f07-117">La première classe mappée est précédée de publicités \_ .</span><span class="sxs-lookup"><span data-stu-id="a1f07-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="a1f07-118">Il s’agit de classes abstraites, mappées selon les règles ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="a1f07-119">La deuxième classe mappée est une classe non abstraite avec le préfixe de nom de service d’annuaire \_ .</span><span class="sxs-lookup"><span data-stu-id="a1f07-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="a1f07-120">Cette classe est dérivée de la \_ classe abstraite ADS, avec l’ajout du qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="a1f07-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="a1f07-121">Par exemple, la classe **utilisateur** du schéma Active Directory est mappée à deux classes.</span><span class="sxs-lookup"><span data-stu-id="a1f07-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="a1f07-122">La première classe est la classe abstraite **\_ utilisateur ADS** , mappée selon les règles ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="a1f07-123">La deuxième classe est la classe non abstraite de l' **\_ utilisateur DS** .</span><span class="sxs-lookup"><span data-stu-id="a1f07-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="a1f07-124">Elle est dérivée de l' **\_ utilisateur ADS** et a le qualificateur de [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) ajouté.</span><span class="sxs-lookup"><span data-stu-id="a1f07-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="a1f07-125">Sauf spécification contraire, le nom d’une classe mappée est la valeur tronquée de la propriété **LDAP-Display-Name** dans la classe Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1f07-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="a1f07-126">Si la propriété **sous-classe-de** est présente dans la classe Active Directory, la classe mappée WMI est dérivée de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a1f07-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="a1f07-127">Si la propriété **de sous-classe** n’est pas présente, la classe mappée WMI est dérivée de la classe de la **\_ \_ \_ classe racine LDAP DS** , comme indiqué dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="a1f07-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="a1f07-128">Cette classe possède la propriété de clé **ADSIPath** , avec un type **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="a1f07-129">Il s’agit du chemin d’accès ADSI unique qui identifie cette instance.</span><span class="sxs-lookup"><span data-stu-id="a1f07-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="a1f07-130">Active Directory prend en charge uniquement l’héritage unique, ce qui fonctionne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="a1f07-131">Un qualificateur **dynamique** de type **VT \_ bool** et Flavor ayant la valeur `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` **true** est créé pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="a1f07-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="a1f07-132">Il s’agit d’un qualificateur WMI standard qui indique que les instances de cette classe sont fournies dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="a1f07-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="a1f07-133">Si la classe n’est pas abstraite, le fournisseur crée un qualificateur de [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) de type **VT \_ BSTR bool** et qualificateur Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` défini sur « fournisseur d’instance DS » pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="a1f07-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="a1f07-134">Il s’agit d’un qualificateur WMI standard qui indique le nom du fournisseur qui fournit dynamiquement des instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="a1f07-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="a1f07-135">Le reste des propriétés ADSI est mappé aux qualificateurs et aux propriétés de classe, conformément aux tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="a1f07-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="a1f07-136">Tous les qualificateurs sont mappés avec une valeur d’indicateur de qualificateur de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .</span><span class="sxs-lookup"><span data-stu-id="a1f07-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="a1f07-137">La liste suivante répertorie les informations de mappage pour la classe Active Directory, en présentant le qualificateur WMI et le type de qualificateur WMI pour chaque propriété Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1f07-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="a1f07-138">**Nom commun**</span><span class="sxs-lookup"><span data-stu-id="a1f07-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-139">**CN** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="a1f07-140">Mappé directement à partir de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-141">**Default-Object-catégorie**</span><span class="sxs-lookup"><span data-stu-id="a1f07-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-142">**DefaultObjectCategory** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="a1f07-143">Mappé directement à partir de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-144">**Descripteur de sécurité par défaut**</span><span class="sxs-lookup"><span data-stu-id="a1f07-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-145">**DefaultSecurityDescriptor** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="a1f07-146">Mappé directement à partir de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-147">**Régit l’ID**</span><span class="sxs-lookup"><span data-stu-id="a1f07-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-148">**GovernsId** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="a1f07-149">Mappé à partir de la représentation sous forme de chaîne de l’OID ; par exemple, « {1 3 3 6} ».</span><span class="sxs-lookup"><span data-stu-id="a1f07-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-150">**Classe d’objet**</span><span class="sxs-lookup"><span data-stu-id="a1f07-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-151">N/A</span><span class="sxs-lookup"><span data-stu-id="a1f07-151">N/A</span></span>

<span data-ttu-id="a1f07-152">Non mappé.</span><span class="sxs-lookup"><span data-stu-id="a1f07-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-153">**Catégorie objet-classe**</span><span class="sxs-lookup"><span data-stu-id="a1f07-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-154">**ObjectClassCategory** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="a1f07-155">Mappé directement à partir de la valeur entière.</span><span class="sxs-lookup"><span data-stu-id="a1f07-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="a1f07-156">En outre, si la valeur est abstract (2), le qualificateur standard **VT \_ bool** CIM, appelé qualificateur **« abstract »** , est également créé.</span><span class="sxs-lookup"><span data-stu-id="a1f07-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-157">**RDN-ATT-ID**</span><span class="sxs-lookup"><span data-stu-id="a1f07-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-158">**RDNATTID** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="a1f07-159">Mappé à partir de la représentation sous forme de chaîne de la valeur OID ; par exemple, « {1 3 3 6} ».</span><span class="sxs-lookup"><span data-stu-id="a1f07-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="a1f07-160">En outre, la propriété identifiée ici est annotée avec le qualificateur CIM **indexé** standard défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-161">**Système uniquement**</span><span class="sxs-lookup"><span data-stu-id="a1f07-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-162">**SystemOnly** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="a1f07-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="a1f07-163">Mappé directement à partir de la valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="a1f07-164">La liste suivante répertorie les propriétés de la classe Active Directory mappées aux propriétés de la classe WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1f07-165">**Peut contenir**</span><span class="sxs-lookup"><span data-stu-id="a1f07-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-166">Chaque propriété de cette liste est mappée à une propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-167">**Doit contenir**</span><span class="sxs-lookup"><span data-stu-id="a1f07-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-168">Chaque propriété de cette liste est mappée à une propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="a1f07-169">Le qualificateur CIM standard **not \_ null** est créé pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="a1f07-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-170">**Système-peut contenir**</span><span class="sxs-lookup"><span data-stu-id="a1f07-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-171">Chaque propriété de cette liste est mappée à une propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="a1f07-172">En outre, chaque propriété est annotée avec un qualificateur **système** , défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-173">**Système-doit contenir**</span><span class="sxs-lookup"><span data-stu-id="a1f07-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="a1f07-174">Chaque propriété de cette liste est mappée à une propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="a1f07-175">Le qualificateur CIM standard **not \_ null** est créé pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="a1f07-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="a1f07-176">En outre, chaque propriété est annotée avec un qualificateur **système** , défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="a1f07-177">Mappage d’attributs</span><span class="sxs-lookup"><span data-stu-id="a1f07-177">Mapping Attributes</span></span>

<span data-ttu-id="a1f07-178">Le fournisseur de services d’annuaire mappe chaque attribut d’une classe Active Directory à une seule propriété de la classe WMI correspondante, conformément aux règles de cette section.</span><span class="sxs-lookup"><span data-stu-id="a1f07-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="a1f07-179">En général, le fournisseur de services d’annuaire nomme la propriété WMI en tant que version tronquée de la valeur **LDAP-Display-Name** de l’attribut Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a1f07-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="a1f07-180">Si la propriété Active Directory **est définie sur une** **valeur** unique, la propriété WMI est combinée avec l’opérateur ou avec un **tableau d' \_ indicateurs \_ CIM**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="a1f07-181">Notez que chaque propriété est marquée avec le qualificateur **VT \_ BSTR** , **ADSyntax**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="a1f07-182">Il représente la syntaxe de Active Directory sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="a1f07-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="a1f07-183">Le tableau suivant répertorie le mappage de la syntaxe de Active Directory au type de données de la propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="a1f07-184">Élément Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1f07-184">Active Directory element</span></span>                                      | <span data-ttu-id="a1f07-185">Type de données WMI</span><span class="sxs-lookup"><span data-stu-id="a1f07-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="a1f07-186">**Point d’accès**</span><span class="sxs-lookup"><span data-stu-id="a1f07-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="a1f07-187">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="a1f07-188">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1f07-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="a1f07-189">**\_valeur BOOLÉENNE CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="a1f07-190">**Chaîne non sensible à la casse**</span><span class="sxs-lookup"><span data-stu-id="a1f07-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="a1f07-191">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="a1f07-192">**Chaîne respectant la casse**</span><span class="sxs-lookup"><span data-stu-id="a1f07-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="a1f07-193">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="a1f07-194">**Nom unique**</span><span class="sxs-lookup"><span data-stu-id="a1f07-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="a1f07-195">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="a1f07-196">**DN-binaire**</span><span class="sxs-lookup"><span data-stu-id="a1f07-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="a1f07-197">Objet incorporé de la classe **DN \_ avec le \_ binaire** défini ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="a1f07-198">**DN-chaîne**</span><span class="sxs-lookup"><span data-stu-id="a1f07-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="a1f07-199">Objet incorporé de la classe **DN \_ avec la \_ chaîne** définie ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="a1f07-200">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a1f07-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="a1f07-201">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="a1f07-202">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a1f07-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="a1f07-203">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="a1f07-204">**Entière**</span><span class="sxs-lookup"><span data-stu-id="a1f07-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="a1f07-205">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="a1f07-206">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="a1f07-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="a1f07-207">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="a1f07-208">Descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="a1f07-208">Security Descriptor</span></span>                                           | <span data-ttu-id="a1f07-209">Objet incorporé de la classe **Uint8Array** défini ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="a1f07-210">Chaîne numérique</span><span class="sxs-lookup"><span data-stu-id="a1f07-210">Numeric String</span></span>                                                | <span data-ttu-id="a1f07-211">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="a1f07-212">ID objet</span><span class="sxs-lookup"><span data-stu-id="a1f07-212">Object ID</span></span>                                                     | <span data-ttu-id="a1f07-213">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="a1f07-214">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="a1f07-214">Octet String</span></span>                                                  | <span data-ttu-id="a1f07-215">Objet incorporé de la classe **Uint8Array** défini ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="a1f07-216">OU le nom</span><span class="sxs-lookup"><span data-stu-id="a1f07-216">OR Name</span></span>                                                       | <span data-ttu-id="a1f07-217">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="a1f07-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="a1f07-218">Presentation-Address</span></span>                                          | <span data-ttu-id="a1f07-219">Objet incorporé de la classe **Uint8Array** défini ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="a1f07-220">Imprimer la chaîne de cas</span><span class="sxs-lookup"><span data-stu-id="a1f07-220">Print Case String</span></span>                                             | <span data-ttu-id="a1f07-221">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="a1f07-222">Lien de réplica</span><span class="sxs-lookup"><span data-stu-id="a1f07-222">Replica Link</span></span>                                                  | <span data-ttu-id="a1f07-223">Objet incorporé de la classe **Uint8Array** défini ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="a1f07-224">**Chaîne (SID)**</span><span class="sxs-lookup"><span data-stu-id="a1f07-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="a1f07-225">Objet incorporé de la classe **Uint8Array** défini ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a1f07-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="a1f07-226">Temps</span><span class="sxs-lookup"><span data-stu-id="a1f07-226">Time</span></span>                                                          | <span data-ttu-id="a1f07-227">**\_DateTime CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="a1f07-228">Heure du code UTC</span><span class="sxs-lookup"><span data-stu-id="a1f07-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="a1f07-229">**\_DateTime CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="a1f07-230">Chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="a1f07-230">Unicode String</span></span>                                                | <span data-ttu-id="a1f07-231">**\_chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="a1f07-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="a1f07-232">La syntaxe de la chaîne d’octets, qui fait référence à un tableau de valeurs **UInt8** , pose un problème lorsqu’elle est mappée à WMI, car WMI autorise des propriétés de types **UInt8** et des tableaux de **uint8**, tandis que Active Directory autorise des propriétés de type chaîne d’octets, ainsi que des tableaux de chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="a1f07-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="a1f07-233">L’exemple suivant illustre la classe de fournisseur de services d’annuaire utilisée pour mapper un tableau de propriétés de type chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="a1f07-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="a1f07-234">WMI mappe toutes les chaînes d’octets Active Directory les valeurs de propriété aux instances incorporées de **Uint8Array**.</span><span class="sxs-lookup"><span data-stu-id="a1f07-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="a1f07-235">De même, WMI mappe des tableaux de chaînes d’octets à des tableaux d’objets **Uint8Array** incorporés.</span><span class="sxs-lookup"><span data-stu-id="a1f07-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="a1f07-236">L’exemple suivant montre les classes qui sont mappées par WMI à DN-Binary et DN-String valeurs de propriété de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a1f07-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="a1f07-237">Le tableau suivant répertorie comment WMI mappe le reste des propriétés d’interface d’attribut Active Directory aux qualificateurs de propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a1f07-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="a1f07-238">Attribut Active Directory-nom de propriété</span><span class="sxs-lookup"><span data-stu-id="a1f07-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="a1f07-239">Qualificateur WMI</span><span class="sxs-lookup"><span data-stu-id="a1f07-239">WMI Qualifier</span></span>       | <span data-ttu-id="a1f07-240">Type de données</span><span class="sxs-lookup"><span data-stu-id="a1f07-240">Data type</span></span>    | <span data-ttu-id="a1f07-241">Informations de mappage</span><span class="sxs-lookup"><span data-stu-id="a1f07-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="a1f07-242">**Syntaxe d’attribut**</span><span class="sxs-lookup"><span data-stu-id="a1f07-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="a1f07-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="a1f07-243">**AttributeSyntax**</span></span> | <span data-ttu-id="a1f07-244">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a1f07-244">**VT\_BSTR**</span></span> | <span data-ttu-id="a1f07-245">Mappé à partir de la représentation sous forme de chaîne de l’OID.</span><span class="sxs-lookup"><span data-stu-id="a1f07-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="a1f07-246">**Nom commun**</span><span class="sxs-lookup"><span data-stu-id="a1f07-246">**Common-Name**</span></span>                          | <span data-ttu-id="a1f07-247">**8525**</span><span class="sxs-lookup"><span data-stu-id="a1f07-247">**CN**</span></span>              | <span data-ttu-id="a1f07-248">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="a1f07-248">**VT\_BSTR**</span></span> | <span data-ttu-id="a1f07-249">Mappé à partir de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="a1f07-250">**Système uniquement**</span><span class="sxs-lookup"><span data-stu-id="a1f07-250">**System-Only**</span></span>                          | <span data-ttu-id="a1f07-251">**Système**</span><span class="sxs-lookup"><span data-stu-id="a1f07-251">**System**</span></span>          | <span data-ttu-id="a1f07-252">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a1f07-252">**VT\_BOOL**</span></span> | <span data-ttu-id="a1f07-253">Mappé à partir de la valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="a1f07-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="a1f07-254">WMI mappe tous les qualificateurs de Active Directory avec les `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` versions de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="a1f07-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="a1f07-255">Classes d’association</span><span class="sxs-lookup"><span data-stu-id="a1f07-255">Association Classes</span></span>

<span data-ttu-id="a1f07-256">Le service d’annuaire est essentiellement un magasin hiérarchique d’objets.</span><span class="sxs-lookup"><span data-stu-id="a1f07-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="a1f07-257">Les objets qui peuvent apparaître à un niveau non-feuille dans la hiérarchie sont appelés « conteneurs ».</span><span class="sxs-lookup"><span data-stu-id="a1f07-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="a1f07-258">La structure de cette hiérarchie est contrôlée par les propriétés « Poss-Superior » et « System-Poss-Superiors » d’une classe dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="a1f07-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="a1f07-259">Ceux-ci, pris ensemble, spécifient le jeu de classes dont les instances peuvent être contenues dans une instance d’une classe de conteneur.</span><span class="sxs-lookup"><span data-stu-id="a1f07-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="a1f07-260">L’exemple suivant modélise une association CIM en tant qu’instances de la classe d’association statique [**\_ \_ \_ relation contenant-contenu de la classe LDAP DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span><span class="sxs-lookup"><span data-stu-id="a1f07-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="a1f07-261">Le fournisseur de classes d’association prend en charge les méthodes [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) et [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .</span><span class="sxs-lookup"><span data-stu-id="a1f07-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 

