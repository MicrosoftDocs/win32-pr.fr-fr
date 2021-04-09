---
title: Liaison à Active Directory Domain Services
description: Dans Active Directory Domain Services, l’action consistant à associer un objet de programmation à un objet Active Directory Domain Services spécifique est appelée liaison.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- liaison à Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, liaison à
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950459"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="5e082-105">Liaison à Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="5e082-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="5e082-106">Dans Active Directory Domain Services, l’action consistant à associer un objet de programmation à un objet Active Directory Domain Services spécifique est appelée *liaison*.</span><span class="sxs-lookup"><span data-stu-id="5e082-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="5e082-107">Lorsqu’un objet de programmation, tel qu’un objet [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , est associé à un objet d’annuaire spécifique, l’objet de programmation est considéré comme *lié à* l’objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="5e082-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="5e082-108">Liaison de fonctions et de méthodes</span><span class="sxs-lookup"><span data-stu-id="5e082-108">Binding Functions and Methods</span></span>

<span data-ttu-id="5e082-109">La méthode de liaison par programmation à un objet Active Directory dépend de la technologie de programmation utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e082-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="5e082-110">Pour plus d’informations sur la liaison à des objets dans Active Directory Domain Services avec une technologie de programmation spécifique, consultez les rubriques figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5e082-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="5e082-111">Technologie de programmation</span><span class="sxs-lookup"><span data-stu-id="5e082-111">Programming technology</span></span>                                                                       | <span data-ttu-id="5e082-112">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="5e082-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="5e082-113">Interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="5e082-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="5e082-114">Liaison à un objet ADSI</span><span class="sxs-lookup"><span data-stu-id="5e082-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="5e082-115">Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="5e082-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="5e082-116">Établissement d’une session LDAP</span><span class="sxs-lookup"><span data-stu-id="5e082-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="5e082-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="5e082-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="5e082-118">[Liaison à des objets d’annuaire](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="5e082-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="5e082-119">Chaînes de liaison</span><span class="sxs-lookup"><span data-stu-id="5e082-119">Binding Strings</span></span>

<span data-ttu-id="5e082-120">Toutes les fonctions et méthodes de liaison requièrent une chaîne de liaison.</span><span class="sxs-lookup"><span data-stu-id="5e082-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="5e082-121">Le formulaire de la chaîne de liaison dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5e082-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="5e082-122">Les Active Directory Domain Services sont pris en charge par deux fournisseurs, LDAP et Winnt.</span><span class="sxs-lookup"><span data-stu-id="5e082-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="5e082-123">À partir de Windows 2000, le fournisseur LDAP est utilisé pour accéder à Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5e082-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="5e082-124">La chaîne de liaison LDAP peut prendre l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e082-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="5e082-125">« LDAP:// <host name> / <object name> »</span><span class="sxs-lookup"><span data-stu-id="5e082-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="5e082-126">« GC:// <host name> / <object name> »</span><span class="sxs-lookup"><span data-stu-id="5e082-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="5e082-127">Dans les exemples ci-dessus, « LDAP : » spécifie le fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="5e082-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="5e082-128">« GC : » utilise le fournisseur LDAP pour effectuer une liaison au service de catalogue global afin d’exécuter des requêtes rapides.</span><span class="sxs-lookup"><span data-stu-id="5e082-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="5e082-129">« &lt; host name &gt; » spécifie le serveur auquel se lier et est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5e082-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="5e082-130">Si possible, ne spécifiez pas de serveur.</span><span class="sxs-lookup"><span data-stu-id="5e082-130">If possible, do not specify a server.</span></span> <span data-ttu-id="5e082-131">Il est également possible de créer une liaison avec un objet dans un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="5e082-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="5e082-132">Pour ce faire, transmettez le nom DNS du domaine cible pour « &lt; nom d’hôte &gt; ».</span><span class="sxs-lookup"><span data-stu-id="5e082-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="5e082-133">Par exemple, pour effectuer une liaison au conteneur Users dans le domaine domaine2 de fabrikam.com, la chaîne de liaison serait « LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com ».</span><span class="sxs-lookup"><span data-stu-id="5e082-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="5e082-134">« &lt; nom de l’objet &gt; » représente un objet spécifique dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5e082-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="5e082-135">Le nom de l’objet peut être un nom unique ou un GUID d’objet.</span><span class="sxs-lookup"><span data-stu-id="5e082-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="5e082-136">Pour plus d’informations sur les chaînes de liaison LDAP, consultez [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span><span class="sxs-lookup"><span data-stu-id="5e082-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="5e082-137">Pour Windows NT 4,0, le fournisseur Winnt est utilisé pour accéder aux données d’annuaire, telles que les utilisateurs, les groupes d’utilisateurs, les ordinateurs, les services et d’autres objets réseau dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5e082-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="5e082-138">Le fournisseur Winnt sur les systèmes Windows 2000 et versions ultérieures a des fonctionnalités limitées par rapport au fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="5e082-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="5e082-139">Pour plus d’informations sur les chaînes de liaison WinNT, consultez [winnt ADsPath](/windows/desktop/ADSI/winnt-adspath).</span><span class="sxs-lookup"><span data-stu-id="5e082-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="5e082-140">Un ADsPath de « LDAP:// » ou « GC:// » peut être utilisé pour établir une liaison à la racine de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="5e082-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="5e082-141">Lorsqu’il est lié à la racine de l’espace de noms, l’objet Namespace fourni ne contient aucune propriété et contient l’objet de domaine pour LDAP et un objet Container contenant un réplica partiel de tous les domaines de la forêt pour GC.</span><span class="sxs-lookup"><span data-stu-id="5e082-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="5e082-142">Pour plus d’informations sur la liaison dans Active Directory Domain Services, consultez :</span><span class="sxs-lookup"><span data-stu-id="5e082-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="5e082-143">Liaison sans serveur et RootDSE</span><span class="sxs-lookup"><span data-stu-id="5e082-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="5e082-144">Liaison au catalogue global</span><span class="sxs-lookup"><span data-stu-id="5e082-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="5e082-145">Utilisation d’objectGUID pour la liaison à un objet</span><span class="sxs-lookup"><span data-stu-id="5e082-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="5e082-146">Liaison à des objets Well-Known à l’aide de WKGUID</span><span class="sxs-lookup"><span data-stu-id="5e082-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="5e082-147">Liaison à un objet à l’aide d’un SID</span><span class="sxs-lookup"><span data-stu-id="5e082-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="5e082-148">Activation de la liaison de Rename-Safe avec la propriété otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="5e082-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="5e082-149">Authentification</span><span class="sxs-lookup"><span data-stu-id="5e082-149">Authentication</span></span>](authentication.md)

 

 
