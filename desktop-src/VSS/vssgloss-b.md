---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318405"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="bcc39-103">B (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="bcc39-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="bcc39-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="bcc39-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bcc39-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**applications de niveau principal**</span><span class="sxs-lookup"><span data-stu-id="bcc39-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="bcc39-106">Indique le point auquel un writer est notifié d’un gel par VSS.</span><span class="sxs-lookup"><span data-stu-id="bcc39-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="bcc39-107">Les enregistreurs qui sont initialisés en tant qu’applications de niveau principal sont avertis après que les Writers ont été initialisés en tant qu’applications de niveau frontal et antérieurs à ceux qui sont initialisés en tant qu’applications au niveau du système.</span><span class="sxs-lookup"><span data-stu-id="bcc39-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="bcc39-108">Voir aussi [*niveau application*](vssgloss-a.md), [*applications de niveau frontal*](vssgloss-f.md), [*applications système*](vssgloss-s.md), [*enregistreur*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="bcc39-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc39-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Événement BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="bcc39-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="bcc39-110">Événement VSS indiquant qu’une sauvegarde VSS est terminée.</span><span class="sxs-lookup"><span data-stu-id="bcc39-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="bcc39-111">Cet événement doit être suivi d’un événement BackupShutdown en fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="bcc39-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="bcc39-112">Voir aussi *événement BackupShutdown*.</span><span class="sxs-lookup"><span data-stu-id="bcc39-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="bcc39-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Document sur les composants de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="bcc39-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="bcc39-114">Document XML créé par un demandeur (à l’aide de l’interface **IVssBackupComponents** ) au cours de la configuration d’une opération de restauration ou de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="bcc39-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="bcc39-115">Le document des composants de la sauvegarde contient une liste des composants explicitement inclus, provenant d’un ou de plusieurs enregistreurs, qui participent à une opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="bcc39-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="bcc39-116">Il ne contient pas d’informations sur les composants inclus implicitement.</span><span class="sxs-lookup"><span data-stu-id="bcc39-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="bcc39-117">En revanche, un document des métadonnées de l’enregistreur contient seulement des composants d’enregistreur qui peuvent participer à une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="bcc39-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="bcc39-118">Un document de composants de sauvegarde peut être enregistré sur le disque.</span><span class="sxs-lookup"><span data-stu-id="bcc39-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="bcc39-119">Voir aussi [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="bcc39-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc39-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**jeu de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="bcc39-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="bcc39-121">Fichiers à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="bcc39-121">Those files to be backed up.</span></span> <span data-ttu-id="bcc39-122">Il inclut les fichiers sélectionnés par inclusion dans un composant, ceux indiqués par les instructions include au niveau de l’enregistreur, moins les fichiers qui ont été explicitement inclus.</span><span class="sxs-lookup"><span data-stu-id="bcc39-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="bcc39-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Événement BackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="bcc39-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="bcc39-124">Événement VSS indiquant qu’une application de sauvegarde conforme s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="bcc39-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="bcc39-125">Normalement, il est précédé d’un événement BackupComplete.</span><span class="sxs-lookup"><span data-stu-id="bcc39-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="bcc39-126">Toutefois, si une sauvegarde se termine de manière inattendue, cet événement peut être généré sans événement BackupComplete précédent.</span><span class="sxs-lookup"><span data-stu-id="bcc39-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="bcc39-127">Voir aussi *événement BackupComplete*.</span><span class="sxs-lookup"><span data-stu-id="bcc39-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="bcc39-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**tampon de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="bcc39-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="bcc39-129">Chaîne contenant les informations relatives au moment où une sauvegarde a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="bcc39-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="bcc39-130">VSS n’impose aucune restriction sur le format de cette chaîne, à ceci près qu’il est intelligible pour toutes les instances d’écriture d’une classe donnée.</span><span class="sxs-lookup"><span data-stu-id="bcc39-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="bcc39-131">Il peut contenir des informations de date et d’heure, des numéros de séquence logique ou toute autre information qui permettra à un rédacteur de la même classe de déterminer à quel moment la dernière sauvegarde a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="bcc39-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



