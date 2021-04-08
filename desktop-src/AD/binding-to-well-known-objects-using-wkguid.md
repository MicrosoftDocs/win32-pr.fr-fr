---
title: Liaison à des objets Well-Known à l’aide de WKGUID
description: Cette rubrique montre comment effectuer une liaison à des objets à l’aide de la chaîne de liaison WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Liaison à des objets Well-Known à l’aide de WKGUID AD
- Active Directory, utilisation de, liaison, utilisation de WKGUID pour établir une liaison avec des objets connus
- objets connus AD
- objets connus AD, liaison à à l’aide de WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724645"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="43920-107">Liaison à des objets Well-Known à l’aide de WKGUID</span><span class="sxs-lookup"><span data-stu-id="43920-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="43920-108">Les conteneurs peuvent avoir un ou plusieurs sous-objets importants qui peuvent être renommés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="43920-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="43920-109">Il peut être difficile de suivre ces sous-objets et de générer des chaînes de liaison correctes pour eux, en particulier s’ils sont renommés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="43920-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="43920-110">Pour prendre en charge la liaison renommée-Safe à ces objets au sein de ces conteneurs, Active Directory Domain Services avoir deux attributs : **wellKnownObjects** et **otherWellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="43920-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="43920-111">Ces attributs ont une syntaxe d’attribut de ADSTYPE \_ DN \_ avec \_ binaire.</span><span class="sxs-lookup"><span data-stu-id="43920-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="43920-112">Ils autorisent plusieurs valeurs et contiennent les tuples GUID/DN des objets connus dans les conteneurs sur lesquels ils sont définis.</span><span class="sxs-lookup"><span data-stu-id="43920-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="43920-113">Le serveur Active Directory conserve la partie nom unique de chaque entrée **wellKnownObjects** et **otherWellKnownObjects** afin qu’il contienne le nom unique actuel de l’objet spécifié lors de la création de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="43920-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="43920-114">La propriété **otherWellKnownObjects** peut être définie et utilisée sur n’importe quel objet.</span><span class="sxs-lookup"><span data-stu-id="43920-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="43920-115">La propriété **wellKnownObjects** est utilisée sur les conteneurs de domainDNS et de configuration.</span><span class="sxs-lookup"><span data-stu-id="43920-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="43920-116">La propriété **wellKnownObjects** est une propriété système uniquement et ne peut être modifiée que par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="43920-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="43920-117">Le conteneur **domainDNS** contient les objets connus suivants :</span><span class="sxs-lookup"><span data-stu-id="43920-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="43920-118">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="43920-118">Users</span></span>
-   <span data-ttu-id="43920-119">Ordinateurs</span><span class="sxs-lookup"><span data-stu-id="43920-119">Computers</span></span>
-   <span data-ttu-id="43920-120">Système</span><span class="sxs-lookup"><span data-stu-id="43920-120">System</span></span>
-   <span data-ttu-id="43920-121">Contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="43920-121">Domain Controllers</span></span>
-   <span data-ttu-id="43920-122">Infrastructure</span><span class="sxs-lookup"><span data-stu-id="43920-122">Infrastructure</span></span>
-   <span data-ttu-id="43920-123">Objets supprimés</span><span class="sxs-lookup"><span data-stu-id="43920-123">Deleted Objects</span></span>
-   <span data-ttu-id="43920-124">Perdu et trouvé</span><span class="sxs-lookup"><span data-stu-id="43920-124">Lost and Found</span></span>

