---
title: Réception de la réponse asynchrone
description: Une fois que le serveur a envoyé une réponse, le client appelle RpcAsyncCompleteCall avec le handle asynchrone afin qu’il puisse recevoir la réponse.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382616"
---
# <a name="receiving-the-asynchronous-reply"></a><span data-ttu-id="bfcda-103">Réception de la réponse asynchrone</span><span class="sxs-lookup"><span data-stu-id="bfcda-103">Receiving the Asynchronous Reply</span></span>

<span data-ttu-id="bfcda-104">Une fois que le serveur a envoyé une réponse, le client appelle [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) avec le handle asynchrone afin qu’il puisse recevoir la réponse.</span><span class="sxs-lookup"><span data-stu-id="bfcda-104">After it is notified that the server has sent a reply, the client calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) with the asynchronous handle so that it can receive the reply.</span></span> <span data-ttu-id="bfcda-105">Lorsque **RpcAsyncCompleteCall** s’est terminé avec succès, le paramètre *reply* pointe vers une mémoire tampon qui contient la valeur de retour de la fonction distante.</span><span class="sxs-lookup"><span data-stu-id="bfcda-105">When **RpcAsyncCompleteCall** has completed successfully, the *Reply* parameter points to a buffer that contains the return value of the remote function.</span></span> <span data-ttu-id="bfcda-106">Toutes les mémoires tampons fournies par le programme client comme des \[ [](/windows/desktop/Midl/out-idl) \] paramètres out ou \[ [**in**](/windows/desktop/Midl/in), **out** \] à la fonction distante asynchrone contiennent des données valides.</span><span class="sxs-lookup"><span data-stu-id="bfcda-106">Any buffers supplied by the client program as \[[**out**](/windows/desktop/Midl/out-idl)\] or \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to the asynchronous remote function contain valid data.</span></span> <span data-ttu-id="bfcda-107">Si le client appelle **RpcAsyncCompleteCall** avant que le serveur n’ait envoyé la réponse, cet appel échoue et retourne la valeur RPC \_ S \_ Async \_ Call \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="bfcda-107">If the client calls **RpcAsyncCompleteCall** before the server has sent the reply, that call will fail and return a value of RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="bfcda-108">Si votre programme client utilise des ports de terminaison d’e/s ou des événements pour la notification, il doit appeler [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) pour libérer le port ou le descripteur lorsqu’il n’en a plus besoin.</span><span class="sxs-lookup"><span data-stu-id="bfcda-108">If your client program uses I/O completion ports or events for notification, it must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to release the port or handle when it no longer needs them.</span></span>

 

 