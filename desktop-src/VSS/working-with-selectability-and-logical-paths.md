---
description: La participation d’un enregistreur dans le cadre d’une opération de sauvegarde ou de restauration, et laquelle de ses données sont enregistrées, dépend des composants qui sont explicitement inclus dans le document des composants de sauvegarde d’un demandeur et de la relation entre ces composants et du chemin logique des autres composants dans le document de métadonnées du writer.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Utilisation de la sélectivité et des chemins logiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533599"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="a4568-103">Utilisation de la sélectivité et des chemins logiques</span><span class="sxs-lookup"><span data-stu-id="a4568-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="a4568-104">La participation d’un enregistreur dans le cadre d’une opération de sauvegarde ou de restauration, et laquelle de ses données sont enregistrées, dépend des composants qui sont [*explicitement inclus*](vssgloss-e.md) dans le document des composants de sauvegarde d’un demandeur et de la relation entre ces composants et du chemin logique des autres composants dans le document de métadonnées du writer.</span><span class="sxs-lookup"><span data-stu-id="a4568-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="a4568-105">Les enregistreurs sans composants ajoutés au document du composant de sauvegarde d’un demandeur avant la génération d’un événement [*PrepareForBackup*](vssgloss-p.md) (dans le cas d’opérations de sauvegarde) ou d’un événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (dans le cas d’opérations de restauration) ne reçoivent aucun événement après ce point et ne participent pas à l’opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="a4568-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="a4568-106">Toutefois, la liberté d’un demandeur d’inclure ou d’exclure un composant donné dans une sauvegarde ou une restauration est régie par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a4568-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="a4568-107">Toute hiérarchie qui existe entre les composants gérés par un enregistreur et exprimée par des [ *chemins logiques*](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="a4568-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="a4568-108">Si le composant est désigné comme étant [ *sélectionnable pour la sauvegarde*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="a4568-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="a4568-109">Indique s’il est désigné comme [ *sélectionnable pour la restauration*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="a4568-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="a4568-110">Indique s’il existe une dépendance explicite entre un composant donné dans un writer donné et d’autres composants dans d’autres enregistreurs</span><span class="sxs-lookup"><span data-stu-id="a4568-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="a4568-111">Vous trouverez plus d’informations sur ces problèmes dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4568-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="a4568-112">Chemin logique des composants</span><span class="sxs-lookup"><span data-stu-id="a4568-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="a4568-113">Utilisation de la sélectivité pour la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="a4568-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="a4568-114">Utilisation de la sélectivité pour la restauration et les sous-composants</span><span class="sxs-lookup"><span data-stu-id="a4568-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="a4568-115">Sélection et utilisation des propriétés de composant</span><span class="sxs-lookup"><span data-stu-id="a4568-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="a4568-116">Dépendances entre les composants gérés par différents Writers</span><span class="sxs-lookup"><span data-stu-id="a4568-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



