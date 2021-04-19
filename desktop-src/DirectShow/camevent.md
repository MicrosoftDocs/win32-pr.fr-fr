---
description: La classe CAMEvent est un wrapper pour les événements de réinitialisation manuelle et de réinitialisation automatique.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: CAMEvent, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542523"
---
# <a name="camevent-class"></a><span data-ttu-id="b6d20-103">CAMEvent, classe</span><span class="sxs-lookup"><span data-stu-id="b6d20-103">CAMEvent class</span></span>

![hiérarchie de la classe camevent](images/util06.png)

<span data-ttu-id="b6d20-105">La classe **CAMEvent** est un wrapper pour les événements de réinitialisation manuelle et de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="b6d20-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="b6d20-106">Cette classe offre un moyen pratique de gérer les événements, plutôt que d’appeler des fonctions telles que [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)et [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span><span class="sxs-lookup"><span data-stu-id="b6d20-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="b6d20-107">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="b6d20-107">Protected Member Variables</span></span>                          | <span data-ttu-id="b6d20-108">Description</span><span class="sxs-lookup"><span data-stu-id="b6d20-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="b6d20-109">**m \_ hEvent**</span><span class="sxs-lookup"><span data-stu-id="b6d20-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="b6d20-110">Handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="b6d20-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="b6d20-111">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="b6d20-111">Public Methods</span></span>                                      | <span data-ttu-id="b6d20-112">Description</span><span class="sxs-lookup"><span data-stu-id="b6d20-112">Description</span></span>                                                     |
| [<span data-ttu-id="b6d20-113">**CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="b6d20-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="b6d20-114">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="b6d20-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="b6d20-115">**~ CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="b6d20-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="b6d20-116">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="b6d20-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="b6d20-117">**Vérification**</span><span class="sxs-lookup"><span data-stu-id="b6d20-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="b6d20-118">Vérifie si l’événement est défini, sans blocage.</span><span class="sxs-lookup"><span data-stu-id="b6d20-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="b6d20-119">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="b6d20-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="b6d20-120">Définit l’état de l’événement comme étant non signalé.</span><span class="sxs-lookup"><span data-stu-id="b6d20-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="b6d20-121">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="b6d20-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="b6d20-122">Signale l’événement.</span><span class="sxs-lookup"><span data-stu-id="b6d20-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="b6d20-123">**Wait**</span><span class="sxs-lookup"><span data-stu-id="b6d20-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="b6d20-124">Bloque jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise.</span><span class="sxs-lookup"><span data-stu-id="b6d20-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="b6d20-125">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="b6d20-125">Operators</span></span>                                           | <span data-ttu-id="b6d20-126">Description</span><span class="sxs-lookup"><span data-stu-id="b6d20-126">Description</span></span>                                                     |
| [<span data-ttu-id="b6d20-127">**HANDLE d’opérateur**</span><span class="sxs-lookup"><span data-stu-id="b6d20-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="b6d20-128">Récupère le handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="b6d20-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="b6d20-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6d20-129">Requirements</span></span>



| <span data-ttu-id="b6d20-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6d20-130">Requirement</span></span> | <span data-ttu-id="b6d20-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6d20-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d20-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6d20-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b6d20-133"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d20-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b6d20-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6d20-134">Library</span></span><br/> | <dl> <span data-ttu-id="b6d20-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d20-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

