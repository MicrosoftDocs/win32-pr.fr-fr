---
title: Activation de la liaison de Rename-Safe avec la propriété otherWellKnownObjects
description: Les objets de la classe de conteneur ont un attribut otherWellKnownObjects que vous pouvez utiliser pour associer un GUID au nom unique (DN) d’un objet enfant dans le conteneur.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- propriété otherWellKnownObjects
- propriété otherWellKnownObjects, à l’aide de pour une liaison de renommage sécurisée
- Active Directory, utilisation de, liaison, liaison de renommage sécurisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190770"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="7fad4-106">Activation de la liaison de Rename-Safe avec la propriété otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="7fad4-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="7fad4-107">Les objets de la classe de conteneur ont un attribut **otherWellKnownObjects** que vous pouvez utiliser pour associer un GUID au nom unique (DN) d’un objet enfant dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="7fad4-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="7fad4-108">Si l’objet enfant est déplacé ou renommé, le serveur Active Directory met à jour le DN dans la valeur **otherWellKnownObjects** de cet objet enfant.</span><span class="sxs-lookup"><span data-stu-id="7fad4-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="7fad4-109">Cela permet d’utiliser la fonctionnalité de liaison WKGUID pour établir une liaison à l’objet enfant à l’aide du GUID et du DN du conteneur plutôt que du DN de l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="7fad4-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="7fad4-110">L’attribut **otherWellKnownObjects** est équivalent à l’attribut **wellKnownObjects** , à ceci près que les applications et services peuvent écrire une valeur **otherWellKnownObjects** , mais que seul le système peut écrire **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="7fad4-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="7fad4-111">L’utilisation de l’attribut **otherWellKnownObjects** et de la liaison WKGUID est bénéfique dans les cas suivants où la liaison de renommage sécurisée est requise par rapport à un objet conteneur spécifique.</span><span class="sxs-lookup"><span data-stu-id="7fad4-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="7fad4-112">Si un objet conteneur contient d’autres objets importants ou si des objets importants peuvent être renommés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="7fad4-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="7fad4-113">Si les objets importants existent pour chaque instance de l’objet conteneur.</span><span class="sxs-lookup"><span data-stu-id="7fad4-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="7fad4-114">Par exemple, le système utilise l’attribut **wellKnownObjects** de chaque objet **domainDNS** pour stocker une valeur pour le conteneur Users, qui existe dans chaque instance d’un objet **domainDNS** .</span><span class="sxs-lookup"><span data-stu-id="7fad4-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="7fad4-115">Cela permet aux applications de se lier au conteneur Users de manière sécurisée en spécifiant le GUID connu et le DN du conteneur **domainDNS** .</span><span class="sxs-lookup"><span data-stu-id="7fad4-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="7fad4-116">Les applications peuvent utiliser l’attribut **otherWellKnownObjects** d’un conteneur de la même façon.</span><span class="sxs-lookup"><span data-stu-id="7fad4-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="7fad4-117">Si vous avez besoin d’une liaison et/ou d’une fonctionnalité de recherche de renommage sécurisé sur les objets importants.</span><span class="sxs-lookup"><span data-stu-id="7fad4-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="7fad4-118">**Pour ajouter des fonctionnalités de recherche et de liaison avec renommage sécurisé**</span><span class="sxs-lookup"><span data-stu-id="7fad4-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="7fad4-119">Ajoutez une valeur à la propriété **otherWellKnownObjects** de l’objet conteneur lorsque l’objet important est créé dans ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="7fad4-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="7fad4-120">La valeur contient le GUID qui représente l’objet connu.</span><span class="sxs-lookup"><span data-stu-id="7fad4-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="7fad4-121">N’oubliez pas qu’il ne s’agit pas de l' **objectGUID** et du **distinguishedName** pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="7fad4-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="7fad4-122">Utilisez la fonctionnalité de liaison WKGUID pour effectuer une liaison ou une recherche dans l’objet important.</span><span class="sxs-lookup"><span data-stu-id="7fad4-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="7fad4-123">L’attribut **otherWellKnownObjects** peut avoir plusieurs valeurs et contient les tuples GUID/DN des objets connus dans les conteneurs sur lesquels ils sont définis.</span><span class="sxs-lookup"><span data-stu-id="7fad4-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="7fad4-124">L’attribut **otherWellKnownObjects** a la syntaxe DNWithBinary dans laquelle les valeurs se présentent sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="7fad4-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="7fad4-125">Dans cet exemple, « &lt; nombre &gt; de caractères » est le nombre de chiffres hexadécimaux dans « &lt; GUID connu &gt; », qui est 32 (nombre de chiffres hexadécimaux dans un GUID) pour **otherWellKnownObjects** et **wellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="7fad4-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="7fad4-126">« &lt; GUID connu &gt; » est la représentation de chiffres hexadécimaux du GUID connu.</span><span class="sxs-lookup"><span data-stu-id="7fad4-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="7fad4-127">« &lt; Object DN &gt; » est le nom unique de l’objet représenté par cette valeur WKO.</span><span class="sxs-lookup"><span data-stu-id="7fad4-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="7fad4-128">Le serveur gère la partie ObjectDN de chaque valeur **wellKnownObjects** et **otherWellKnownObjects** afin qu’il contienne le nom unique actuel de l’objet spécifié à l’origine lors de la création de la valeur.</span><span class="sxs-lookup"><span data-stu-id="7fad4-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="7fad4-129">Par exemple, si {df447b5e-AA5B-11D2-8D53-00c04f79ab81} est le GUID connu de l’objet MyObject dans le conteneur MyContainer du domaine Fabrikam.com, la valeur **otherWellKnownObjects** spécifie le GUID connu et le DN de MyObject :</span><span class="sxs-lookup"><span data-stu-id="7fad4-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="7fad4-130">Pour effectuer une liaison à cet objet, utilisez la chaîne de liaison WKGUID suivante qui spécifie le GUID connu de l’objet et le DN du conteneur :</span><span class="sxs-lookup"><span data-stu-id="7fad4-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="7fad4-131">Après la liaison à cet objet, vous pouvez utiliser les interfaces COM ADSI pour rechercher, lire, modifier ou supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="7fad4-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="7fad4-132">Pour plus d’informations et pour obtenir un exemple de code qui montre comment ajouter un objet à l’attribut **otherWellKnownObjects** , consultez l' [exemple de code pour la création d’un objet conteneur](example-code-for-creating-a-container-object.md).</span><span class="sxs-lookup"><span data-stu-id="7fad4-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 




