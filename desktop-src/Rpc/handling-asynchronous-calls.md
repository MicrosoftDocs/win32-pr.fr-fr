---
title: Gestion des appels asynchrones
description: La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre. Le serveur doit effectuer le suivi de ce handle et l’utiliser pour envoyer la réponse quand l’appel de procédure distante asynchrone se termine.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380053"
---
# <a name="handling-asynchronous-calls"></a>Gestion des appels asynchrones

La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre. Le serveur doit effectuer le suivi de ce handle et l’utiliser pour envoyer la réponse quand l’appel de procédure distante asynchrone se termine.

Si le serveur doit abandonner un RPC asynchrone, il appelle [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall). Cette fonction effectue le même Nettoyage côté serveur que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) et propage un code d’exception (fourni par l’application serveur) au client, sauf qu’elle n’effectue pas le marshaling des arguments out.

Pour obtenir un exemple de procédure asynchrone, consultez [envoi de la réponse asynchrone](sending-the-asynchronous-reply.md).

 

 




