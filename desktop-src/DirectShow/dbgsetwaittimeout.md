---
description: Définit la valeur du délai d’attente du débogage. Ignoré dans les builds de vente au détail.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: DbgSetWaitTimeout, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539617"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="cc239-104">DbgSetWaitTimeout fonction)</span><span class="sxs-lookup"><span data-stu-id="cc239-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="cc239-105">Définit la valeur du délai d’attente du débogage.</span><span class="sxs-lookup"><span data-stu-id="cc239-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="cc239-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="cc239-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc239-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc239-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="cc239-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc239-109">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="cc239-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="cc239-110">Valeur du délai d’attente en millisecondes, ou infinie pour attendre indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="cc239-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc239-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc239-111">Return value</span></span>

<span data-ttu-id="cc239-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cc239-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc239-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cc239-113">Remarks</span></span>

<span data-ttu-id="cc239-114">Dans les versions Debug, les fonctions [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) et [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) utilisent cette valeur comme intervalle de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc239-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc239-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc239-115">Requirements</span></span>



| <span data-ttu-id="cc239-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc239-116">Requirement</span></span> | <span data-ttu-id="cc239-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc239-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc239-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc239-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc239-119"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc239-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc239-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc239-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc239-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cc239-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc239-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc239-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc239-123">Fonctions de débogage d’attente</span><span class="sxs-lookup"><span data-stu-id="cc239-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




