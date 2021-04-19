---
description: La classe CAMMsgEvent est un wrapper pour les objets d’événement qui effectuent le traitement des messages.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: CAMMsgEvent, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536040"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="3aeb9-103">CAMMsgEvent, classe</span><span class="sxs-lookup"><span data-stu-id="3aeb9-103">CAMMsgEvent class</span></span>

![hiérarchie de la classe cammsgevent](images/util06.png)

<span data-ttu-id="3aeb9-105">La `CAMMsgEvent` classe est un wrapper pour les objets d’événement qui effectuent le traitement des messages.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="3aeb9-106">Cette classe dérive de l’objet [**CAMEvent**](camevent.md) .</span><span class="sxs-lookup"><span data-stu-id="3aeb9-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="3aeb9-107">Elle ajoute une méthode, [**CAMMsgEvent :: WaitMsg**](cammsgevent-waitmsg.md), qui distribue les messages entrants en attente.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="3aeb9-108">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="3aeb9-108">Public Methods</span></span>                                 | <span data-ttu-id="3aeb9-109">Description</span><span class="sxs-lookup"><span data-stu-id="3aeb9-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3aeb9-110">**CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="3aeb9-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="3aeb9-111">Constructeur.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="3aeb9-112">**WaitMsg**</span><span class="sxs-lookup"><span data-stu-id="3aeb9-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="3aeb9-113">Attend que l’événement soit signalé, tout en distribuant les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3aeb9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aeb9-114">Requirements</span></span>



| <span data-ttu-id="3aeb9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aeb9-115">Requirement</span></span> | <span data-ttu-id="3aeb9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aeb9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aeb9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3aeb9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3aeb9-118"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aeb9-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3aeb9-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3aeb9-119">Library</span></span><br/> | <dl> <span data-ttu-id="3aeb9-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3aeb9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




