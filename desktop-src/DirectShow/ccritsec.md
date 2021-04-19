---
description: La classe CCritSec fournit un verrou de thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: CCritSec, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537453"
---
# <a name="ccritsec-class"></a><span data-ttu-id="c8184-103">CCritSec, classe</span><span class="sxs-lookup"><span data-stu-id="c8184-103">CCritSec class</span></span>

<span data-ttu-id="c8184-104">La classe **CCritSec** fournit un verrou de thread.</span><span class="sxs-lookup"><span data-stu-id="c8184-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="c8184-105">Cette classe est un wrapper léger pour un objet **de \_ section critique** Windows.</span><span class="sxs-lookup"><span data-stu-id="c8184-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="c8184-106">Vous pouvez verrouiller et déverrouiller le thread en appelant les méthodes [**CCritSec :: Lock**](ccritsec-lock.md) et [**CCritSec :: Unlock**](ccritsec-unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="c8184-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="c8184-107">Toutefois, il est plus sûr d’utiliser cette classe conjointement avec la classe [**CAutoLock**](cautolock.md) .</span><span class="sxs-lookup"><span data-stu-id="c8184-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="c8184-108">Lorsque la classe **CAutoLock** devient hors de portée, elle déverrouille automatiquement l’objet **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="c8184-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="c8184-109">En outre, il est compilé en code inline efficace.</span><span class="sxs-lookup"><span data-stu-id="c8184-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="c8184-110">Variables membres publiques</span><span class="sxs-lookup"><span data-stu-id="c8184-110">Public Member Variables</span></span>                            | <span data-ttu-id="c8184-111">Description</span><span class="sxs-lookup"><span data-stu-id="c8184-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="c8184-112">**m \_ currentOwner**</span><span class="sxs-lookup"><span data-stu-id="c8184-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="c8184-113">Identificateur de thread du thread propriétaire.</span><span class="sxs-lookup"><span data-stu-id="c8184-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="c8184-114">**m \_ lockCount**</span><span class="sxs-lookup"><span data-stu-id="c8184-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="c8184-115">Nombre de verrous en attente sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="c8184-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="c8184-116">**m \_ fTrace**</span><span class="sxs-lookup"><span data-stu-id="c8184-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="c8184-117">Valeur booléenne qui spécifie s’il faut tracer ce verrou.</span><span class="sxs-lookup"><span data-stu-id="c8184-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="c8184-118">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="c8184-118">Public Methods</span></span>                                     | <span data-ttu-id="c8184-119">Description</span><span class="sxs-lookup"><span data-stu-id="c8184-119">Description</span></span>                                              |
| [<span data-ttu-id="c8184-120">**CCritSec**</span><span class="sxs-lookup"><span data-stu-id="c8184-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="c8184-121">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c8184-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="c8184-122">**~ CCritSec**</span><span class="sxs-lookup"><span data-stu-id="c8184-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="c8184-123">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="c8184-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="c8184-124">**Lock**</span><span class="sxs-lookup"><span data-stu-id="c8184-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="c8184-125">Verrouille l’objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="c8184-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="c8184-126">**Bloquer**</span><span class="sxs-lookup"><span data-stu-id="c8184-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="c8184-127">Déverrouille l’objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="c8184-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="c8184-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8184-128">Requirements</span></span>



| <span data-ttu-id="c8184-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8184-129">Requirement</span></span> | <span data-ttu-id="c8184-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8184-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8184-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8184-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c8184-132"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8184-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c8184-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8184-133">Library</span></span><br/> | <dl> <span data-ttu-id="c8184-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c8184-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8184-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8184-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8184-136">Objets de section critique</span><span class="sxs-lookup"><span data-stu-id="c8184-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="c8184-137">Référence de classe de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8184-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

