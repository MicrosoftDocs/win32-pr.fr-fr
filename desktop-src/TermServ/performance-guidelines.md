---
title: Recommandations sur les performances
description: Instructions pour le développement d’applications qui fonctionnent correctement dans un environnement de Services Bureau à distance.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380360"
---
# <a name="performance-guidelines"></a><span data-ttu-id="b25bb-103">Recommandations sur les performances</span><span class="sxs-lookup"><span data-stu-id="b25bb-103">Performance guidelines</span></span>

<span data-ttu-id="b25bb-104">Les sections suivantes fournissent des instructions pour le développement d’applications qui fonctionnent correctement dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b25bb-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b25bb-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b25bb-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b25bb-106">Effets graphiques</span><span class="sxs-lookup"><span data-stu-id="b25bb-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="b25bb-107">Liste des fonctionnalités qui doivent être désactivées lors de l’exécution en tant que session à distance dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b25bb-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b25bb-108">Instructions pour les tâches en arrière-plan dans Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b25bb-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="b25bb-109">Pour optimiser la disponibilité du processeur pour tous les utilisateurs, désactivez les tâches en arrière-plan lors de l’exécution dans un environnement Services Bureau à distance ou créez des tâches en arrière-plan efficaces qui ne nécessitent pas beaucoup de ressources.</span><span class="sxs-lookup"><span data-stu-id="b25bb-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="b25bb-110">Utilisation de threads</span><span class="sxs-lookup"><span data-stu-id="b25bb-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="b25bb-111">Vous devez ajuster et équilibrer l’utilisation des threads d’application pour un environnement multi-utilisateur, multiprocesseur Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b25bb-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="b25bb-112">Détection de l’environnement de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b25bb-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="b25bb-113">Pour optimiser les performances, il est recommandé que les applications détectent si elles s’exécutent dans une session cliente Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b25bb-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="b25bb-114">Vérifiez les fuites de mémoire de votre application et résolvez les problèmes éventuels.</span><span class="sxs-lookup"><span data-stu-id="b25bb-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="b25bb-115">Bien entendu, il s’agit d’un bon conseil pour n’importe quelle application, mais dans un environnement Services Bureau à distance, une application peut être exécutée plusieurs fois par plusieurs utilisateurs, ce qui a pour effet d’agrandir rapidement l’effet d’une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b25bb-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="b25bb-116">Les animations, les grandes images, l’audio et d’autres services gourmands en bande passante doivent être configurables.</span><span class="sxs-lookup"><span data-stu-id="b25bb-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="b25bb-117">Lorsque ces services ne sont pas la fonction principale, ils peuvent être désactivés par défaut pour les sessions à distance, mais activés lorsqu’une session s’exécute localement ou sur une connexion à bande passante élevée.</span><span class="sxs-lookup"><span data-stu-id="b25bb-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="b25bb-118">Si l’objectif d’une application est de fournir des services à bande passante élevée, tels que des diffusions vidéo en continu, il n’est pas nécessaire que le service soit désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="b25bb-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




