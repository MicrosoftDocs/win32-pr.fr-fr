---
title: Niveaux matériels
description: Les niveaux de matériel du niveau 1 au niveau 3 ont des ressources accrues disponibles pour le pipeline.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228215"
---
# <a name="hardware-tiers"></a>Niveaux matériels

Les niveaux de matériel du niveau 1 au niveau 3 ont des ressources accrues disponibles pour le pipeline.

-   [Limites dépend du matériel](#limits-dependant-on-hardware)
-   [Limites invariables](#invariable-limits)
-   [Rubriques connexes](#related-topics)

## <a name="limits-dependant-on-hardware"></a>Limites dépend du matériel



| Ressources disponibles pour le pipeline                                                                                                              | Niveau 1                                                                   | Niveau 2        | Niveau 3        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| Niveaux de fonctionnalité                                                                                                                                   | 11.0+                                                                    | 11.0+         | 11.1 +         |
| Nombre maximal de descripteurs dans une vue de mémoire tampon constante (CBV), un Affichage des ressources de nuanceur (SRV) ou un tas de vue d’accès non ordonné (UAV) utilisé pour le rendu | 1 000 000                                                                | 1 000 000     | 1000000 +    |
| Nombre maximal de vues de mémoire tampon constante dans toutes les tables de descripteurs par étape de nuanceur                                                                | 14                                                                       | 14            | **tas complet** |
| Nombre maximal de vues de ressources de nuanceur dans toutes les tables de descripteurs par étape de nuanceur                                                                | 128                                                                      | **tas complet** | tas complet     |
| Nombre maximal de vues d’accès non ordonnées dans toutes les tables de descripteurs dans toutes les étapes                                                              | 64 pour les niveaux de fonctionnalité 11.1 +<br/> 8 pour le niveau de fonctionnalité 11<br/> | 64            | **tas complet** |
| Nombre maximal d’échantillonneurs dans toutes les tables de descripteurs par étape de nuanceur                                                                             | 16                                                                       | **2048** | 2 048     |



 

Les entrées en **gras** mettent en évidence des améliorations significatives par rapport au niveau précédent.

Il existe une restriction supplémentaire pour le matériel de niveau 1 qui s’applique à tous les segments de mémoire, et au matériel de niveau 2 qui s’applique aux tas CBV et UAV, que toutes les entrées de tas de descripteurs couvertes par les tables de descripteurs dans la signature racine *doivent* être remplies par les descripteurs au moment de l’exécution du nuanceur, même si le nuanceur Il n’existe aucune restriction de ce type pour le matériel de niveau 3. L’une des mesures d’atténuation pour cette restriction est l’utilisation diligente des [descripteurs null](descriptors.md).

## <a name="invariable-limits"></a>Limites invariables

Le nombre maximal d’échantillonneurs dans un tas de descripteur visible par le nuanceur est 2048.

Le nombre maximal d’échantillons statiques uniques dans les signatures racines dynamiques est 2032 (ce qui laisse 16 pour les pilotes qui ont besoin de leurs propres échantillonneurs).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> <dt>

[Niveaux de fonctionnalité matérielle](hardware-feature-levels.md)
</dt> </dl>

 

 





