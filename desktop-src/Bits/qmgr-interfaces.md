---
title: Interfaces QMGR
description: Utilisez les interfaces du gestionnaire de files d’attente (QMGR) suivantes pour télécharger des fichiers et surveiller des travaux dans la file d’attente de téléchargement.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190797"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="56af2-103">Interfaces QMGR</span><span class="sxs-lookup"><span data-stu-id="56af2-103">QMGR Interfaces</span></span>

<span data-ttu-id="56af2-104">\[Les interfaces du gestionnaire de files d’attente (QMGR) peuvent être utilisées dans les systèmes d’exploitation spécifiés dans la section Configuration requise de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="56af2-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="56af2-105">Il est possible qu’ils soient modifiés ou indisponibles dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="56af2-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="56af2-106">Utilisez plutôt les [interfaces bits](bits-interfaces.md).\]</span><span class="sxs-lookup"><span data-stu-id="56af2-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="56af2-107">Utilisez les interfaces du gestionnaire de files d’attente (QMGR) suivantes pour télécharger des fichiers et surveiller des travaux dans la file d’attente de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="56af2-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="56af2-108">Interface</span><span class="sxs-lookup"><span data-stu-id="56af2-108">Interface</span></span>                                                                 | <span data-ttu-id="56af2-109">Description</span><span class="sxs-lookup"><span data-stu-id="56af2-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56af2-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="56af2-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="56af2-111">Implémentez pour recevoir une notification lorsque des événements se produisent.</span><span class="sxs-lookup"><span data-stu-id="56af2-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="56af2-112">**IBackgroundCopyGroup**</span><span class="sxs-lookup"><span data-stu-id="56af2-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="56af2-113">Utilisez pour gérer le groupe.</span><span class="sxs-lookup"><span data-stu-id="56af2-113">Use to manage the group.</span></span> <span data-ttu-id="56af2-114">Par exemple, ajoutez un travail au groupe, définissez les propriétés du groupe et démarrez et arrêtez le groupe dans la file d’attente de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="56af2-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="56af2-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="56af2-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="56af2-116">Utilisez pour ajouter des fichiers au travail et pour récupérer l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="56af2-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="56af2-117">**IBackgroundCopyQMgr**</span><span class="sxs-lookup"><span data-stu-id="56af2-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="56af2-118">Utilisez pour créer un nouveau groupe, récupérer un groupe existant ou énumérer tous les groupes de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="56af2-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="56af2-119">**IEnumBackgroundCopyGroups**</span><span class="sxs-lookup"><span data-stu-id="56af2-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="56af2-120">Utilisez pour récupérer une liste de groupes dans la file d’attente de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="56af2-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="56af2-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="56af2-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="56af2-122">Utilisez pour récupérer une liste de travaux dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="56af2-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





