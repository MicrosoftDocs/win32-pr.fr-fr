---
title: Propagation des informations d’erreur
description: La propagation des informations d’erreur étendues autorise les serveurs qui reçoivent une \_ erreur RPC S \_ \, ou tout autre code d’erreur, à permettre au runtime RPC de propager les informations qu’il a reçues à ses appelants.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840553"
---
# <a name="propagating-error-information"></a><span data-ttu-id="a9e75-103">Propagation des informations d’erreur</span><span class="sxs-lookup"><span data-stu-id="a9e75-103">Propagating Error Information</span></span>

<span data-ttu-id="a9e75-104">La propagation des informations d’erreur étendues autorise les serveurs qui reçoivent une \_ erreur RPC S \_ \* ou tout autre code d’erreur à permettre au runtime RPC de propager les informations qu’il a reçues à ses appelants.</span><span class="sxs-lookup"><span data-stu-id="a9e75-104">Propagating extended error information allows servers that receive an RPC\_S\_\* error, or any other error code for that matter, to allow the RPC run time to propagate the information it received to its callers.</span></span> <span data-ttu-id="a9e75-105">Tout le serveur doit faire appel à [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) lors de la rencontre d’une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="a9e75-105">All the server must do is call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) upon encountering a fatal error.</span></span> <span data-ttu-id="a9e75-106">Le temps d’exécution RPC prend en charge le chaînage des informations d’erreur étendues, le cas échéant, provoquant l’erreur irrécupérable pour signaler l’erreur irrécupérable, tant que le code d’erreur donné à **RpcRaiseException** ou **RpcAsyncAbortCall** est le même que le code d’erreur à l’origine de l’erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="a9e75-106">The RPC run time takes care of chaining the extended error information, if any, causing the fatal error to report the fatal error itself, as long as the error code given to **RpcRaiseException** or **RpcAsyncAbortCall** is the same as the error code causing the fatal error.</span></span>

 

 




