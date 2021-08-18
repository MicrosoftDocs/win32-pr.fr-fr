---
title: Ne pas utiliser la sécurité du point de terminaison
description: Endpoint Security est un modèle de sécurité dans lequel un descripteur de sécurité est fourni lorsqu’un point de terminaison est créé avec le groupe RpcServerUseProtseq \ des fonctions RPC.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d302ec0d331eaadb3291e36b30084264b4a6331745110fc642dd2ede02c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930696"
---
# <a name="do-not-use-endpoint-security"></a>Ne pas utiliser la sécurité du point de terminaison

Endpoint Security est un modèle de sécurité dans lequel un descripteur de sécurité est fourni lorsqu’un point de terminaison est créé avec le groupe [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* de fonctions RPC. N’utilisez pas ce modèle de sécurité. Ne fournissez pas de descripteurs de sécurité à ces fonctions. Au mieux, cette méthode est un gaspillage des ressources du processeur. Au pire, dans de nombreux environnements, il est possible de contourner le descripteur de sécurité, car les [autres points de terminaison RPC qui s’exécutent dans la section de processus](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) illustrent le plus de vigilance.

La sécurité des points de terminaison existe uniquement pour la compatibilité descendante.

 

 




