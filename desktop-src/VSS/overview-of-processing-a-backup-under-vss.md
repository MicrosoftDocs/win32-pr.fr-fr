---
description: Lors du traitement d’une sauvegarde, le demandeur et les rédacteurs coordonnent la mise en place d’une image système stable à partir de laquelle sauvegarder des données (le volume des clichés instantanés), pour regrouper des fichiers en fonction de leur utilisation et pour stocker des informations sur les données enregistrées.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Vue d’ensemble du traitement d’une sauvegarde sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318985"
---
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="e4484-103">Vue d’ensemble du traitement d’une sauvegarde sous VSS</span><span class="sxs-lookup"><span data-stu-id="e4484-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="e4484-104">Lors du traitement d’une sauvegarde, le demandeur et les rédacteurs coordonnent la mise en place d’une image système stable à partir de laquelle sauvegarder des données (le volume des clichés instantanés), pour regrouper des fichiers en fonction de leur utilisation et pour stocker des informations sur les données enregistrées.</span><span class="sxs-lookup"><span data-stu-id="e4484-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="e4484-105">Cela doit être effectué lors de la création d’une interruption minimale du workflow de travail normal de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="e4484-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="e4484-106">Un demandeur interroge les enregistreurs pour ses métadonnées, traite ces données, notifie les enregistreurs avant le début du cliché instantané et des opérations de sauvegarde, puis notifie à nouveau les Writers après la fin des opérations de sauvegarde et de cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="e4484-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="e4484-107">En réponse à ces notifications, le writer fournit des informations sur les fichiers à sauvegarder, y compris la spécification de groupes de fichiers à coordonner ([*composants*](vssgloss-c.md)) — interrompt les opérations d’e/s avant le cliché instantané, puis revient au fonctionnement normal après l’achèvement d’un cliché instantané ou à la fin de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="e4484-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="e4484-108">Au cours du traitement de la sauvegarde, un enregistreur spécifie les fichiers dont il est responsable par le biais de ses métadonnées en lecture seule : le document de métadonnées de l’enregistreur (voir [métadonnées VSS : utilisation du document de métadonnées de l’enregistreur](working-with-the-writer-metadata-document.md)).</span><span class="sxs-lookup"><span data-stu-id="e4484-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="e4484-109">Le demandeur interprète ensuite ces métadonnées, choisit les éléments à sauvegarder et stocke ces décisions dans son propre objet de métadonnées, le document sur les composants de sauvegarde (voir [métadonnées VSS : utilisation du document sur les composants de sauvegarde](working-with-the-backup-components-document.md)).</span><span class="sxs-lookup"><span data-stu-id="e4484-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="e4484-110">Ce document sur les composants de sauvegarde est disponible à des fins d’inspection et de modification du writer au cours des opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="e4484-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="e4484-111">Ce diagramme illustre les interactions entre le demandeur, le service VSS, la prise en charge du noyau VSS, tous les enregistreurs VSS impliqués et tous les fournisseurs de matériel VSS.</span><span class="sxs-lookup"><span data-stu-id="e4484-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![interactions entre le demandeur, les composants de sauvegarde, les rédacteurs et les fournisseurs](images/vssimpl.png)

<span data-ttu-id="e4484-113">Pour mieux comprendre les tâches de base impliquées dans la réalisation d’une sauvegarde, il est utile de décomposer cette vue d’ensemble dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e4484-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="e4484-114">Vue d’ensemble de l’initialisation de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e4484-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="e4484-115">Vue d’ensemble de la phase de découverte de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e4484-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="e4484-116">Vue d’ensemble des tâches de pré-sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e4484-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="e4484-117">Vue d’ensemble de la sauvegarde réelle des fichiers</span><span class="sxs-lookup"><span data-stu-id="e4484-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="e4484-118">Vue d’ensemble de l’arrêt de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="e4484-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



