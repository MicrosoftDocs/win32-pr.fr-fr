---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516254"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="93574-103">E (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="93574-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="93574-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) e [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="93574-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="93574-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusion explicite de composant**</span><span class="sxs-lookup"><span data-stu-id="93574-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="93574-106">Ajout des informations d’un composant au document des composants de sauvegarde d’un demandeur lorsqu’il participe à une opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="93574-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="93574-107">Les demandeurs utilisent [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour inclure explicitement un composant dans une opération de sauvegarde, et [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) ou [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) pour inclure explicitement un composant dans une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="93574-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="93574-108">Si un composant d’un enregistreur est sauvegardé ou restauré, tous les composants non sélectionnables sans ancêtres sélectionnables doivent être inclus explicitement dans une opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="93574-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="93574-109">Les composants sélectionnables sans les ancêtres sélectionnables choisis par un demandeur pour la participation à une sauvegarde ou une restauration doivent être inclus explicitement dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="93574-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="93574-110">Les composants non sélectionnables avec un ancêtre sélectionnable ne sont jamais explicitement inclus.</span><span class="sxs-lookup"><span data-stu-id="93574-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="93574-111">Les composants sélectionnables avec un ancêtre sélectionnable peuvent être inclus de manière explicite, ou peuvent être inclus implicitement si l’ancêtre est inclus explicitement.</span><span class="sxs-lookup"><span data-stu-id="93574-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="93574-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**clichés instantanés exposés**</span><span class="sxs-lookup"><span data-stu-id="93574-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="93574-113">Cliché instantané de volume monté sur un système et disponible pour les processus autres que celui qui le gère.</span><span class="sxs-lookup"><span data-stu-id="93574-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="93574-114">Un volume de clichés instantanés monté sous une lettre de lecteur ou un emplacement de répertoire est appelé « localement exposé ».</span><span class="sxs-lookup"><span data-stu-id="93574-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="93574-115">Un volume de clichés instantanés accessible via un partage (à l’exception des clichés instantanés accessibles aux clients) est appelé « exposé à distance ».</span><span class="sxs-lookup"><span data-stu-id="93574-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="93574-116">Tous les clichés instantanés exposés sont également des clichés instantanés en surface.</span><span class="sxs-lookup"><span data-stu-id="93574-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="93574-117">Voir aussi cliché [*instantané accessible*](vssgloss-c.md)par le client, cliché [*instantané*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="93574-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



