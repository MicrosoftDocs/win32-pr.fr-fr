---
title: Gestion des appels asynchrones
description: La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre. Le serveur doit effectuer le suivi de ce handle et l’utiliser pour envoyer la réponse quand l’appel de procédure distante asynchrone se termine.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc05efd8c94a8b67ad68f2d19cacd6c46ed16e80ad6bbdf6df5b475b4dc68eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020839"
---
# <a name="handling-asynchronous-calls"></a>Gestion des appels asynchrones

La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre. Le serveur doit effectuer le suivi de ce handle et l’utiliser pour envoyer la réponse quand l’appel de procédure distante asynchrone se termine.

Si le serveur doit abandonner un RPC asynchrone, il appelle [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall). Cette fonction effectue le même Nettoyage côté serveur que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) et propage un code d’exception (fourni par l’application serveur) au client, sauf qu’elle n’effectue pas le marshaling des arguments out.

Pour obtenir un exemple de procédure asynchrone, consultez [envoi de la réponse asynchrone](sending-the-asynchronous-reply.md).

 

 




