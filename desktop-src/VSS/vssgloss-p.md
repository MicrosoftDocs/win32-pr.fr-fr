---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526278"
---
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="b9b98-103">P (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="b9b98-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="b9b98-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="b9b98-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b9b98-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**prise en charge partielle des fichiers**</span><span class="sxs-lookup"><span data-stu-id="b9b98-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-106">Capacité à implémenter des opérations de sauvegarde en modifiant les sous-sections des fichiers impliqués, plutôt que d’utiliser l’ensemble des fichiers.</span><span class="sxs-lookup"><span data-stu-id="b9b98-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="b9b98-107">Voir aussi [*ciblage dirigé*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="b9b98-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**cliché instantané persistant**</span><span class="sxs-lookup"><span data-stu-id="b9b98-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-109">Cliché instantané qui n’est pas supprimé automatiquement lorsque le demandeur libère un objet [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou lorsque l’ordinateur est redémarré.</span><span class="sxs-lookup"><span data-stu-id="b9b98-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="b9b98-110">Voir aussi cliché [*instantané avec mise en sortie automatique*](vssgloss-a.md), cliché [*instantané*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b9b98-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Duplex**</span><span class="sxs-lookup"><span data-stu-id="b9b98-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-112">Type spécial de volume de clichés instantanés qui représente entièrement et complètement un volume de clichés instantanés sans avoir besoin de l’un des volumes originaux.</span><span class="sxs-lookup"><span data-stu-id="b9b98-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="b9b98-113">Il s’agit également d’un miroir scindé, mais cette documentation utilise le terme Plex.</span><span class="sxs-lookup"><span data-stu-id="b9b98-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Événement PostRestore**</span><span class="sxs-lookup"><span data-stu-id="b9b98-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-115">Événement VSS indiquant qu’une restauration VSS est terminée.</span><span class="sxs-lookup"><span data-stu-id="b9b98-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Événement PostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="b9b98-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-117">Événement VSS indiquant qu’un cliché instantané a été effectué.</span><span class="sxs-lookup"><span data-stu-id="b9b98-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="b9b98-118">Voir aussi cliché [*instantané*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b9b98-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Événement PrepareForBackup**</span><span class="sxs-lookup"><span data-stu-id="b9b98-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-120">Événement VSS indiquant qu’une opération de sauvegarde est sur le point d’être effectuée.</span><span class="sxs-lookup"><span data-stu-id="b9b98-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Événement PrepareForSnapshot**</span><span class="sxs-lookup"><span data-stu-id="b9b98-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-122">Événement VSS indiquant que les rédacteurs doivent prendre des mesures pour préparer une opération de cliché instantané à venir.</span><span class="sxs-lookup"><span data-stu-id="b9b98-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="b9b98-123">Voir aussi cliché [*instantané*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b9b98-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Événement de prérestauration**</span><span class="sxs-lookup"><span data-stu-id="b9b98-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-125">Événement VSS indiquant qu’une opération de restauration est sur le point d’être effectuée.</span><span class="sxs-lookup"><span data-stu-id="b9b98-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="b9b98-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**moteur**</span><span class="sxs-lookup"><span data-stu-id="b9b98-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="b9b98-127">Objet de système d’exploitation qui intercepte et gère les demandes d’e/s afin de créer et de représenter des clichés instantanés de volume dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b9b98-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="b9b98-128">Voir aussi [*fournisseur de matériel*](vssgloss-h.md), [*fournisseur de logiciels*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b9b98-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



