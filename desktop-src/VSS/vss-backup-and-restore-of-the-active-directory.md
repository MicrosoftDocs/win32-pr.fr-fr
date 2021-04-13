---
description: L’enregistreur de Active Directory ne requiert aucune action spéciale pendant les opérations de sauvegarde.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Sauvegarde et restauration VSS du Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526290"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="ec83b-103">Sauvegarde et restauration VSS du Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec83b-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="ec83b-104">L’enregistreur de Active Directory ne requiert aucune action spéciale pendant les opérations de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ec83b-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="ec83b-105">Le rédacteur fournit au demandeur des informations sur les composants et les jeux de fichiers, et le demandeur utilise ces informations pour décider quels fichiers copier sur le support de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ec83b-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="ec83b-106">Il n’est pas nécessaire d’utiliser des API spéciales pour sauvegarder le Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec83b-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="ec83b-107">La façon dont une restauration est effectuée varie selon que la Active Directory est restaurée dans le cadre d’une opération de récupération d’urgence ou si la restauration s’effectue sur un système sur lequel le Active Directory s’exécute.</span><span class="sxs-lookup"><span data-stu-id="ec83b-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="ec83b-108">En outre, l’ancienneté de la copie de sauvegarde de l’état de Active Directory peut être un problème en raison de la Active Directory des objets tombstone.</span><span class="sxs-lookup"><span data-stu-id="ec83b-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="ec83b-109">Active Directory la restauration après une récupération d’urgence</span><span class="sxs-lookup"><span data-stu-id="ec83b-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="ec83b-110">Suite à un incident nécessitant une récupération d’urgence, le Active Directory peut être restauré dans le cadre de la restauration de l’état du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ec83b-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="ec83b-111">Cette opération de restauration est essentiellement une restauration en toute écriture.</span><span class="sxs-lookup"><span data-stu-id="ec83b-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="ec83b-112">Active Directory de la restauration sur le système sur lequel il s’exécute</span><span class="sxs-lookup"><span data-stu-id="ec83b-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="ec83b-113">Le système doit être redémarré en mode de restauration des services d’annuaire si le Active Directory est en cours d’exécution sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ec83b-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="ec83b-114">Le système d’exploitation s’exécute alors sans la Active Directory, et toute la validation de l’utilisateur se produit par le biais du gestionnaire de comptes de sécurité (SAM) dans le registre.</span><span class="sxs-lookup"><span data-stu-id="ec83b-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="ec83b-115">Seul l’administrateur a l’autorisation de récupérer les Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec83b-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="ec83b-116">Une fois en mode de restauration du service d’annuaire, une restauration VSS peut se poursuivre normalement.</span><span class="sxs-lookup"><span data-stu-id="ec83b-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="ec83b-117">Il n’y a aucune raison d’utiliser des API de Active Directory Win32 non-VSS pour restaurer l’état de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec83b-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="ec83b-118">Active Directory restaure et Active Directory les objets tombstone</span><span class="sxs-lookup"><span data-stu-id="ec83b-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="ec83b-119">Tout plan de récupération doit s’assurer que l’ancienneté de la sauvegarde ne doit pas dépasser la durée de vie de désactivation Active Directory (60 jours par défaut).</span><span class="sxs-lookup"><span data-stu-id="ec83b-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="ec83b-120">La restauration d’une sauvegarde antérieure à l’objet tombstone entraînera un contrôleur de domaine à avoir des objets qui ne sont pas répliqués sur les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="ec83b-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="ec83b-121">Les objets qui ne sont pas répliqués ne sont pas supprimés automatiquement sur ce contrôleur de domaine (restauré), car les objets tombstone de ces objets sur les autres réplicas ont déjà été supprimés.</span><span class="sxs-lookup"><span data-stu-id="ec83b-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="ec83b-122">Un administrateur doit supprimer manuellement chacun des objets sur le contrôleur de domaine restauré qui ne sont pas répliqués.</span><span class="sxs-lookup"><span data-stu-id="ec83b-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="ec83b-123">Les sauvegardes incrémentielles des Active Directory ne sont pas prises en charge ; une sauvegarde complète est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ec83b-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



