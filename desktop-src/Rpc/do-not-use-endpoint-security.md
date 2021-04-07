---
title: Ne pas utiliser la sécurité du point de terminaison
description: Endpoint Security est un modèle de sécurité dans lequel un descripteur de sécurité est fourni lorsqu’un point de terminaison est créé avec le groupe RpcServerUseProtseq \ des fonctions RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672841"
---
# <a name="do-not-use-endpoint-security"></a>Ne pas utiliser la sécurité du point de terminaison

Endpoint Security est un modèle de sécurité dans lequel un descripteur de sécurité est fourni lorsqu’un point de terminaison est créé avec le groupe [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* de fonctions RPC. N’utilisez pas ce modèle de sécurité. Ne fournissez pas de descripteurs de sécurité à ces fonctions. Au mieux, cette méthode est un gaspillage des ressources du processeur. Au pire, dans de nombreux environnements, il est possible de contourner le descripteur de sécurité, car les [autres points de terminaison RPC qui s’exécutent dans la section de processus](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) illustrent le plus de vigilance.

La sécurité des points de terminaison existe uniquement pour la compatibilité descendante.

 

 




