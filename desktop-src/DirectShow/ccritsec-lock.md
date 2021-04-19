---
description: La méthode Lock verrouille l’objet de section critique.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: CCritSec. Lock, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541374"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="f9c44-103">CCritSec. Lock, méthode</span><span class="sxs-lookup"><span data-stu-id="f9c44-103">CCritSec.Lock method</span></span>

<span data-ttu-id="f9c44-104">La méthode **Lock** verrouille l’objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="f9c44-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c44-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9c44-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="f9c44-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9c44-106">Parameters</span></span>

<span data-ttu-id="f9c44-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9c44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9c44-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9c44-108">Return value</span></span>

<span data-ttu-id="f9c44-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f9c44-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c44-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f9c44-110">Remarks</span></span>

<span data-ttu-id="f9c44-111">Cette méthode appelle la fonction [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="f9c44-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="f9c44-112">Appelez la fonction membre [**CCritSec :: Unlock**](ccritsec-unlock.md) pour déverrouiller la section critique.</span><span class="sxs-lookup"><span data-stu-id="f9c44-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="f9c44-113">Vous pouvez effectuer plusieurs appels à la méthode **Lock** sur le même thread. Veillez à appeler **Unlock** un nombre de fois correspondant.</span><span class="sxs-lookup"><span data-stu-id="f9c44-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="f9c44-114">Si l’objet est déjà verrouillé par un autre thread, la méthode **CCritSec :: Lock** est bloquée jusqu’à ce que l’objet soit libéré, ou jusqu’à ce qu’une exception de blocage possible se produise.</span><span class="sxs-lookup"><span data-stu-id="f9c44-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c44-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9c44-115">Requirements</span></span>



| <span data-ttu-id="f9c44-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9c44-116">Requirement</span></span> | <span data-ttu-id="f9c44-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9c44-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c44-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9c44-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f9c44-119"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9c44-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f9c44-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9c44-120">Library</span></span><br/> | <dl> <span data-ttu-id="f9c44-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9c44-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c44-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9c44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c44-123">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="f9c44-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

