---
title: À propos de Active Directory Domain Services
description: Ce guide fournit des informations essentielles pour l’intégration de Microsoft Active Directory dans des applications distribuées conçues pour les systèmes d’exploitation qui prennent en charge Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, à propos de
- Active Directory Active Directory Domain Services, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031284"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="86bc9-105">À propos de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="86bc9-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="86bc9-106">Écrire des applications puissantes qui utilisent Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="86bc9-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="86bc9-107">Ce guide fournit des informations essentielles pour l’intégration de Active Directory Domain Services dans des applications distribuées conçues pour les systèmes d’exploitation qui prennent en charge Active Directory Domain Services, notamment :</span><span class="sxs-lookup"><span data-stu-id="86bc9-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="86bc9-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86bc9-108">Windows Server 2008</span></span>
-   <span data-ttu-id="86bc9-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86bc9-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="86bc9-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86bc9-110">Windows Server 2012</span></span>
-   <span data-ttu-id="86bc9-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="86bc9-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="86bc9-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="86bc9-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="86bc9-113">Ces rubriques concernent les développeurs de logiciels.</span><span class="sxs-lookup"><span data-stu-id="86bc9-113">These topics are for software developers.</span></span> <span data-ttu-id="86bc9-114">Pour les problèmes de support, consultez [support Microsoft](https://windows.microsoft.com/windows/support#1tc).</span><span class="sxs-lookup"><span data-stu-id="86bc9-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="86bc9-115">Pour plus d’informations sur l’administration de Active Directory, consultez [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) sur TechNet.</span><span class="sxs-lookup"><span data-stu-id="86bc9-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="86bc9-116">Fonctionnalités d’annuaire fondamentales</span><span class="sxs-lookup"><span data-stu-id="86bc9-116">Fundamental Directory Features</span></span>

<span data-ttu-id="86bc9-117">Un service d’annuaire est un service fondamental pour les applications distribuées.</span><span class="sxs-lookup"><span data-stu-id="86bc9-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="86bc9-118">Un service d’annuaire doit fournir les fonctionnalités indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="86bc9-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="86bc9-119">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="86bc9-119">Feature</span></span>               | <span data-ttu-id="86bc9-120">Description</span><span class="sxs-lookup"><span data-stu-id="86bc9-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86bc9-121">Transparence de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="86bc9-121">Location transparency</span></span> | <span data-ttu-id="86bc9-122">En mesure de trouver l’utilisateur, le groupe, le service en réseau ou la ressource, les données sans l’adresse de l’objet</span><span class="sxs-lookup"><span data-stu-id="86bc9-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="86bc9-123">Données d’objet</span><span class="sxs-lookup"><span data-stu-id="86bc9-123">Object data</span></span>           | <span data-ttu-id="86bc9-124">Possibilité de stocker des données d’utilisateur, de groupe, d’organisation et de service dans une arborescence hiérarchique</span><span class="sxs-lookup"><span data-stu-id="86bc9-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="86bc9-125">Requête enrichie</span><span class="sxs-lookup"><span data-stu-id="86bc9-125">Rich query</span></span>            | <span data-ttu-id="86bc9-126">En mesure de localiser un objet en interrogeant les propriétés de l’objet</span><span class="sxs-lookup"><span data-stu-id="86bc9-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="86bc9-127">Haute disponibilité</span><span class="sxs-lookup"><span data-stu-id="86bc9-127">High availability</span></span>     | <span data-ttu-id="86bc9-128">Possibilité de localiser un réplica du répertoire à un emplacement efficace pour les opérations de lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="86bc9-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="86bc9-129">Fonctionnalités avancées de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="86bc9-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="86bc9-130">Active Directory Domain Services fournit les fonctionnalités listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="86bc9-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86bc9-131">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="86bc9-131">Feature</span></span></th>
<th><span data-ttu-id="86bc9-132">Description</span><span class="sxs-lookup"><span data-stu-id="86bc9-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86bc9-133">Prise en charge des normes Internet</span><span class="sxs-lookup"><span data-stu-id="86bc9-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="86bc9-134">Active Directory Domain Services implémente ses fonctionnalités conformément aux normes Internet publiées, telles que LDAP et DNS.</span><span class="sxs-lookup"><span data-stu-id="86bc9-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86bc9-135">Sécurité étroitement intégrée et flexible</span><span class="sxs-lookup"><span data-stu-id="86bc9-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="86bc9-136">Les avantages sont notamment les suivants :</span><span class="sxs-lookup"><span data-stu-id="86bc9-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="86bc9-137">Choix des packages d’authentification.</span><span class="sxs-lookup"><span data-stu-id="86bc9-137">Choice of authentication packages.</span></span> <span data-ttu-id="86bc9-138">Kerberos, SSL (Secure Sockets Layer) (SSL) ou une combinaison ; par exemple, établissez un canal SSL pour le chiffrement, puis utilisez Kerberos pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="86bc9-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="86bc9-139">Gestion centralisée de l’accès aux services et aux ressources à l’aide des utilisateurs et des groupes dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="86bc9-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="86bc9-140">Délégation de l’administration afin que les administrateurs centraux puissent déléguer des tâches d’administration telles que la modification de mot de passe ou la création et la suppression d’objets spécifiques.</span><span class="sxs-lookup"><span data-stu-id="86bc9-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="86bc9-141">Le serveur Active Directory utilise les mêmes mécanismes de contrôle d’accès que ceux utilisés sur les systèmes de fichiers dans les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="86bc9-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="86bc9-142">Ainsi, les outils qui gèrent le contrôle d’accès sur un système de fichiers fonctionnent pour Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="86bc9-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="86bc9-143">Infrastructure de clé publique complète.</span><span class="sxs-lookup"><span data-stu-id="86bc9-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="86bc9-144">Le serveur de certificats Microsoft et la prise en charge des cartes à puce sont intégrés à Active Directory Domain Services pour fournir la gestion des certificats et des ouvertures de session par carte à puce.</span><span class="sxs-lookup"><span data-stu-id="86bc9-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86bc9-145">Facile à programmer</span><span class="sxs-lookup"><span data-stu-id="86bc9-145">Easily programmable</span></span></td>
<td><span data-ttu-id="86bc9-146">Le serveur Active Directory peut être accessible par programmation et administré à l’aide de l’API des <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfaces de Service Active Directory</a> , de l’API <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> ou de l’espace de noms <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</span><span class="sxs-lookup"><span data-stu-id="86bc9-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86bc9-147">Services système activés pour les annuaires</span><span class="sxs-lookup"><span data-stu-id="86bc9-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="86bc9-148">Votre application cliente peut être facilement déployée sur des bureaux distribués en créant un package Windows Installer et en utilisant la fonctionnalité de déploiement d’application disponible dans les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="86bc9-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86bc9-149">Intégration d’application clé</span><span class="sxs-lookup"><span data-stu-id="86bc9-149">Key application integration</span></span></td>
<td><span data-ttu-id="86bc9-150">Les applications distribuées de clés, telles qu’Exchange, sont intégrées à Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="86bc9-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="86bc9-151">Ainsi, les entreprises peuvent réduire le nombre de services d’annuaire à gérer.</span><span class="sxs-lookup"><span data-stu-id="86bc9-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86bc9-152">Schéma riche et extensible</span><span class="sxs-lookup"><span data-stu-id="86bc9-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="86bc9-153">Le schéma définit les objets et les propriétés qui peuvent être écrits et lus à partir d’un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="86bc9-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="86bc9-154">Le schéma Active Directory est riche.</span><span class="sxs-lookup"><span data-stu-id="86bc9-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="86bc9-155">La plupart des objets et propriétés nécessaires à un service sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="86bc9-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="86bc9-156">Si ce n’est pas le cas, une application distribuée peut étendre le schéma pour prendre en charge les spécifications de l’application.</span><span class="sxs-lookup"><span data-stu-id="86bc9-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="86bc9-157">Pour plus d’informations sur Active Directory Domain Services, consultez :</span><span class="sxs-lookup"><span data-stu-id="86bc9-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="86bc9-158">Concepts de base de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="86bc9-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="86bc9-159">Architecture Active Directory</span><span class="sxs-lookup"><span data-stu-id="86bc9-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="86bc9-160">Schéma Active Directory</span><span class="sxs-lookup"><span data-stu-id="86bc9-160">Active Directory Schema</span></span>](active-directory-schema.md)

