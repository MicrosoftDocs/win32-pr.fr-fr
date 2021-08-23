---
title: Architecture du gestionnaire de listes de réseaux
description: Architecture du gestionnaire de listes de réseaux
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ecbb36c5421bc7e3057c43feb10f92400493b306ecb21502a541c1bb4cba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685643"
---
# <a name="network-list-manager-architecture"></a>Architecture du gestionnaire de listes de réseaux

Le gestionnaire de listes de réseaux s’exécute en tant que service dans le contexte de Svchost.exe et est démarré au cours de la procédure de démarrage de l’ordinateur. Le service Gestionnaire de listes de réseaux gère un tableau des réseaux et des attributs réseau disponibles qui sont récupérés par les applications via l’API du gestionnaire de listes de réseaux. Le gestionnaire de listes de réseaux fournit des fonctions de base pour filtrer et interroger le service Network List Manager pour des réseaux spécifiques et récupérer les attributs de ces réseaux. Le diagramme suivant illustre l’architecture du gestionnaire de listes de réseaux et l’interaction entre le service Network List Manager et l’application cliente.

![diagramme de l’architecture de détection du réseau](images/architecture.png)

 

 




