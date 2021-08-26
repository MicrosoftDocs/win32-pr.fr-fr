---
title: Serveurs DNS
description: En savoir plus sur les serveurs DNS. Un serveur DNS est un ordinateur qui termine le processus de résolution de noms dans DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Serveurs DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f1eb0391d588431e082c69bcd19768c4047b1e4e24c64fbda251c11703a7eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131829"
---
# <a name="dns-servers"></a>Serveurs DNS

Un *serveur DNS* est un ordinateur qui termine le processus de résolution de noms dans DNS. Les serveurs DNS contiennent des [*fichiers de zone*](z-gly.md) qui leur permettent de résoudre les noms en adresses IP et adresses IP en noms. Lorsqu’il est interrogé, un serveur DNS répond de l’une des trois façons suivantes :

-   Le serveur retourne les données de résolution de noms ou de résolution IP demandées.
-   Le serveur retourne un pointeur vers un autre serveur DNS qui peut traiter la demande.
-   Le serveur indique qu’il n’a pas les données demandées.

Les serveurs DNS peuvent, au cours de la préparation, renvoyer les données de résolution demandées, interroger d’autres serveurs DNS, mais au-delà, les serveurs DNS n’effectuent aucune autre opération.

Il existe trois types principaux de serveurs DNS : les serveurs principaux, les serveurs secondaires et les serveurs de mise en cache.

## <a name="primary-server"></a>Serveur principal

Le *serveur principal* est le serveur faisant autorité pour la zone. Toutes les tâches d’administration associées à la zone (telles que la création de sous-domaines dans la zone, ou d’autres tâches d’administration similaires) doivent être effectuées sur le serveur principal. En outre, toute modification associée à la zone, ou toute modification ou ajout à des RR dans les fichiers de zone, doit être effectuée sur le serveur principal. Pour une zone donnée, il y a un serveur principal, sauf lorsque vous intégrez Active Directory Services et le serveur DNS Microsoft.

## <a name="secondary-servers"></a>Serveurs secondaires

Les *serveurs secondaires* sont des serveurs DNS de sauvegarde. Les serveurs secondaires reçoivent tous leurs fichiers de zone des fichiers de zone du serveur principal dans un transfert de zone. Plusieurs serveurs secondaires peuvent exister pour une zone donnée, autant que nécessaire pour assurer l' [*équilibrage*](l-gly.md)de la charge, la [*tolérance aux pannes*](f-gly.md)et la réduction du trafic. En outre, tout serveur DNS donné peut être un serveur secondaire pour plusieurs zones.

Outre les serveurs DNS principal et secondaire, des rôles de serveur DNS supplémentaires peuvent être utilisés lorsque ces serveurs sont appropriés pour une infrastructure DNS. Ces serveurs supplémentaires mettent en cache les serveurs et les [*redirecteurs*](f-gly.md).

## <a name="caching-servers"></a>Serveurs de mise en cache

Les [*serveurs de mise en cache*](c-gly.md), également appelés serveurs avec mise en cache uniquement, s’exécutent comme leur nom. ils fournissent uniquement un service de requête mis en cache pour les réponses DNS. Plutôt que de gérer des fichiers de zone comme d’autres serveurs secondaires, la mise en cache des serveurs DNS effectue des requêtes, met en cache les réponses et retourne les résultats au client d’interrogation. La principale différence entre la mise en cache de serveurs et d’autres serveurs secondaires réside dans le fait que les autres serveurs secondaires gèrent les fichiers de zone (et effectuent les transferts de zone le cas échéant, générant ainsi le trafic réseau associé au transfert), pas les serveurs de mise en cache.

 

 




