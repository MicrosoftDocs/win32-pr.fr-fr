---
description: La liste suivante répertorie les objectifs de la conception de MSP pour TAPI.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Objectifs de conception généraux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524902"
---
# <a name="general-design-goals"></a><span data-ttu-id="b4169-103">Objectifs de conception généraux</span><span class="sxs-lookup"><span data-stu-id="b4169-103">General Design Goals</span></span>

<span data-ttu-id="b4169-104">La liste suivante répertorie les objectifs de la conception de MSP pour TAPI.</span><span class="sxs-lookup"><span data-stu-id="b4169-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="b4169-105">Les classes de base sont restées simples, avec les membres et les méthodes introduits uniquement lorsque cela est absolument nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b4169-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="b4169-106">Héritage simple.</span><span class="sxs-lookup"><span data-stu-id="b4169-106">Simple inheritance.</span></span> <span data-ttu-id="b4169-107">Aucun héritage multiple entre les classes, bien que l’héritage multiple soit utilisé pour les interfaces.</span><span class="sxs-lookup"><span data-stu-id="b4169-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="b4169-108">Le verrouillage ne se produit que dans une seule direction pour empêcher tout interblocage.</span><span class="sxs-lookup"><span data-stu-id="b4169-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="b4169-109">Les méthodes sur l’objet d’appel qui requièrent le verrou sur l’appel peuvent appeler des méthodes sur le flux qui requièrent le verrou sur le flux.</span><span class="sxs-lookup"><span data-stu-id="b4169-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="b4169-110">Toutefois, les méthodes sur le flux qui requièrent le verrou sur le flux n’appellera jamais une méthode sur l’appel qui requiert un verrou sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="b4169-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="b4169-111">Les refCounts sont utilisés pour protéger l’accès.</span><span class="sxs-lookup"><span data-stu-id="b4169-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="b4169-112">Tous les rappels postés dans le pool de threads détiennent refCounts.</span><span class="sxs-lookup"><span data-stu-id="b4169-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="b4169-113">Le refcount est annulé lorsque l’attente est annulée.</span><span class="sxs-lookup"><span data-stu-id="b4169-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="b4169-114">L’objet Address contient refCounts sur les terminaux.</span><span class="sxs-lookup"><span data-stu-id="b4169-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="b4169-115">Les objets d’appel ont des refCounts sur l’adresse et sur les flux.</span><span class="sxs-lookup"><span data-stu-id="b4169-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="b4169-116">Les objets de flux ont des refCounts sur les appels et les terminaux.</span><span class="sxs-lookup"><span data-stu-id="b4169-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="b4169-117">Les terminaux ont des refCounts sur les flux.</span><span class="sxs-lookup"><span data-stu-id="b4169-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="b4169-118">L’refCounts circulaire s’arrête lorsque la méthode Shutdown sur les objets Address et Call est appelée.</span><span class="sxs-lookup"><span data-stu-id="b4169-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



