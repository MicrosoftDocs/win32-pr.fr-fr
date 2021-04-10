---
description: COMREPL est un utilitaire qui réplique le catalogue COM+ d’un ordinateur source donné sur un ou plusieurs ordinateurs cibles.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: L’utilitaire de réplication COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950779"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="93022-103">L’utilitaire de réplication COMREPL</span><span class="sxs-lookup"><span data-stu-id="93022-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="93022-104">COMREPL est un utilitaire qui réplique le catalogue COM+ d’un ordinateur source donné sur un ou plusieurs ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="93022-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="93022-105">Pensez à l’ordinateur source qui représente une « configuration principale ».</span><span class="sxs-lookup"><span data-stu-id="93022-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="93022-106">COMREPL est utilisé pour répliquer cette configuration principale afin de conserver un ensemble d’ordinateurs configurés de façon identique.</span><span class="sxs-lookup"><span data-stu-id="93022-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="93022-107">L’unité de réplication est l’ensemble de la configuration COM+ sur l’ordinateur maître.</span><span class="sxs-lookup"><span data-stu-id="93022-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="93022-108">Toutes les applications COM+ sur le serveur maître sont répliquées sur les ordinateurs cibles. C’est tout ou rien.</span><span class="sxs-lookup"><span data-stu-id="93022-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="93022-109">En outre, toutes les applications COM+ précédemment installées sur les ordinateurs cibles, à l’exception des applications COM+ préinstallées, seront supprimées dans le cadre du processus de réplication.</span><span class="sxs-lookup"><span data-stu-id="93022-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="93022-110">COMREPL réplique uniquement les données de configuration COM+.</span><span class="sxs-lookup"><span data-stu-id="93022-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="93022-111">Cela comprend les applications COM+ et les paramètres d’ordinateur spécifiques à COM+.</span><span class="sxs-lookup"><span data-stu-id="93022-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="93022-112">Microsoft Internet Information Services (IIS) a un utilitaire similaire (IISSync), qui utilise COMREPL pour répliquer la configuration IIS et COM+.</span><span class="sxs-lookup"><span data-stu-id="93022-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="93022-113">Pour plus d’informations sur le lancement et l’utilisation de COMREPL, consultez les rubriques suivantes dans cette section :</span><span class="sxs-lookup"><span data-stu-id="93022-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="93022-114">Utilisation de COMREPL</span><span class="sxs-lookup"><span data-stu-id="93022-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="93022-115">Ce qui est répliqué</span><span class="sxs-lookup"><span data-stu-id="93022-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="93022-116">Phases de réplication</span><span class="sxs-lookup"><span data-stu-id="93022-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="93022-117">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="93022-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="93022-118">Journalisation et rapports d’erreurs</span><span class="sxs-lookup"><span data-stu-id="93022-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="93022-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93022-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93022-120">Création de packages d’installation pour les applications COM+</span><span class="sxs-lookup"><span data-stu-id="93022-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="93022-121">Déploiement de proxys d’application</span><span class="sxs-lookup"><span data-stu-id="93022-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="93022-122">Le catalogue COM+</span><span class="sxs-lookup"><span data-stu-id="93022-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



