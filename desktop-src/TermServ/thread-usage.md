---
title: Utilisation de threads
description: Vous devez ajuster et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509582"
---
# <a name="thread-usage"></a><span data-ttu-id="5cb97-103">Utilisation de threads</span><span class="sxs-lookup"><span data-stu-id="5cb97-103">Thread usage</span></span>

<span data-ttu-id="5cb97-104">Les threads offrent un moyen pratique d’autoriser une application à maximiser son utilisation des ressources du processeur dans un système, en particulier dans une configuration à plusieurs processeurs.</span><span class="sxs-lookup"><span data-stu-id="5cb97-104">Threads provide a convenient way of allowing an application to maximize its usage of CPU resources in a system, especially in a multiple processor configuration.</span></span> <span data-ttu-id="5cb97-105">Dans un environnement Services Bureau à distance, toutefois, plusieurs utilisateurs peuvent exécuter des applications multithread, et tous les threads de tous les utilisateurs sont en concurrence pour les ressources de processeur central de ce système.</span><span class="sxs-lookup"><span data-stu-id="5cb97-105">In a Remote Desktop Services environment, however, multiple users can be running multithreaded applications, and all of the threads for all of the users compete for the central CPU resources of that system.</span></span> <span data-ttu-id="5cb97-106">En tenant compte de cela, vous devez régler et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5cb97-106">With this in mind, you should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span> <span data-ttu-id="5cb97-107">Alors qu’une application multithread mal conçue avec des threads inactifs ou inutilisés peut s’exécuter correctement sur un ordinateur client, la même application peut ne pas s’exécuter correctement sur un serveur Services Bureau à distance multi-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5cb97-107">While a poorly designed multithreaded application with idle or wasted threads might perform adequately on a client computer, the same application might not perform well on a multiuser Remote Desktop Services server.</span></span>

 

 




