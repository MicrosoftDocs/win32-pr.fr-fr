---
description: Les clichés instantanés transportables peuvent être utilisés pour faciliter une récupération rapide.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Récupération rapide à l’aide de volumes de clichés instantanés transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524697"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="32c55-103">Récupération rapide à l’aide de volumes de clichés instantanés transportables</span><span class="sxs-lookup"><span data-stu-id="32c55-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="32c55-104">Les [*clichés instantanés transportables*](vssgloss-t.md) peuvent être utilisés pour faciliter une *récupération rapide*.</span><span class="sxs-lookup"><span data-stu-id="32c55-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="32c55-105">La récupération rapide peut être utilisée pour revenir rapidement à un cliché instantané antérieur.</span><span class="sxs-lookup"><span data-stu-id="32c55-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="32c55-106">Les étapes impliquées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32c55-106">The steps involved are:</span></span>

1.  <span data-ttu-id="32c55-107">Créez le cliché instantané transportable des numéros d’unités logiques appropriés.</span><span class="sxs-lookup"><span data-stu-id="32c55-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="32c55-108">Le cliché instantané peut être [*persistant*](vssgloss-p.md) ou non persistant.</span><span class="sxs-lookup"><span data-stu-id="32c55-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="32c55-109">Supprimer les numéros d’unités logiques d’origine</span><span class="sxs-lookup"><span data-stu-id="32c55-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="32c55-110">Si l’ordinateur est à l’intérieur d’un cluster, marquez les ressources de disque affectées comme étant hors connexion ou activez le [mode de maintenance](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) pour ces ressources de disque.</span><span class="sxs-lookup"><span data-stu-id="32c55-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="32c55-111">Masquez les numéros d’unités logiques affectés à partir de cet ordinateur (et de tous les autres nœuds si l’ordinateur se trouve dans un cluster).</span><span class="sxs-lookup"><span data-stu-id="32c55-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="32c55-112">Importez le cliché instantané à l’aide de la méthode [**IVssBackupComponents :: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .</span><span class="sxs-lookup"><span data-stu-id="32c55-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="32c55-113">Rompez le cliché instantané à l’aide de la méthode [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="32c55-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="32c55-114">Marquez les nouveaux volumes de clichés instantanés comme étant en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="32c55-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="32c55-115">Si l’ordinateur se trouve dans un cluster, exposez les nouveaux numéros d’unités logiques de clichés instantanés en tant que LUN d’origine.</span><span class="sxs-lookup"><span data-stu-id="32c55-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="32c55-116">Démasquez les numéros d’unité logique de cliché instantané aux autres nœuds du cluster.</span><span class="sxs-lookup"><span data-stu-id="32c55-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="32c55-117">Marquez les ressources qui étaient précédemment marquées comme étant en ligne ou désactivez le mode de maintenance pour ces ressources de disque.</span><span class="sxs-lookup"><span data-stu-id="32c55-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="32c55-118">Les clichés instantanés transportables dans un cluster ne sont pas pris en charge avant Windows Server 2003 avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="32c55-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="32c55-119">Cela est uniquement pris en charge avec les numéros d’unités logiques conformes, qui ont au moins une page VPD (SCSI vital Product Data) 0x83 \_ l’identificateur de stockage de type 1, 2 ou 8, et l’Association 0, et les numéros d’unités logiques doivent gérer un disque de base avec le partitionnement MBR.</span><span class="sxs-lookup"><span data-stu-id="32c55-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
