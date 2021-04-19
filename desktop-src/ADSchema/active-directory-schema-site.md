---
title: Terminologie relative au schéma Active Directory
description: Les termes suivants sont couramment utilisés pour faire référence au schéma Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106509481"
---
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="932b1-103">Terminologie relative au schéma Active Directory</span><span class="sxs-lookup"><span data-stu-id="932b1-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="932b1-104">Les termes suivants sont couramment utilisés pour faire référence au schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="932b1-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="932b1-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut</span><span class="sxs-lookup"><span data-stu-id="932b1-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="932b1-106">Éléments de données utilisés pour décrire les objets qui sont représentés par les classes définies dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="932b1-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="932b1-107">Les attributs sont définis dans le schéma séparément des classes ; Cela permet d’appliquer une définition d’attribut unique à de nombreuses classes.</span><span class="sxs-lookup"><span data-stu-id="932b1-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="932b1-108">Par exemple, [**Description**](a-description.md) est un attribut qui peut être appliqué à n’importe quelle classe dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="932b1-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="932b1-109">L’attribut **Description** est défini une fois dans le schéma, garantissant la cohérence, au lieu d’avoir une définition différente pour la **Description** d’un utilisateur et la **Description** d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="932b1-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="932b1-110">Le terme *propriété* est fréquemment utilisé de façon interchangeable avec le terme *attribut*.</span><span class="sxs-lookup"><span data-stu-id="932b1-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="932b1-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instance d’attribut</span><span class="sxs-lookup"><span data-stu-id="932b1-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="932b1-112">Occurrence d’un attribut défini dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="932b1-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="932b1-113">Ce terme est utilisé pour faire la distinction entre la définition d’un attribut et une occurrence discrète de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="932b1-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="932b1-114">Par exemple, le stockage d’un objet utilisateur pour « Jeff Smith » avec l’attribut [**Common-Name**](a-cn.md) défini sur « Jeff Smith » crée une instance de [**nom commun**](a-cn.md).</span><span class="sxs-lookup"><span data-stu-id="932b1-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="932b1-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Type</span><span class="sxs-lookup"><span data-stu-id="932b1-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="932b1-116">Description formelle d’un type d’objet discret et identifiable stocké dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="932b1-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="932b1-117">Par exemple, l' [**utilisateur**](c-user.md), la [**file d’attente d’impression et le**](c-printqueue.md) [**groupe**](c-group.md) sont toutes des classes.</span><span class="sxs-lookup"><span data-stu-id="932b1-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="932b1-118">En outre, il existe trois catégories de classes distinctes : les [classes structurelles](classes-structural.md), les [classes abstraites](classes-abstract.md)et les [classes auxiliaires](classes-auxiliary.md).</span><span class="sxs-lookup"><span data-stu-id="932b1-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="932b1-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instance de classe</span><span class="sxs-lookup"><span data-stu-id="932b1-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="932b1-120">Occurrence d’une classe définie dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="932b1-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="932b1-121">Ce terme est utilisé pour faire la distinction entre la définition d’une classe et une occurrence discrète de la classe.</span><span class="sxs-lookup"><span data-stu-id="932b1-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="932b1-122">Par exemple, le stockage d’un objet [**utilisateur**](c-user.md) pour « Jeff Smith » dans le service d’annuaire crée une instance de l' [**utilisateur**](c-user.md).</span><span class="sxs-lookup"><span data-stu-id="932b1-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="932b1-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Règles de contenu</span><span class="sxs-lookup"><span data-stu-id="932b1-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="932b1-124">Définition du contenu possible des instances de classe stockées dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="932b1-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="932b1-125">Dans les services d’annuaire NT (NTDS), sur lesquels Active Directory est basé, les règles de contenu sont entièrement exprimées par les attributs [**« doit contenir »**](a-mustcontain.md) et [**« peut contenir »**](a-maycontain.md) des définitions de schéma pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="932b1-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Dérivation</span><span class="sxs-lookup"><span data-stu-id="932b1-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="932b1-127">Consultez *héritage*.</span><span class="sxs-lookup"><span data-stu-id="932b1-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Arborescence d’informations de répertoire</span><span class="sxs-lookup"><span data-stu-id="932b1-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="932b1-129">Le répertoire lui-même, représenté sous la forme d’une arborescence dans laquelle les vertex sont les entrées de répertoire (instances de classe) et les lignes de connexion sont les relations parent-enfant entre les entrées.</span><span class="sxs-lookup"><span data-stu-id="932b1-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-130"><span id="DIT"></span><span id="dit"></span>DIT</span><span class="sxs-lookup"><span data-stu-id="932b1-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="932b1-131">Consultez *arborescence des informations de répertoire*.</span><span class="sxs-lookup"><span data-stu-id="932b1-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Contrôler les droits d’accès</span><span class="sxs-lookup"><span data-stu-id="932b1-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="932b1-133">Classe qui décrit un droit d’accès non lié à une ressource, mais une action.</span><span class="sxs-lookup"><span data-stu-id="932b1-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="932b1-134">Par exemple, un utilisateur peut se voir accorder le droit de créer des valeurs d’ID relatives.</span><span class="sxs-lookup"><span data-stu-id="932b1-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span><span class="sxs-lookup"><span data-stu-id="932b1-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="932b1-136">Possibilité de créer de nouvelles classes d’objets à partir de classes d’objets existantes.</span><span class="sxs-lookup"><span data-stu-id="932b1-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="932b1-137">Le nouvel objet est défini en tant que sous- *classe* de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="932b1-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="932b1-138">L’objet parent devient une *superclasse* du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="932b1-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="932b1-139">Une sous-classe hérite des attributs du parent, y compris les règles de structure et les règles de contenu.</span><span class="sxs-lookup"><span data-stu-id="932b1-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span><span class="sxs-lookup"><span data-stu-id="932b1-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="932b1-141">Voir *protocole LDAP (Lightweight Directory Access*).</span><span class="sxs-lookup"><span data-stu-id="932b1-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocole d’accès à Lightweight Directory</span><span class="sxs-lookup"><span data-stu-id="932b1-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="932b1-143">Protocole de communication Internet standard utilisé pour communiquer avec le NTDS.</span><span class="sxs-lookup"><span data-stu-id="932b1-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="932b1-144">LDAP version 2 et version 3 sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="932b1-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="932b1-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="932b1-146">Consultez *descripteur de sécurité*.</span><span class="sxs-lookup"><span data-stu-id="932b1-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Dessin</span><span class="sxs-lookup"><span data-stu-id="932b1-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="932b1-148">Unité de stockage des données dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="932b1-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="932b1-149">Les objets de service d’annuaire ne doivent pas être confondus avec les objets COM ou d’autres objets système orientés objet, qui ont un comportement de composant exécutable et au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="932b1-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="932b1-150">Les objets de service d’annuaire contiennent uniquement des données.</span><span class="sxs-lookup"><span data-stu-id="932b1-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="932b1-151">Un objet de service d’annuaire est défini par un objet de [**schéma de classe**](c-classschema.md) et un groupe d’objets de [**schéma d’attribut**](c-attributeschema.md) référencés par l’objet de schéma de [**classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="932b1-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="932b1-152">Les objets de schéma de [**classe**](c-classschema.md) et d’attribut sont eux [**-**](c-attributeschema.md) mêmes des objets de service d’annuaire et ont des définitions dans le schéma comme tout autre objet.</span><span class="sxs-lookup"><span data-stu-id="932b1-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="932b1-153">Consultez la *classe*.</span><span class="sxs-lookup"><span data-stu-id="932b1-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificateur d’objet</span><span class="sxs-lookup"><span data-stu-id="932b1-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="932b1-155">Valeurs numériques uniques, émises par différentes autorités émettrices, pour identifier de manière unique les éléments de données, les syntaxes et diverses autres parties des applications distribuées.</span><span class="sxs-lookup"><span data-stu-id="932b1-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="932b1-156">Les identificateurs d’objet (OID) sont disponibles dans les applications OSI, les répertoires X. 500, SNMP et d’autres applications pour lesquelles l’unicité est importante.</span><span class="sxs-lookup"><span data-stu-id="932b1-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="932b1-157">Les OID sont basés sur une arborescence, dans laquelle une autorité de délivrance supérieure, telle que l’ISO, alloue une branche de l’arbre à une sous-autorité qui, à son tour, peut allouer des sous-branches.</span><span class="sxs-lookup"><span data-stu-id="932b1-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="932b1-158">Dans le fichier NTDS, les OID incluent certains émis par le fichier ISO pour les classes et les attributs X. 500, et certains émis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="932b1-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="932b1-159">La notation OID est une chaîne de nombres en pointillés, par exemple « 1.2.840.113556.1.5.4 », qui se traduit comme indiqué dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="932b1-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="932b1-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="932b1-160">Value</span></span>  | <span data-ttu-id="932b1-161">Description</span><span class="sxs-lookup"><span data-stu-id="932b1-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="932b1-162">1</span><span class="sxs-lookup"><span data-stu-id="932b1-162">1</span></span>      | <span data-ttu-id="932b1-163">ISO : « autorité racine », a émis « 1,2 » à ANSI, qui à son tour...</span><span class="sxs-lookup"><span data-stu-id="932b1-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="932b1-164">2</span><span class="sxs-lookup"><span data-stu-id="932b1-164">2</span></span>      | <span data-ttu-id="932b1-165">ANSI... a émis « 1.2.840 » aux États-Unis, qui à son tour...</span><span class="sxs-lookup"><span data-stu-id="932b1-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="932b1-166">840</span><span class="sxs-lookup"><span data-stu-id="932b1-166">840</span></span>    | <span data-ttu-id="932b1-167">ÉTATS-UNIS... a émis « 1.2.840.113556 » à Microsoft...</span><span class="sxs-lookup"><span data-stu-id="932b1-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="932b1-168">113556</span><span class="sxs-lookup"><span data-stu-id="932b1-168">113556</span></span> | <span data-ttu-id="932b1-169">Microsoft... où Microsoft gère en interne plusieurs branches OID sous « 1.2.840.113556 ».</span><span class="sxs-lookup"><span data-stu-id="932b1-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="932b1-170">1</span><span class="sxs-lookup"><span data-stu-id="932b1-170">1</span></span>      | <span data-ttu-id="932b1-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="932b1-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="932b1-172">5</span><span class="sxs-lookup"><span data-stu-id="932b1-172">5</span></span>      | <span data-ttu-id="932b1-173">Classes NTDS</span><span class="sxs-lookup"><span data-stu-id="932b1-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="932b1-174">4</span><span class="sxs-lookup"><span data-stu-id="932b1-174">4</span></span>      | <span data-ttu-id="932b1-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="932b1-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="932b1-176"><span id="OID"></span><span id="oid"></span>OID</span><span class="sxs-lookup"><span data-stu-id="932b1-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="932b1-177">Consultez *identificateur d’objet*.</span><span class="sxs-lookup"><span data-stu-id="932b1-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schéma</span><span class="sxs-lookup"><span data-stu-id="932b1-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="932b1-179">Définition formelle du contenu et de la structure du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="932b1-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="932b1-180">Le schéma définit tous les attributs et les classes.</span><span class="sxs-lookup"><span data-stu-id="932b1-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="932b1-181">Pour chaque classe, les attributs [**Poss-Superior**](a-posssuperiors.md), [**doit contenir**](a-mustcontain.md)et [**peut contenir**](a-maycontain.md) sont définis.</span><span class="sxs-lookup"><span data-stu-id="932b1-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="932b1-182">[**Poss-Superior**](a-posssuperiors.md) définit les structures d’arborescence possibles pour le service d’annuaire en spécifiant les classes qui peuvent être le parent d’une classe donnée.</span><span class="sxs-lookup"><span data-stu-id="932b1-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="932b1-183">[**Contains**](a-mustcontain.md) et [**Contains Contains**](a-maycontain.md) répertorient les attributs d’une classe qui doivent être présents pour stocker la classe et les attributs supplémentaires éventuellement présents.</span><span class="sxs-lookup"><span data-stu-id="932b1-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="932b1-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="932b1-185">Informations sur la propriété d’un objet et les autorisations dont disposent les autres utilisateurs sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="932b1-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="932b1-186">La propriété [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) d’une entrée de schéma contient une chaîne qui représente le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="932b1-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="932b1-187">Pour plus d’informations sur le format des informations contenues dans ce champ, consultez [format de chaîne du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="932b1-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="932b1-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Règles de structure</span><span class="sxs-lookup"><span data-stu-id="932b1-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="932b1-189">Définition de la ou des structures d’arborescence possibles.</span><span class="sxs-lookup"><span data-stu-id="932b1-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="932b1-190">Dans le NTDS, les règles de structure sont entièrement exprimées par l’attribut Poss-Superior présent sur chaque objet de [**schéma de classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="932b1-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="932b1-191">Consultez *schéma*.</span><span class="sxs-lookup"><span data-stu-id="932b1-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Sous-classe</span><span class="sxs-lookup"><span data-stu-id="932b1-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="932b1-193">Objet de [**schéma de classe**](c-classschema.md) qui hérite d’un autre objet de schéma de [**classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="932b1-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="932b1-194">Consultez *héritage*.</span><span class="sxs-lookup"><span data-stu-id="932b1-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclasse</span><span class="sxs-lookup"><span data-stu-id="932b1-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="932b1-196">Objet de [**schéma de classe**](c-classschema.md) à partir duquel un ou plusieurs autres objets de schéma de [**classe**](c-classschema.md) héritent.</span><span class="sxs-lookup"><span data-stu-id="932b1-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="932b1-197">Consultez *héritage*.</span><span class="sxs-lookup"><span data-stu-id="932b1-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Arbres</span><span class="sxs-lookup"><span data-stu-id="932b1-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="932b1-199">Consultez *arborescence des informations de répertoire*.</span><span class="sxs-lookup"><span data-stu-id="932b1-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="932b1-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="932b1-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="932b1-201">Famille de normes développées conjointement par l’ISO et l’ITU, anciennement appelée CCITT, qui spécifient l’affectation de noms, la représentation des données et les protocoles de communication pour un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="932b1-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 