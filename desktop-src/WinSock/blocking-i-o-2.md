---
description: La forme la plus simple des e/s dans Windows Sockets 2 est le blocage des e/s.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blocage des entrées/sorties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513228"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="24d98-103">Blocage des entrées/sorties</span><span class="sxs-lookup"><span data-stu-id="24d98-103">Blocking Input/Output</span></span>

<span data-ttu-id="24d98-104">La forme la plus simple des e/s dans Windows Sockets 2 est le blocage des e/s.</span><span class="sxs-lookup"><span data-stu-id="24d98-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="24d98-105">Comme mentionné dans les [indicateurs et les modes d’attribut de socket](socket-attribute-flags-and-modes-2.md), les sockets sont créés en mode blocage par défaut.</span><span class="sxs-lookup"><span data-stu-id="24d98-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="24d98-106">Toute opération d’e/s avec un socket bloquant n’est pas retournée tant que l’opération n’a pas été complètement terminée.</span><span class="sxs-lookup"><span data-stu-id="24d98-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="24d98-107">Ainsi, tout thread ne peut exécuter qu’une seule opération d’e/s à la fois.</span><span class="sxs-lookup"><span data-stu-id="24d98-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="24d98-108">Par exemple, si un thread émet une opération de réception et qu’aucune donnée n’est actuellement disponible, le thread se bloque jusqu’à ce que les données deviennent disponibles et placées dans la mémoire tampon du thread.</span><span class="sxs-lookup"><span data-stu-id="24d98-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="24d98-109">Bien que cela soit simple, il ne s’agit pas nécessairement de la méthode la plus efficace pour effectuer des e/s (pour plus d’informations, consultez la page relative aux [Pseudo-blocages et au blocage réel](pseudo-vs--true-blocking-2.md) ).</span><span class="sxs-lookup"><span data-stu-id="24d98-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



