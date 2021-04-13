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
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="feaf1-104">Gestion des appels asynchrones</span><span class="sxs-lookup"><span data-stu-id="feaf1-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="feaf1-105">La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="feaf1-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="feaf1-106">Le serveur doit effectuer le suivi de ce handle et l’utiliser pour envoyer la réponse quand l’appel de procédure distante asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="feaf1-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="feaf1-107">Si le serveur doit abandonner un RPC asynchrone, il appelle [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span><span class="sxs-lookup"><span data-stu-id="feaf1-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="feaf1-108">Cette fonction effectue le même Nettoyage côté serveur que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) et propage un code d’exception (fourni par l’application serveur) au client, sauf qu’elle n’effectue pas le marshaling des arguments out.</span><span class="sxs-lookup"><span data-stu-id="feaf1-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="feaf1-109">Pour obtenir un exemple de procédure asynchrone, consultez [envoi de la réponse asynchrone](sending-the-asynchronous-reply.md).</span><span class="sxs-lookup"><span data-stu-id="feaf1-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




