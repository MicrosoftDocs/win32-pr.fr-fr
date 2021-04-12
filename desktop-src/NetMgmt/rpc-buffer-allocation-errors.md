---
title: Erreurs d’allocation de mémoire tampon RPC
description: Étant donné que la bibliothèque Runtime RPC alloue de la mémoire pour les mémoires tampons d’envoi et de réception, la fonction doit s’attendre à des erreurs d’allocation RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309966"
---
# <a name="rpc-buffer-allocation-errors"></a><span data-ttu-id="0de48-103">Erreurs d’allocation de mémoire tampon RPC</span><span class="sxs-lookup"><span data-stu-id="0de48-103">RPC Buffer Allocation Errors</span></span>

<span data-ttu-id="0de48-104">Étant donné que la bibliothèque Runtime RPC alloue de la mémoire pour les mémoires tampons d’envoi et de réception, la fonction doit s’attendre à des erreurs d’allocation RPC.</span><span class="sxs-lookup"><span data-stu-id="0de48-104">Because the RPC run-time library allocates memory for send and receive buffers, the function should expect RPC allocation errors.</span></span> <span data-ttu-id="0de48-105">Dans le cas d’une erreur d’allocation RPC, un descripteur pouvant être repris est invalidé.</span><span class="sxs-lookup"><span data-stu-id="0de48-105">In the event of an RPC allocation error, a resumable handle is invalidated.</span></span> <span data-ttu-id="0de48-106">Il s’agit d’une exigence, car les fonctions pouvant être reprises ne peuvent pas être rembobinées.</span><span class="sxs-lookup"><span data-stu-id="0de48-106">This is a requirement because resumable functions are not rewindable.</span></span>

 

 




