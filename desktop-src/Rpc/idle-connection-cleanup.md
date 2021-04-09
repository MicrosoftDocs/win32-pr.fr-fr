---
title: Nettoyage des connexions inactives
description: Par défaut, les connexions dans le pool de threads ne sont pas fermées tant que l’ensemble de l’Association n’est pas arrêté.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839506"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="cf798-103">Nettoyage des connexions inactives</span><span class="sxs-lookup"><span data-stu-id="cf798-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="cf798-104">Par défaut, les connexions dans le pool de threads ne sont pas fermées tant que l’ensemble de l’Association n’est pas arrêté.</span><span class="sxs-lookup"><span data-stu-id="cf798-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="cf798-105">Cette stratégie permet aux clients disposant d’un grand nombre de threads ou d’identités de sécurité d’effectuer des appels RPC au serveur de manière efficace.</span><span class="sxs-lookup"><span data-stu-id="cf798-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="cf798-106">L’inconvénient est qu’une quantité insuffisante de ressources peut être engagée pour maintenir ces connexions.</span><span class="sxs-lookup"><span data-stu-id="cf798-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="cf798-107">Pour gérer le processus, RPC fournit la fonction [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) .</span><span class="sxs-lookup"><span data-stu-id="cf798-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="cf798-108">Cette fonction active le nettoyage des connexions inactives ; le client analyse régulièrement le pool de connexions et ferme les connexions qui n’ont pas été utilisées récemment.</span><span class="sxs-lookup"><span data-stu-id="cf798-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="cf798-109">Si l’Association a conservé des handles de contexte, le nettoyage de la connexion inactive ferme toutes les connexions inactives, mais veille à ce qu’au moins une connexion reste ouverte, même si la connexion est inactive (sinon, le serveur reçoit des dépassements de contexte).</span><span class="sxs-lookup"><span data-stu-id="cf798-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="cf798-110">Si l’Association n’a pas conservé de handles de contexte, le nettoyage de la connexion inactive ferme toutes les connexions inactives, même si cela ne laisse aucune connexion dans le pool.</span><span class="sxs-lookup"><span data-stu-id="cf798-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="cf798-111">Sur Windows XP, le délai d’exécution RPC conserve le suivi du nombre de connexions ouvertes dans une association et active automatiquement le nettoyage de la connexion inactive si le nombre de connexions dans une association dépasse un certain seuil.</span><span class="sxs-lookup"><span data-stu-id="cf798-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




