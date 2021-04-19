---
description: COMREPL fait son travail en trois phases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Phases de réplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515378"
---
# <a name="replication-phases"></a><span data-ttu-id="be968-103">Phases de réplication</span><span class="sxs-lookup"><span data-stu-id="be968-103">Replication Phases</span></span>

<span data-ttu-id="be968-104">COMREPL fait son travail en trois phases.</span><span class="sxs-lookup"><span data-stu-id="be968-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="be968-105">Le processus de réplication est divisé en différentes phases pour les deux raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="be968-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="be968-106">Pour séparer le travail effectué afin de préparer la source à partir du travail effectué sur chaque cible</span><span class="sxs-lookup"><span data-stu-id="be968-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="be968-107">Pour retarder la modification de la cible jusqu’à ce que toutes les données soient acquises à partir de la source</span><span class="sxs-lookup"><span data-stu-id="be968-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="be968-108">Les phases de réplication sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="be968-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="be968-109">Phase</span><span class="sxs-lookup"><span data-stu-id="be968-109">Phase</span></span>         | <span data-ttu-id="be968-110">Description</span><span class="sxs-lookup"><span data-stu-id="be968-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be968-111">Phase de préparation</span><span class="sxs-lookup"><span data-stu-id="be968-111">Prepare phase</span></span> | <span data-ttu-id="be968-112">Exporte toutes les applications installées localement sur l’ordinateur source.</span><span class="sxs-lookup"><span data-stu-id="be968-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="be968-113">Cette phase ne touche pas la configuration des cibles.</span><span class="sxs-lookup"><span data-stu-id="be968-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="be968-114">Phase de copie</span><span class="sxs-lookup"><span data-stu-id="be968-114">Copy phase</span></span>    | <span data-ttu-id="be968-115">Copie des données sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="be968-115">Copies data to a target computer.</span></span> <span data-ttu-id="be968-116">Toutes les applications exportées sur la source sont copiées vers la cible.</span><span class="sxs-lookup"><span data-stu-id="be968-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="be968-117">Il s’agit d’une opération de copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="be968-117">This is a file copy operation.</span></span> <span data-ttu-id="be968-118">(Voir [gestion des fichiers](file-management.md).) Cette étape obtient également des données de l’ordinateur source qui ne sont pas encapsulées dans des fichiers d’application exportés (par exemple, les identités d’application).</span><span class="sxs-lookup"><span data-stu-id="be968-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="be968-119">Ces données sont conservées en mémoire dans COMREPL.</span><span class="sxs-lookup"><span data-stu-id="be968-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="be968-120">Cette phase ne touche pas la configuration des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="be968-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="be968-121">Phase d’installation</span><span class="sxs-lookup"><span data-stu-id="be968-121">Install phase</span></span> | <span data-ttu-id="be968-122">Installe le catalogue source sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="be968-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="be968-123">Lorsque cette étape est lancée, toutes les données nécessaires à la reconfiguration de la cible se trouvent dans les fichiers d’application dans le système de fichiers de la cible ou sont conservées en tant que données d’instance dans COMREPL.</span><span class="sxs-lookup"><span data-stu-id="be968-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="be968-124">Cette phase va entraîner la suppression de toutes les applications installées sur la cible (à l’exception des applications décrites dans [ce qui est répliqué](what-gets-replicated.md)) avant l’installation des applications copiées à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="be968-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="be968-125">COMREPL s’installe simultanément sur plusieurs cibles à l’aide d’un thread d’installation par cible.</span><span class="sxs-lookup"><span data-stu-id="be968-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="be968-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be968-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be968-127">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="be968-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="be968-128">Journalisation et rapports d’erreurs</span><span class="sxs-lookup"><span data-stu-id="be968-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="be968-129">Utilisation de COMREPL</span><span class="sxs-lookup"><span data-stu-id="be968-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="be968-130">Ce qui est répliqué</span><span class="sxs-lookup"><span data-stu-id="be968-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



