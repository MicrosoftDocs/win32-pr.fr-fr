---
description: Les fonctions suivantes sont utilisées avec les files d’attente de fichiers.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Fonctions de file d’attente de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521052"
---
# <a name="file-queue-functions"></a><span data-ttu-id="90492-103">Fonctions de file d’attente de fichiers</span><span class="sxs-lookup"><span data-stu-id="90492-103">File Queue Functions</span></span>

<span data-ttu-id="90492-104">Les fonctions suivantes sont utilisées avec les files d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="90492-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="90492-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="90492-105">Function</span></span>                                                             | <span data-ttu-id="90492-106">Description</span><span class="sxs-lookup"><span data-stu-id="90492-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90492-107">**SetupCloseFileQueue**</span><span class="sxs-lookup"><span data-stu-id="90492-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="90492-108">Met fin à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="90492-108">Terminates the queue.</span></span> <span data-ttu-id="90492-109">Les transactions restantes ne sont pas validées.</span><span class="sxs-lookup"><span data-stu-id="90492-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="90492-110">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="90492-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="90492-111">Valide toutes les transactions mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="90492-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="90492-112">**SetupOpenFileQueue**</span><span class="sxs-lookup"><span data-stu-id="90492-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="90492-113">Initialise et retourne un handle vers la file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="90492-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="90492-114">**SetupPromptReboot**</span><span class="sxs-lookup"><span data-stu-id="90492-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="90492-115">Invite l’utilisateur à redémarrer son ordinateur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="90492-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="90492-116">**SetupQueueCopy**</span><span class="sxs-lookup"><span data-stu-id="90492-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="90492-117">Met en file d’attente une copie de fichier.</span><span class="sxs-lookup"><span data-stu-id="90492-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="90492-118">**SetupQueueCopySection**</span><span class="sxs-lookup"><span data-stu-id="90492-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="90492-119">Met en file d’attente les fichiers dans une section de fichiers de copie INF.</span><span class="sxs-lookup"><span data-stu-id="90492-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="90492-120">**SetupQueueDefaultCopy**</span><span class="sxs-lookup"><span data-stu-id="90492-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="90492-121">Met en file d’attente les fichiers dans une section de fichiers de copie INF à l’aide des informations par défaut spécifiées dans un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="90492-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="90492-122">**SetupQueueDelete**</span><span class="sxs-lookup"><span data-stu-id="90492-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="90492-123">Met en file d’attente la suppression d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="90492-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="90492-124">**SetupQueueDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="90492-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="90492-125">Met en file d’attente les fichiers dans un fichier INF supprimer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="90492-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="90492-126">**SetupQueueRename**</span><span class="sxs-lookup"><span data-stu-id="90492-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="90492-127">Met en file d’attente un changement de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="90492-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="90492-128">**SetupQueueRenameSection**</span><span class="sxs-lookup"><span data-stu-id="90492-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="90492-129">Met en file d’attente les fichiers dans une section renommer les fichiers INF.</span><span class="sxs-lookup"><span data-stu-id="90492-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="90492-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="90492-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="90492-131">Analyse la file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="90492-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="90492-132">**SetupSetPlatformPathOverride**</span><span class="sxs-lookup"><span data-stu-id="90492-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="90492-133">Définit la substitution du chemin d’accès de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="90492-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



