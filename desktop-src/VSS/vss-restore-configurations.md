---
description: La restauration de fichiers sur un système en cours d’exécution peut être problématique. Il est important que les applications en cours d’exécution (Writers) indiquent ce qu’il faut faire lorsque des problèmes surviennent pendant les restaurations, par exemple, si le fichier en cours de restauration est en cours d’utilisation.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurations de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113178"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="e01e4-104">Configurations de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="e01e4-104">VSS Restore Configurations</span></span>

<span data-ttu-id="e01e4-105">La restauration de fichiers sur un système en cours d’exécution peut être problématique.</span><span class="sxs-lookup"><span data-stu-id="e01e4-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="e01e4-106">Il est important que les applications en cours d’exécution (Writers) indiquent ce qu’il faut faire lorsque des problèmes surviennent pendant les restaurations, par exemple, si le fichier en cours de restauration est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e01e4-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="e01e4-107">Sous VSS, les rédacteurs disposent de deux méthodes complémentaires pour gérer les restaurations : les [*méthodes de restauration*](vssgloss-r.md) et les [*cibles de restauration*](vssgloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="e01e4-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="e01e4-108">En outre, les demandeurs peuvent choisir de restaurer les fichiers aux emplacements précédemment non spécifiés et de notifier les enregistreurs (voir [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span><span class="sxs-lookup"><span data-stu-id="e01e4-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="e01e4-109">La méthode Restore (également appelée cible de restauration d’origine) est spécifiée par un enregistreur à l’heure de la sauvegarde et définit une définition à l’aide de l’enregistreur de la méthode à utiliser pour restaurer tous ses composants à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e01e4-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="e01e4-110">Tous les fichiers et les composants gérés par un enregistreur partagent la même méthode de restauration.</span><span class="sxs-lookup"><span data-stu-id="e01e4-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="e01e4-111">Les cibles de restauration permettent aux rédacteurs de modifier le mode de restauration des composants spécifiques au moment de la restauration.</span><span class="sxs-lookup"><span data-stu-id="e01e4-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="e01e4-112">Contrairement aux méthodes de restauration, les cibles de restauration sont définies pour un jeu de composants.</span><span class="sxs-lookup"><span data-stu-id="e01e4-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="e01e4-113">Une présentation détaillée de l’utilisation des méthodes de restauration et des cibles de restauration se trouve dans les rubriques ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e01e4-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="e01e4-114">État de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="e01e4-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="e01e4-115">Définition des méthodes de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="e01e4-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="e01e4-116">Définition des cibles de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="e01e4-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="e01e4-117">Définition des options de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="e01e4-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="e01e4-118">(Pour plus d’informations sur les restaurations qui n’utilisent pas ces mécanismes, consultez [restaurations sans participation au rédacteur](restores-without-writer-participation.md).)</span><span class="sxs-lookup"><span data-stu-id="e01e4-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