<span data-ttu-id="43920-125">Le conteneur de configuration a l’objet connu : objets supprimés.</span><span class="sxs-lookup"><span data-stu-id="43920-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="43920-126">Ces objets se trouvent dans chaque **domainDNS** et conteneur de configuration dans un service domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="43920-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="43920-127">Vous pouvez effectuer une liaison à un objet connu à l’aide du format de liaison WKGUID.</span><span class="sxs-lookup"><span data-stu-id="43920-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="43920-128">La liaison avec WKGUID est uniquement prise en charge dans Active Directory Domain Services, autrement dit, le fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="43920-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43920-129">Utilisez toujours le format de liaison WKGUID pour effectuer une liaison aux objets connus, comme indiqué ci-dessus, dans les conteneurs domaine et configuration.</span><span class="sxs-lookup"><span data-stu-id="43920-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="43920-130">Cela permet de s’assurer que ces conteneurs peuvent être liés, même s’ils sont déplacés ou renommés.</span><span class="sxs-lookup"><span data-stu-id="43920-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="43920-131">Le format de chaîne de liaison WKGUID est le suivant :</span><span class="sxs-lookup"><span data-stu-id="43920-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="43920-132">« &lt; Server name &gt; » est le nom du serveur d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="43920-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="43920-133">Le « &lt; nom du serveur &gt; » est facultatif.</span><span class="sxs-lookup"><span data-stu-id="43920-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="43920-134">« &lt; Xxxxx &gt; » est la représentation sous forme de chaîne de la valeur hexadécimale du GUID qui représente l’objet connu.</span><span class="sxs-lookup"><span data-stu-id="43920-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="43920-135">La chaîne GUID est spécifiée dans le formulaire « XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX » et n’est pas la même forme que la chaîne GUID produite par la fonction [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , qui prend la forme « {XXXXXXXX-XXXX-XXXX-xxxx-xxxxxxxxxxxx} ».</span><span class="sxs-lookup"><span data-stu-id="43920-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="43920-136">Pour plus d’informations et pour obtenir un exemple de code qui montre comment créer une chaîne pouvant être liée à partir d’un GUID, consultez l' [exemple de code permettant de créer une représentation sous forme de chaîne pouvant être liée d’un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="43920-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="43920-137">Pour effectuer une liaison à un objet spécifié dans **otherWellKnownObjects** dans un objet, spécifiez « &lt; xxxxx &gt; » comme forme de chaîne de liaison du GUID d’objet connu de l’objet.</span><span class="sxs-lookup"><span data-stu-id="43920-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="43920-138">Pour plus d’informations, consultez lecture de l’attribut [objectGUID d’un objet et création d’une représentation sous forme de chaîne du GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span><span class="sxs-lookup"><span data-stu-id="43920-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="43920-139">Pour plus d’informations sur la définition de la propriété **otherWellKnownObjects** sur les objets, consultez Activation de la [liaison de Rename-Safe avec la propriété otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span><span class="sxs-lookup"><span data-stu-id="43920-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="43920-140">Pour établir une liaison à un objet spécifié dans **wellKnownObjects** dans domainDNS ou dans des conteneurs de configuration, spécifiez « &lt; xxxxx &gt; » comme l’une des constantes suivantes, comme indiqué dans le tableau suivant, tel que défini dans ntdsapi. h.</span><span class="sxs-lookup"><span data-stu-id="43920-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="43920-141">Conteneur</span><span class="sxs-lookup"><span data-stu-id="43920-141">Container</span></span>          | <span data-ttu-id="43920-142">Identificateur GUID</span><span class="sxs-lookup"><span data-stu-id="43920-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="43920-143">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="43920-143">Users</span></span>              | <span data-ttu-id="43920-144">\_conteneur d’utilisateurs GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="43920-145">Ordinateurs</span><span class="sxs-lookup"><span data-stu-id="43920-145">Computers</span></span>          | <span data-ttu-id="43920-146">\_conteneur de calculs \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="43920-147">Système</span><span class="sxs-lookup"><span data-stu-id="43920-147">System</span></span>             | <span data-ttu-id="43920-148">\_conteneur de systèmes GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="43920-149">Contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="43920-149">Domain Controllers</span></span> | <span data-ttu-id="43920-150">\_conteneur de \_ contrôleurs de domaine GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="43920-151">Infrastructure</span><span class="sxs-lookup"><span data-stu-id="43920-151">Infrastructure</span></span>     | <span data-ttu-id="43920-152">conteneur d’infrastructure de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="43920-153">Objets supprimés</span><span class="sxs-lookup"><span data-stu-id="43920-153">Deleted Objects</span></span>    | <span data-ttu-id="43920-154">\_conteneur d' \_ objets supprimés GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="43920-155">Perdu et trouvé</span><span class="sxs-lookup"><span data-stu-id="43920-155">Lost and Found</span></span>     | <span data-ttu-id="43920-156">GUID \_ LOSTANDFOUND \_ conteneur \_ W</span><span class="sxs-lookup"><span data-stu-id="43920-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="43920-157">Par exemple, pour effectuer une liaison au conteneur utilisateur dans un domaine, spécifiez « xxxxx » comme **\_ conteneur des utilisateurs \_ \_ GUID** &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="43920-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="43920-158">« &lt; container dn &gt; » est le nom unique de l’objet conteneur qui a cet objet représenté en tant que valeur dans sa propriété **wellKnownObjects** .</span><span class="sxs-lookup"><span data-stu-id="43920-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="43920-159">Par exemple, pour effectuer une liaison au conteneur Users dans un domaine, spécifiez le nom unique du domaine comme « &lt; container dn &gt; ».</span><span class="sxs-lookup"><span data-stu-id="43920-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="43920-160">Par exemple, pour effectuer une liaison au conteneur Users du domaine Fabrikam.com, utilisez la chaîne de liaison suivante.</span><span class="sxs-lookup"><span data-stu-id="43920-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="43920-161">Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une liaison à un GUID connu, consultez l' [exemple de code pour la liaison à des objets bien connus](example-code-for-binding-to-well-known-objects.md).</span><span class="sxs-lookup"><span data-stu-id="43920-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 