---
description: Si un socket est en mode non bloquant, toute opération d’e/s doit être terminée immédiatement ou renvoyer le code d’erreur WSAEWOULDBLOCK indiquant que l’opération ne peut pas être terminée immédiatement.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Entrée/sortie non bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526128"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="ee8a9-103">Entrée/sortie non bloquantes</span><span class="sxs-lookup"><span data-stu-id="ee8a9-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="ee8a9-104">Si un socket est en mode non bloquant, toute opération d’e/s doit être terminée immédiatement ou renvoyer le code d’erreur WSAEWOULDBLOCK indiquant que l’opération ne peut pas être terminée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ee8a9-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="ee8a9-105">Dans ce dernier cas, un mécanisme est nécessaire pour déterminer s’il est approprié de retenter l’opération dans l’attente que l’opération aboutisse.</span><span class="sxs-lookup"><span data-stu-id="ee8a9-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="ee8a9-106">Un ensemble d’événements réseau a été défini à cet effet.</span><span class="sxs-lookup"><span data-stu-id="ee8a9-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="ee8a9-107">Ces événements peuvent être interrogés ou attendus à l’aide de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), ou ils peuvent être inscrits pour la remise asynchrone en appelant [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) ou [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee8a9-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="ee8a9-108">Pour plus d’informations, consultez [notification des événements réseau](notification-of-network-events-2.md) .</span><span class="sxs-lookup"><span data-stu-id="ee8a9-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
