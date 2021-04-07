---
title: Sauvegarde et restauration d’un serveur Active Directory
description: Active Directory Domain Services fournir des fonctions pour sauvegarder et restaurer des données dans la base de données d’annuaire.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, utilisation, sauvegarde et restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724652"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="6ec2c-104">Sauvegarde et restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="6ec2c-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="6ec2c-105">Active Directory Domain Services fournir des fonctions pour sauvegarder et restaurer des données dans la base de données d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="6ec2c-106">Cette section décrit comment [sauvegarder](backing-up-an-active-directory-server.md) et [restaurer](restoring-an-active-directory-server.md) un serveur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="6ec2c-107">Pour plus d’informations sur la sauvegarde d’un serveur Active Directory à l’aide des utilitaires fournis dans les systèmes d’exploitation Windows 2000 et Windows Server 2003, consultez le kit de ressources applicables, disponible sur le site Web Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="6ec2c-108">La sauvegarde d’un serveur de Active Directory doit être effectuée en ligne et doit être effectuée lors de l’installation du Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="6ec2c-109">Active Directory Domain Services reposent sur une base de données spéciale et exportent un ensemble de fonctions de sauvegarde qui fournissent l’interface de sauvegarde par programme.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="6ec2c-110">La sauvegarde ne prend pas en charge les sauvegardes incrémentielles.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="6ec2c-111">Une application de sauvegarde se lie à une DLL côté client locale avec des points d’entrée définis dans ntdsbcli. h.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="6ec2c-112">La restauration d’un serveur Active Directory est toujours effectuée en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="6ec2c-113">Bien que les rubriques de cette section décrivent uniquement comment sauvegarder et restaurer un serveur Active Directory, sachez que Windows 2000 et les systèmes d’exploitation Windows Server 2003 disposent de plusieurs composants « État du système » qui doivent être sauvegardés et restaurés ensemble.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="6ec2c-114">Ces composants d’État du système sont constitués des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6ec2c-114">These system state components consist of:</span></span>

-   <span data-ttu-id="6ec2c-115">Fichiers de démarrage tels que Ntldr, Ntdetect, tous les fichiers protégés par SFP et la configuration du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="6ec2c-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="6ec2c-116">Contrôleur domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="6ec2c-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="6ec2c-117">SysVol (contrôleur de domaine uniquement)</span><span class="sxs-lookup"><span data-stu-id="6ec2c-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="6ec2c-118">Serveur de certificats (CA uniquement)</span><span class="sxs-lookup"><span data-stu-id="6ec2c-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="6ec2c-119">Base de données de cluster (nœud de cluster uniquement)</span><span class="sxs-lookup"><span data-stu-id="6ec2c-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="6ec2c-120">Registre</span><span class="sxs-lookup"><span data-stu-id="6ec2c-120">Registry</span></span>
-   <span data-ttu-id="6ec2c-121">Base de données d’inscription de classe COM+</span><span class="sxs-lookup"><span data-stu-id="6ec2c-121">COM+ class registration database</span></span>

<span data-ttu-id="6ec2c-122">L’état du système peut être sauvegardé dans n’importe quel ordre, mais la restauration de l’état du système doit se produire dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="6ec2c-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="6ec2c-123">Restaurez les fichiers de démarrage.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="6ec2c-124">Restaurez SysVol, le serveur de certificats, la base de données de cluster et la base de données d’inscription de classe COM+, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="6ec2c-125">Restaurez le serveur de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="6ec2c-126">Restaurez le registre.</span><span class="sxs-lookup"><span data-stu-id="6ec2c-126">Restore the registry.</span></span>

<span data-ttu-id="6ec2c-127">Pour plus d’informations sur la sauvegarde et la restauration des services de certificats, consultez [utilisation des fonctions de sauvegarde et de restauration des services de certificats](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span><span class="sxs-lookup"><span data-stu-id="6ec2c-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="6ec2c-128">Pour plus d’informations sur la sauvegarde et la restauration de Active Directory Domain Services, consultez :</span><span class="sxs-lookup"><span data-stu-id="6ec2c-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="6ec2c-129">Considérations relatives à la sauvegarde Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6ec2c-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="6ec2c-130">Sauvegarde d’un serveur de Active Directory</span><span class="sxs-lookup"><span data-stu-id="6ec2c-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="6ec2c-131">Restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="6ec2c-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="6ec2c-132">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="6ec2c-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 