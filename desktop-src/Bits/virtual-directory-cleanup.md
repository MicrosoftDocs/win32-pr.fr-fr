---
title: Nettoyage de répertoire virtuel
description: BITS étend les répertoires virtuels IIS pour prendre en charge les téléchargements.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941159"
---
# <a name="virtual-directory-cleanup"></a><span data-ttu-id="fb3fa-103">Nettoyage de répertoire virtuel</span><span class="sxs-lookup"><span data-stu-id="fb3fa-103">Virtual Directory Cleanup</span></span>

<span data-ttu-id="fb3fa-104">BITS étend les répertoires virtuels IIS pour prendre en charge les téléchargements.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-104">BITS extends IIS virtual directories to support uploads.</span></span> <span data-ttu-id="fb3fa-105">Chaque répertoire virtuel a une propriété de délai d’expiration de session (la propriété de métabase IIS [BITSSessionTimeout](bits-iis-extension-properties.md) ) qui spécifie la période pendant laquelle le client bits doit progresser dans le téléchargement du fichier.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-105">Each virtual directory has a session time-out property (the IIS [BITSSessionTimeout](bits-iis-extension-properties.md) metabase property) that specifies the period of time in which the BITS client must make progress in uploading the file.</span></span> <span data-ttu-id="fb3fa-106">Si aucune progression n’est effectuée pendant cette période (la minuterie est réinitialisée lorsque la progression est effectuée), le service BITS ferme la session.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-106">If no progress is made during that period (the timer is reset when progress is made), BITS closes the session.</span></span> <span data-ttu-id="fb3fa-107">Le délai d’expiration de session par défaut est de 14 jours.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-107">The default session time-out is 14 days.</span></span>

<span data-ttu-id="fb3fa-108">BITS ajoute un élément de travail au [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page) pour chaque répertoire virtuel que vous créez et activez.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-108">BITS adds a work item to the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) for each virtual directory you create and enable.</span></span> <span data-ttu-id="fb3fa-109">L’élément de travail supprime les ressources associées aux sessions fermées.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-109">The work item deletes resources associated with the closed sessions.</span></span> <span data-ttu-id="fb3fa-110">Par défaut, le nettoyage se produit toutes les 12 heures.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-110">By default, the cleanup occurs every 12 hours.</span></span> <span data-ttu-id="fb3fa-111">Si deux répertoires virtuels pointent vers le même répertoire physique, le processus de nettoyage initié par l’un des répertoires supprime les ressources associées à toutes les sessions fermées dans le répertoire physique.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-111">If two virtual directories point to the same physical directory, the cleanup process initiated by one of the directories deletes the resources associated with all closed sessions in the physical directory.</span></span>

<span data-ttu-id="fb3fa-112">Utilisez l’onglet extension BITS ou les interfaces [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page) pour modifier la planification de nettoyage en fonction de votre application.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-112">Use the BITS Extension tab or the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) interfaces to change the cleanup schedule as appropriate for your application.</span></span> <span data-ttu-id="fb3fa-113">Vous pouvez également appeler la méthode [**IBITSExtensionSetup :: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) pour récupérer un pointeur d’interface vers la tâche de nettoyage associée au répertoire virtuel.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-113">You can also call the [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) method to retrieve an interface pointer to the cleanup task associated with the virtual directory.</span></span>

> [!Note]  
> <span data-ttu-id="fb3fa-114">Si le Planificateur de tâches est désactivé une fois que le répertoire virtuel est activé, le processus de nettoyage du répertoire virtuel ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-114">If the Task Scheduler is disabled after the virtual directory is enabled, the virtual directory cleanup process will not work.</span></span>

 

 

 