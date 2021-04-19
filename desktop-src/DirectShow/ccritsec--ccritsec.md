---
description: Méthode de destructeur.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec, destructeur (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543273"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="6d703-103">CCritSec. ~ CCritSec, destructeur</span><span class="sxs-lookup"><span data-stu-id="6d703-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="6d703-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="6d703-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d703-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d703-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="6d703-106">Notes</span><span class="sxs-lookup"><span data-stu-id="6d703-106">Remarks</span></span>

<span data-ttu-id="6d703-107">Cette méthode appelle la fonction [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) pour supprimer la section critique.</span><span class="sxs-lookup"><span data-stu-id="6d703-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d703-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d703-108">Requirements</span></span>



| <span data-ttu-id="6d703-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d703-109">Requirement</span></span> | <span data-ttu-id="6d703-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d703-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d703-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d703-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6d703-112"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d703-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6d703-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d703-113">Library</span></span><br/> | <dl> <span data-ttu-id="6d703-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6d703-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d703-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d703-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d703-116">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="6d703-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

