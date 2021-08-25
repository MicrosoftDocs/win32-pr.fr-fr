---
title: RPC asynchrone sur le protocole Named-Pipe
description: Si vous utilisez des canaux nommés (ncacn \_ NP) comme protocole de transport, vous devez éviter d’autoriser un grand nombre d’appels en attente d’inactivité sur le serveur.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1dade78846bc978abeb8bbbe5c324144db2645177722ca5afd1a62f99a3ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023669"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>RPC asynchrone sur le protocole Named-Pipe

Si vous utilisez des canaux nommés ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) comme protocole de transport, vous devez éviter d’autoriser un grand nombre d’appels en attente d’inactivité sur le serveur. Avec les canaux nommés, chaque client qui attend une réponse aura un canal nommé en attente de lecture sur le serveur, chacun d’entre eux nécessitant une certaine quantité de mémoire du noyau.

Par exemple, vous ne souhaitez pas utiliser un appel de notification pour le nouveau courrier électronique avec le transport de canal nommé, car ce type d’appel reste en attente même lorsque les clients sont inactifs et que la mémoire du noyau peut être épuisée. Notez qu’il ne s’agit pas d’un problème avec les autres protocoles orientés connexion, tels que [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).

Étant donné que les canaux nommés sont un protocole de transport, votre application peut les utiliser en spécifiant [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) comme protocole dans une liaison de chaîne. Pour plus d’informations sur les canaux nommés, consultez [canaux nommés](/windows/desktop/ipc/named-pipes). Pour plus d’informations sur la création de liaisons de chaînes, consultez [utilisation des liaisons de chaînes](finding-server-host-systems.md).

 

 