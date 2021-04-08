---
description: Utilisation de COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Utilisation de COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748637"
---
# <a name="using-comrepl"></a><span data-ttu-id="19a66-103">Utilisation de COMREPL</span><span class="sxs-lookup"><span data-stu-id="19a66-103">Using COMREPL</span></span>

<span data-ttu-id="19a66-104">Pour lancer l’utilitaire de ligne de commande COMREPL, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="19a66-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="19a66-105">Ajoutez% windir% \\ system32 \\ com au chemin d’accès de l’environnement par défaut en tapant ce qui suit dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="19a66-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="19a66-106">**définir le chemin d’accès =% PATH%;% WINDIR% \\ system32 \\ com**</span><span class="sxs-lookup"><span data-stu-id="19a66-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="19a66-107">Entrez la commande COMREPL suivante :</span><span class="sxs-lookup"><span data-stu-id="19a66-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="19a66-108">**Comrepl** *ordinateursource sera* *targetComputerList* **\[ \[ /n \] /v \]**</span><span class="sxs-lookup"><span data-stu-id="19a66-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="19a66-109">où :</span><span class="sxs-lookup"><span data-stu-id="19a66-109">where:</span></span>

    -   <span data-ttu-id="19a66-110">*ordinateursource sera* est le nom d’ordinateur de la source</span><span class="sxs-lookup"><span data-stu-id="19a66-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="19a66-111">*targetComputerList* est le nom de l’ordinateur des cibles séparées par des espaces</span><span class="sxs-lookup"><span data-stu-id="19a66-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="19a66-112">**/n** supprime l’invite de confirmation avant de démarrer la réplication</span><span class="sxs-lookup"><span data-stu-id="19a66-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="19a66-113">**/v** renvoie la sortie du fichier journal vers la console</span><span class="sxs-lookup"><span data-stu-id="19a66-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="19a66-114">Notes</span><span class="sxs-lookup"><span data-stu-id="19a66-114">Notes</span></span>

-   <span data-ttu-id="19a66-115">Étant donné que COM+ n’est pas répliqué (uniquement les données de configuration et les applications), COM+ doit déjà être installé sur tous les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="19a66-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="19a66-116">L’utilisateur doit passer des vérifications de rôle pour l’application système sur les ordinateurs source et cible.</span><span class="sxs-lookup"><span data-stu-id="19a66-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="19a66-117">Aucun compte d’ordinateur local pouvant être utilisé par des rôles n’est répliqué.</span><span class="sxs-lookup"><span data-stu-id="19a66-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="19a66-118">Le ou les ordinateurs cibles doivent être en ligne.</span><span class="sxs-lookup"><span data-stu-id="19a66-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="19a66-119">L’utilisateur est responsable de la réplication de toutes les données non-COM + (par exemple, les tables de base de données, les fichiers de données, etc.) sur le ou les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="19a66-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="19a66-120">Les clusters peuvent participer à la réplication, mais notez que COMREPL est répliqué uniquement sur les ordinateurs nommés.</span><span class="sxs-lookup"><span data-stu-id="19a66-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19a66-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19a66-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a66-122">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="19a66-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="19a66-123">Journalisation et rapports d’erreurs</span><span class="sxs-lookup"><span data-stu-id="19a66-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="19a66-124">Phases de réplication</span><span class="sxs-lookup"><span data-stu-id="19a66-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="19a66-125">Ce qui est répliqué</span><span class="sxs-lookup"><span data-stu-id="19a66-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



