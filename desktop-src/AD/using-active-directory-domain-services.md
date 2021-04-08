---
title: Utilisation des services de domaine Active Directory
description: Cette section fournit des instructions relatives à l’écriture d’applications qui utilisent ou publient des données dans un service d’annuaire Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, utilisation
- Active Directory Active Directory Domain Services, utilisation
- Exemples de Active Directory Active Directory
- Exemples de Active Directory Domain Services Active Directory
- exemples Active Directory
- Active Directory Active Directory, exemples voir Active Directory Domain Services exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734548"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="e76f9-109">Utilisation des services de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="e76f9-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="e76f9-110">Cette section fournit des instructions relatives à l’écriture d’applications qui utilisent ou publient des données dans un service d’annuaire Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e76f9-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="e76f9-111">La documentation suivante est destinée aux programmeurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="e76f9-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="e76f9-112">Si vous essayez de résoudre une erreur d’impression Active Directory, consultez les [suggestions suivantes](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) sur les pages de la communauté Microsoft. Si cela ne vous aide pas, essayez ces recommandations à partir de [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span><span class="sxs-lookup"><span data-stu-id="e76f9-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="e76f9-113">Active Directory Domain Services sont conformes à Lightweight Directory Access Protocol 3,0, qui est défini par RFC 2251 et d’autres RFC.</span><span class="sxs-lookup"><span data-stu-id="e76f9-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="e76f9-114">Les jeux d’API suivants peuvent être utilisés pour accéder à Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e76f9-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="e76f9-115">Chaque ensemble d’API présente des avantages et des inconvénients qui dépendent du langage de programmation, de l’environnement de programmation et de la méthode d’exécution prévue.</span><span class="sxs-lookup"><span data-stu-id="e76f9-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="e76f9-116">La majorité des exemples de ce guide utilisent ADSI, qui est pris en charge par les langages tels que C et C++, ainsi que les langages compatibles Automation tels que Microsoft Visual Basic et Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="e76f9-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="e76f9-117">Pour plus d’informations sur les technologies Active Directory Domain Services spécifiques, consultez :</span><span class="sxs-lookup"><span data-stu-id="e76f9-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="e76f9-118">Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="e76f9-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="e76f9-119">Interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="e76f9-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="e76f9-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="e76f9-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="e76f9-121">Cette section aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="e76f9-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="e76f9-122">Liaison à Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e76f9-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="e76f9-123">Recherche dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e76f9-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e76f9-124">Création et suppression d’objets dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e76f9-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e76f9-125">Déplacement d’objets</span><span class="sxs-lookup"><span data-stu-id="e76f9-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="e76f9-126">Lecture et écriture des attributs d’objets dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e76f9-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e76f9-127">Contrôle de l’accès aux objets dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e76f9-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e76f9-128">Extension du schéma</span><span class="sxs-lookup"><span data-stu-id="e76f9-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="e76f9-129">Extension de l’interface utilisateur pour les objets d’annuaire</span><span class="sxs-lookup"><span data-stu-id="e76f9-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="e76f9-130">Gestion des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e76f9-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="e76f9-131">Gestion des groupes</span><span class="sxs-lookup"><span data-stu-id="e76f9-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="e76f9-132">Suivi des modifications</span><span class="sxs-lookup"><span data-stu-id="e76f9-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="e76f9-133">Publication de service</span><span class="sxs-lookup"><span data-stu-id="e76f9-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="e76f9-134">Comptes d’ouverture de session du service</span><span class="sxs-lookup"><span data-stu-id="e76f9-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="e76f9-135">Authentification mutuelle à l'aide de Kerberos</span><span class="sxs-lookup"><span data-stu-id="e76f9-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="e76f9-136">Sauvegarde et restauration de Active Directory</span><span class="sxs-lookup"><span data-stu-id="e76f9-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="e76f9-137">Stockage des Dynamic Data</span><span class="sxs-lookup"><span data-stu-id="e76f9-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="e76f9-138">Partitions de l’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="e76f9-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="e76f9-139">Détection du mode d’opération d’un domaine</span><span class="sxs-lookup"><span data-stu-id="e76f9-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 