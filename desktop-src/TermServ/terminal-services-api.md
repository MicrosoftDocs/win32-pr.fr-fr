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
# <a name="remote-desktop-services-api"></a>API Services Bureau à distance

La plupart des applications s’exécutent sans modification dans un environnement Services Bureau à distance (anciennement appelé Terminal Services) et n’ont pas besoin d’utiliser l’API Services Bureau à distance. L’API Services Bureau à distance est surtout utile pour les applications client/serveur et les applications pour l’administration des Services Bureau à distance.

L’API Services Bureau à distance est un ensemble d’appels de fonction dans Wtsapi32.dll. Pour concevoir votre application afin qu’elle s’exécute dans des environnements Services Bureau à distance et non Services Bureau à distance, utilisez la liaison dynamique au moment de l’exécution pour vérifier la présence de Wtsapi32.dll. Pour plus d’informations, consultez la page [liaison au moment de l’exécution pour Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

L’API Services Bureau à distance permet aux applications d’effectuer les tâches suivantes dans un environnement de Services Bureau à distance :

-   [Services Bureau à distance l’administration](terminal-services-administration.md), telles que l’énumération et la gestion des serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) (anciennement appelés serveurs Terminal Server) dans un domaine ou l’énumération et la gestion des sessions et des processus sur un serveur hôte de session Bureau à distance.
-   Amélioration des applications client/serveur dans un environnement de Services Bureau à distance.
-   Utilisation de [services Bureau à distance canaux virtuels](terminal-services-virtual-channels.md) pour communiquer entre les modules client et serveur d’une application.
-   [Définition et récupération d’services Bureau à distance informations spécifiques sur la configuration de l’utilisateur](terminal-services-user-configuration.md).

 

 




