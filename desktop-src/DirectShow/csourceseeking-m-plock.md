---
description: Pointeur vers un objet de section critique.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Membre CSourceSeeking :: m_pLock (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537101"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="7b069-103">CSourceSeeking :: m \_ pLock, membre</span><span class="sxs-lookup"><span data-stu-id="7b069-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="7b069-104">Pointeur vers un objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="7b069-104">Pointer to a critical section object.</span></span> <span data-ttu-id="7b069-105">La `CSourceSeeking` classe utilise cette section critique pour synchroniser l’accès aux variables d’heure de début et de fin, de durée et de taux.</span><span class="sxs-lookup"><span data-stu-id="7b069-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="7b069-106">Cette variable est initialisée dans la méthode du constructeur ; consultez [**CSourceSeeking :: CSourceSeeking**](csourceseeking-csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="7b069-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b069-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b069-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="7b069-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b069-108">Requirements</span></span>



| <span data-ttu-id="7b069-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b069-109">Requirement</span></span> | <span data-ttu-id="7b069-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b069-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b069-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b069-111">Header</span></span><br/>  | <dl> <span data-ttu-id="7b069-112"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b069-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b069-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b069-113">Library</span></span><br/> | <dl> <span data-ttu-id="7b069-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7b069-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b069-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b069-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b069-116">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="7b069-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




