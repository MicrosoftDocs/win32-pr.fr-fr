---
description: Pour activer le transfert de fichiers d’application, COMREPL gère automatiquement les jeux de dossiers du système de fichiers sur la source et la cible. Ces dossiers COMREPL sont tous enracinés dans \\ la réplication com% systemdir% \\ .
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gestion des fichiers (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523428"
---
# <a name="file-management"></a><span data-ttu-id="9571b-104">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="9571b-104">File Management</span></span>

<span data-ttu-id="9571b-105">Pour activer le transfert de fichiers d’application, COMREPL gère automatiquement les jeux de dossiers du système de fichiers sur la source et la cible.</span><span class="sxs-lookup"><span data-stu-id="9571b-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="9571b-106">Ces dossiers COMREPL sont tous enracinés dans \\ la réplication com% systemdir% \\ .</span><span class="sxs-lookup"><span data-stu-id="9571b-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="9571b-107">Dossiers sources</span><span class="sxs-lookup"><span data-stu-id="9571b-107">Source folders</span></span>



| <span data-ttu-id="9571b-108">Dossier</span><span class="sxs-lookup"><span data-stu-id="9571b-108">Folder</span></span>                   | <span data-ttu-id="9571b-109">Objectif</span><span class="sxs-lookup"><span data-stu-id="9571b-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9571b-110">ReplicaSource</span><span class="sxs-lookup"><span data-stu-id="9571b-110">ReplicaSource</span></span><br/> | <span data-ttu-id="9571b-111">Les applications exportées pendant la phase de préparation sont stockées ici.</span><span class="sxs-lookup"><span data-stu-id="9571b-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="9571b-112">Ce dossier est remplacé chaque fois que la phase de préparation est exécutée sur un ordinateur source donné.</span><span class="sxs-lookup"><span data-stu-id="9571b-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="9571b-113">Ce dossier n’étant jamais explicitement supprimé, la réplication vers des cibles peut avoir lieu à tout moment après la préparation de la source.</span><span class="sxs-lookup"><span data-stu-id="9571b-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="9571b-114">Chaque application est stockée dans son propre sous-dossier nommé <appName> + <appID> .</span><span class="sxs-lookup"><span data-stu-id="9571b-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="9571b-115">Dossiers cibles</span><span class="sxs-lookup"><span data-stu-id="9571b-115">Target folders</span></span>



| <span data-ttu-id="9571b-116">Dossier</span><span class="sxs-lookup"><span data-stu-id="9571b-116">Folder</span></span>                    | <span data-ttu-id="9571b-117">Objectif</span><span class="sxs-lookup"><span data-stu-id="9571b-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9571b-118">ReplicaNew</span><span class="sxs-lookup"><span data-stu-id="9571b-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="9571b-119">La phase de copie copie tous les fichiers et sous-dossiers de ReplicaSource sur la source vers ReplicaNew sur la cible.</span><span class="sxs-lookup"><span data-stu-id="9571b-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="9571b-120">Tout contenu précédent de ReplicaNew est supprimé chaque fois que la phase de copie est exécutée sur une cible donnée.</span><span class="sxs-lookup"><span data-stu-id="9571b-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="9571b-121">Ce dossier existe uniquement pendant l’exécution du processus de réplication.</span><span class="sxs-lookup"><span data-stu-id="9571b-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="9571b-122">(Voir ReplicaCurrent.)</span><span class="sxs-lookup"><span data-stu-id="9571b-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="9571b-123">ReplicaCurrent</span><span class="sxs-lookup"><span data-stu-id="9571b-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="9571b-124">Les applications répliquées actuellement installées sur la cible sont stockées ici.</span><span class="sxs-lookup"><span data-stu-id="9571b-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="9571b-125">Lorsque la phase d’installation est démarrée, le dossier ReplicaNew est renommé en ReplicaCurrent.</span><span class="sxs-lookup"><span data-stu-id="9571b-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="9571b-126">S’il existe déjà un dossier ReplicaCurrent, il est renommé en ReplicaOld.</span><span class="sxs-lookup"><span data-stu-id="9571b-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="9571b-127">S’il existe déjà un dossier ReplicaOld, son contenu est supprimé.</span><span class="sxs-lookup"><span data-stu-id="9571b-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="9571b-128">ReplicaOld</span><span class="sxs-lookup"><span data-stu-id="9571b-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="9571b-129">Enregistre les fichiers d’application installés lors de la prochaine réplication.</span><span class="sxs-lookup"><span data-stu-id="9571b-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="9571b-130">Ces fichiers sont enregistrés à des fins de sauvegarde uniquement.</span><span class="sxs-lookup"><span data-stu-id="9571b-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="9571b-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9571b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9571b-132">Journalisation et rapports d’erreurs</span><span class="sxs-lookup"><span data-stu-id="9571b-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="9571b-133">Phases de réplication</span><span class="sxs-lookup"><span data-stu-id="9571b-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="9571b-134">Utilisation de COMREPL</span><span class="sxs-lookup"><span data-stu-id="9571b-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="9571b-135">Ce qui est répliqué</span><span class="sxs-lookup"><span data-stu-id="9571b-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




