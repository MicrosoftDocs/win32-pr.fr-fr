---
title: Partitions de l’annuaire d’applications
description: Dans Windows Server 2003, Active Directory Domain Services prendre en charge les partitions d’annuaire d’applications.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Partitions de l’annuaire d’applications Active Directory
- Partitions de l’annuaire d’applications Active Directory, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031055"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="52bc1-105">Partitions de l’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-105">Application Directory Partitions</span></span>

<span data-ttu-id="52bc1-106">Dans Windows Server 2003, Active Directory Domain Services prendre en charge les partitions d’annuaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="52bc1-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="52bc1-107">Une partition d’annuaire d’applications peut contenir une hiérarchie de tout type d’objets, à l’exception des principaux de sécurité, et peut être configurée pour répliquer sur n’importe quel ensemble de contrôleurs de domaine dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="52bc1-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="52bc1-108">Contrairement à une partition de domaine, il n’est pas nécessaire qu’une partition d’annuaire d’applications soit répliquée sur tous les contrôleurs de domaine d’un domaine, et la partition peut être répliquée sur des contrôleurs de domaine dans différents domaines de la forêt.</span><span class="sxs-lookup"><span data-stu-id="52bc1-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="52bc1-109">Pour plus d’informations sur les partitions de l’annuaire d’applications, consultez [à propos des partitions de l’annuaire d’applications](about-application-directory-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="52bc1-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="52bc1-110">Une partition d’annuaire d’applications peut être créée.</span><span class="sxs-lookup"><span data-stu-id="52bc1-110">An application directory partition can be created.</span></span> <span data-ttu-id="52bc1-111">modifié et supprimé à l’aide des opérations ADSI standard, LDAP et [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="52bc1-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="52bc1-112">Le contexte de sécurité requis pour créer et modifier une partition d’annuaire d’applications est le même que pour la création d’une partition de domaine.</span><span class="sxs-lookup"><span data-stu-id="52bc1-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="52bc1-113">Les rubriques suivantes décrivent comment utiliser les partitions d’annuaire d’applications :</span><span class="sxs-lookup"><span data-stu-id="52bc1-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="52bc1-114">Réplication de la partition de l’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="52bc1-115">Sécurité de la partition de l’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="52bc1-116">Création d’une partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="52bc1-117">Suppression d’une partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="52bc1-118">Énumération des partitions d’annuaire d’applications dans une forêt</span><span class="sxs-lookup"><span data-stu-id="52bc1-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="52bc1-119">Localisation d’un serveur hôte de partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="52bc1-120">Ajout ou suppression d’un réplica de partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="52bc1-121">Énumération des réplicas d’une partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="52bc1-122">Modification de la configuration de la partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="52bc1-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 