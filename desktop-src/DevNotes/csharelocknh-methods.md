---
description: Groupe de méthodes utilisé pour manipuler des verrous.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Méthodes CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513128"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="54e43-103">Méthodes CShareLockNH</span><span class="sxs-lookup"><span data-stu-id="54e43-103">CShareLockNH Methods</span></span>

<span data-ttu-id="54e43-104">Groupe de méthodes utilisé pour manipuler des verrous.</span><span class="sxs-lookup"><span data-stu-id="54e43-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="54e43-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54e43-105">Methods</span></span>

<span data-ttu-id="54e43-106">Voici les méthodes exportées par Rwnh.dll.</span><span class="sxs-lookup"><span data-stu-id="54e43-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="54e43-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="54e43-107">Method</span></span>                                                                   | <span data-ttu-id="54e43-108">Description</span><span class="sxs-lookup"><span data-stu-id="54e43-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="54e43-109">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="54e43-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="54e43-110">Acquiert un verrou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="54e43-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="54e43-111">**ExclusiveToPartial**</span><span class="sxs-lookup"><span data-stu-id="54e43-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="54e43-112">Modifie l’État.</span><span class="sxs-lookup"><span data-stu-id="54e43-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="54e43-113">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="54e43-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="54e43-114">Libère un verrou.</span><span class="sxs-lookup"><span data-stu-id="54e43-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="54e43-115">**FirstPartialToExclusive**</span><span class="sxs-lookup"><span data-stu-id="54e43-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="54e43-116">Utilisé pour la conversion d’un verrou partiel en verrou exclusif.</span><span class="sxs-lookup"><span data-stu-id="54e43-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="54e43-117">**PartialLock**</span><span class="sxs-lookup"><span data-stu-id="54e43-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="54e43-118">Empêche plusieurs threads de terminer l’acquisition d’un verrou.</span><span class="sxs-lookup"><span data-stu-id="54e43-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="54e43-119">**PartialUnlock**</span><span class="sxs-lookup"><span data-stu-id="54e43-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="54e43-120">Libère un verrou partiel.</span><span class="sxs-lookup"><span data-stu-id="54e43-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="54e43-121">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="54e43-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="54e43-122">Obtient un verrou pour le mode partagé.</span><span class="sxs-lookup"><span data-stu-id="54e43-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="54e43-123">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="54e43-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="54e43-124">Libère un verrou en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="54e43-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="54e43-125">**SharedToPartial**</span><span class="sxs-lookup"><span data-stu-id="54e43-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="54e43-126">Obtient un verrou partiel.</span><span class="sxs-lookup"><span data-stu-id="54e43-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="54e43-127">**TryExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="54e43-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="54e43-128">Obtient un verrou en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="54e43-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 



