---
title: Utilisation de la sécurité au niveau du transport sur le serveur
description: Utilisation de la sécurité au niveau du transport sur le serveur avec l’appel de procédure distante (RPC).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- Appel de procédure distante RPC, tâches, à l’aide de la sécurité au niveau du transport sur le serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abd1f072f249336f4804aed56fb1122556596c43286383b763839d988a2406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010587"
---
# <a name="using-transport-level-security-on-the-server"></a>Utilisation de la sécurité au niveau du transport sur le serveur

Cette section présente les discussions relatives à la sécurité au niveau du transport, qui sont réparties dans les rubriques suivantes :

-   [Utilisation de Transport-Level sécurité sur le client](using-transport-level-security-on-the-client.md)

Lorsque vous utilisez [ncacn \_ NP](/windows/desktop/Midl/ncacn-np) ou [Ncalrpc](/windows/desktop/Midl/ncalrpc) comme séquence de protocole, le serveur spécifie un descripteur de sécurité pour le point de terminaison au moment où il sélectionne la séquence de protocole. Pour plus d’informations sur les séquences de protocole, consultez [spécification de séquences de protocole](specifying-protocol-sequences.md). Votre application fournit le descripteur de sécurité sous la forme d’un paramètre supplémentaire (une extension des paramètres de l’OSF-DCE standard) sur toutes les fonctions qui commencent par les préfixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) et [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Le descripteur de sécurité détermine si un client peut se connecter au point de terminaison.

Chaque processus et chaque thread sont associés à un jeton de sécurité. Ce jeton comprend un descripteur de sécurité par défaut qui est utilisé pour tous les objets créés par le processus, tels que le point de terminaison. Si votre application ne spécifie pas de descripteur de sécurité lors de l’appel d’une fonction avec les préfixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) et [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), la bibliothèque Runtime RPC applique le descripteur de sécurité par défaut du jeton de sécurité de processus au point de terminaison.

Pour garantir que l’application serveur est accessible à tous les clients, l’administrateur doit démarrer l’application serveur sur un processus qui possède un descripteur de sécurité par défaut que tous les clients peuvent utiliser. En règle générale, seuls les processus système ont un descripteur de sécurité par défaut.

Pour plus d’informations sur ces fonctions et les fonctions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) et [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 