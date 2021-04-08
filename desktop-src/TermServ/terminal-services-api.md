---
title: API Services Bureau à distance
description: L’API Services Bureau à distance est surtout utile pour les applications client/serveur et les applications pour l’administration des Services Bureau à distance.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839785"
---
# <a name="remote-desktop-services-api"></a><span data-ttu-id="1d5c1-103">API Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="1d5c1-103">Remote Desktop Services API</span></span>

<span data-ttu-id="1d5c1-104">La plupart des applications s’exécutent sans modification dans un environnement Services Bureau à distance (anciennement appelé Terminal Services) et n’ont pas besoin d’utiliser l’API Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-104">Most applications run without modification in a Remote Desktop Services (formerly known as Terminal Services) environment and do not need to use the Remote Desktop Services API.</span></span> <span data-ttu-id="1d5c1-105">L’API Services Bureau à distance est surtout utile pour les applications client/serveur et les applications pour l’administration des Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-105">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

<span data-ttu-id="1d5c1-106">L’API Services Bureau à distance est un ensemble d’appels de fonction dans Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-106">The Remote Desktop Services API is a set of function calls into Wtsapi32.dll.</span></span> <span data-ttu-id="1d5c1-107">Pour concevoir votre application afin qu’elle s’exécute dans des environnements Services Bureau à distance et non Services Bureau à distance, utilisez la liaison dynamique au moment de l’exécution pour vérifier la présence de Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-107">To design your application to run in both Remote Desktop Services and non-Remote Desktop Services environments, use run-time dynamic linking to check for the presence of Wtsapi32.dll.</span></span> <span data-ttu-id="1d5c1-108">Pour plus d’informations, consultez la page [liaison au moment de l’exécution pour Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="1d5c1-108">For more information, see [Run-Time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="1d5c1-109">L’API Services Bureau à distance permet aux applications d’effectuer les tâches suivantes dans un environnement de Services Bureau à distance :</span><span class="sxs-lookup"><span data-stu-id="1d5c1-109">The Remote Desktop Services API enables applications to perform the following tasks in a Remote Desktop Services environment:</span></span>

-   <span data-ttu-id="1d5c1-110">[Services Bureau à distance l’administration](terminal-services-administration.md), telles que l’énumération et la gestion des serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) (anciennement appelés serveurs Terminal Server) dans un domaine ou l’énumération et la gestion des sessions et des processus sur un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-110">[Remote Desktop Services Administration](terminal-services-administration.md), such as enumerating and managing Remote Desktop Session Host (RD Session Host) servers (formerly known as terminal servers) in a domain or enumerating and managing sessions and processes on an RD Session Host server.</span></span>
-   <span data-ttu-id="1d5c1-111">Amélioration des applications client/serveur dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-111">Enhancing client/server applications in a Remote Desktop Services environment.</span></span>
-   <span data-ttu-id="1d5c1-112">Utilisation de [services Bureau à distance canaux virtuels](terminal-services-virtual-channels.md) pour communiquer entre les modules client et serveur d’une application.</span><span class="sxs-lookup"><span data-stu-id="1d5c1-112">Using [Remote Desktop Services Virtual Channels](terminal-services-virtual-channels.md) to communicate between client and server modules of an application.</span></span>
-   <span data-ttu-id="1d5c1-113">[Définition et récupération d’services Bureau à distance informations spécifiques sur la configuration de l’utilisateur](terminal-services-user-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="1d5c1-113">[Setting and retrieving Remote Desktop Services specific user configuration information](terminal-services-user-configuration.md).</span></span>

 

 




