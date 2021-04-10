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
# <a name="network-list-manager-architecture"></a>Architecture du gestionnaire de listes de réseaux

Le gestionnaire de listes de réseaux s’exécute en tant que service dans le contexte de Svchost.exe et est démarré au cours de la procédure de démarrage de l’ordinateur. Le service Gestionnaire de listes de réseaux gère un tableau des réseaux et des attributs réseau disponibles qui sont récupérés par les applications via l’API du gestionnaire de listes de réseaux. Le gestionnaire de listes de réseaux fournit des fonctions de base pour filtrer et interroger le service Network List Manager pour des réseaux spécifiques et récupérer les attributs de ces réseaux. Le diagramme suivant illustre l’architecture du gestionnaire de listes de réseaux et l’interaction entre le service Network List Manager et l’application cliente.

![diagramme de l’architecture de détection du réseau](images/architecture.png)

 

 




