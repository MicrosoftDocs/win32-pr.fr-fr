---
title: Architecture du gestionnaire de listes de réseaux
description: Architecture du gestionnaire de listes de réseaux
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940321"
---
# <a name="network-list-manager-architecture"></a><span data-ttu-id="15991-103">Architecture du gestionnaire de listes de réseaux</span><span class="sxs-lookup"><span data-stu-id="15991-103">Network List Manager Architecture</span></span>

<span data-ttu-id="15991-104">Le gestionnaire de listes de réseaux s’exécute en tant que service dans le contexte de Svchost.exe et est démarré au cours de la procédure de démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="15991-104">Network List Manager runs as a service in the context of Svchost.exe and is started during the computer boot procedure.</span></span> <span data-ttu-id="15991-105">Le service Gestionnaire de listes de réseaux gère un tableau des réseaux et des attributs réseau disponibles qui sont récupérés par les applications via l’API du gestionnaire de listes de réseaux.</span><span class="sxs-lookup"><span data-stu-id="15991-105">The Network List Manager service maintains a table of available networks and network attributes that are retrieved by applications through the Network List Manager API.</span></span> <span data-ttu-id="15991-106">Le gestionnaire de listes de réseaux fournit des fonctions de base pour filtrer et interroger le service Network List Manager pour des réseaux spécifiques et récupérer les attributs de ces réseaux.</span><span class="sxs-lookup"><span data-stu-id="15991-106">Network List Manager provides basic functions to filter and query the Network List Manager service for specific networks and retrieve the attributes of these networks.</span></span> <span data-ttu-id="15991-107">Le diagramme suivant illustre l’architecture du gestionnaire de listes de réseaux et l’interaction entre le service Network List Manager et l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="15991-107">The following diagram shows the Network List Manager architecture and the interaction between the Network List Manager service and the client application.</span></span>

![diagramme de l’architecture de détection du réseau](images/architecture.png)

 

 




