---
description: Lors du traitement d’une sauvegarde sous VSS, les demandeurs et les Writers ont collaboré pour produire une image système stable à partir de laquelle sauvegarder des données, ce qui nécessitait une coordination et la création d’un cliché instantané du système actuel.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Vue d’ensemble du traitement d’une restauration sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529784"
---
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="4d48f-103">Vue d’ensemble du traitement d’une restauration sous VSS</span><span class="sxs-lookup"><span data-stu-id="4d48f-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="4d48f-104">Lors du traitement d’une sauvegarde sous VSS, les demandeurs et les Writers ont collaboré pour produire une image système stable à partir de laquelle sauvegarder des données, ce qui nécessitait une coordination et la création d’un cliché instantané du système actuel.</span><span class="sxs-lookup"><span data-stu-id="4d48f-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="4d48f-105">Contrairement à une sauvegarde VSS, où l’objectif de la coordination des demandeurs et des Writers consiste à produire une image système stable à partir de laquelle copier des données, l’objectif d’une restauration basée sur VSS est de renvoyer des fichiers sur le disque de la manière la plus utile aux applications (Writers) en cours d’exécution sur le système.</span><span class="sxs-lookup"><span data-stu-id="4d48f-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="4d48f-106">Cela ne nécessite pas une image système stable, donc aucun cliché instantané n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4d48f-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="4d48f-107">Au lieu de cela, l’attention est axée sur l’évitement de l’interruption de l’activité de l’enregistreur, ce qui empêche la création de jeux de données incohérents sur le disque et permet aux rédacteurs d’évaluer et de fusionner les données si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4d48f-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="4d48f-108">À l’instar d’une opération de sauvegarde, une restauration VSS requiert l’accès à un document de composants de sauvegarde et à des documents de métadonnées d’écriture.</span><span class="sxs-lookup"><span data-stu-id="4d48f-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="4d48f-109">Ces documents ne sont généralement pas obtenus en interrogeant des applications en cours d’exécution, mais ils sont récupérés à partir de versions stockées en tant que documents XML sur un support de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="4d48f-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="4d48f-110">Comme c’est le cas pendant les opérations de sauvegarde, les documents de métadonnées de l’enregistreur restent des objets en lecture seule et (une fois récupérés) le document des composants de sauvegarde peut encore être modifié.</span><span class="sxs-lookup"><span data-stu-id="4d48f-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="4d48f-111">Les modifications apportées au document composants de sauvegarde permettent aux rédacteurs et aux demandeurs de communiquer sur les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4d48f-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="4d48f-112">Substitution des [*méthodes de restauration*](vssgloss-r.md) avec les [*cibles de restauration*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="4d48f-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="4d48f-113">Utilisation de [ *mappages d’emplacements secondaires*](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="4d48f-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="4d48f-114">Restauration des fichiers vers les nouveaux emplacements sur le disque</span><span class="sxs-lookup"><span data-stu-id="4d48f-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="4d48f-115">Utilisation de différentes règles de sélection de celles utilisées lors de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="4d48f-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="4d48f-116">Pour mieux comprendre les tâches de base impliquées dans la réalisation d’une restauration, il est utile de décomposer cette vue d’ensemble selon les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d48f-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="4d48f-117">Vue d’ensemble de l’initialisation de la restauration</span><span class="sxs-lookup"><span data-stu-id="4d48f-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="4d48f-118">Vue d’ensemble de la préparation pour la restauration</span><span class="sxs-lookup"><span data-stu-id="4d48f-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="4d48f-119">Vue d’ensemble de la restauration réelle des fichiers</span><span class="sxs-lookup"><span data-stu-id="4d48f-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="4d48f-120">Vue d’ensemble du nettoyage et de l’arrêt de la restauration</span><span class="sxs-lookup"><span data-stu-id="4d48f-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



