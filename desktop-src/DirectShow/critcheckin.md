---
description: Retourne la valeur TRUE si le thread actuel est le propriétaire de la section critique spécifiée.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: CritCheckIn, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532593"
---
# <a name="critcheckin-function"></a><span data-ttu-id="75e9c-103">CritCheckIn fonction)</span><span class="sxs-lookup"><span data-stu-id="75e9c-103">CritCheckIn function</span></span>

<span data-ttu-id="75e9c-104">Retourne la **valeur true** si le thread actuel est le propriétaire de la section critique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="75e9c-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75e9c-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="75e9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75e9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e9c-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="75e9c-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="75e9c-108">Pointeur vers une section critique [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="75e9c-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e9c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75e9c-109">Return value</span></span>

<span data-ttu-id="75e9c-110">Dans les versions Debug, retourne la **valeur true** si le thread actuel est le propriétaire de cette section critique, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="75e9c-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="75e9c-111">Dans les versions commerciales, retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="75e9c-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e9c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="75e9c-112">Remarks</span></span>

<span data-ttu-id="75e9c-113">Cette fonction est particulièrement utile dans la macro [**Assert**](assert.md) pour tester si un thread possède un verrou donné.</span><span class="sxs-lookup"><span data-stu-id="75e9c-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="75e9c-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="75e9c-114">Examples</span></span>

<span data-ttu-id="75e9c-115">L’exemple de code suivant montre comment utiliser cette fonction :</span><span class="sxs-lookup"><span data-stu-id="75e9c-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="75e9c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75e9c-116">Requirements</span></span>



| <span data-ttu-id="75e9c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75e9c-117">Requirement</span></span> | <span data-ttu-id="75e9c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="75e9c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e9c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="75e9c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="75e9c-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75e9c-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="75e9c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75e9c-121">Library</span></span><br/> | <dl> <span data-ttu-id="75e9c-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="75e9c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e9c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75e9c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e9c-124">Fonctions de débogage des sections critiques</span><span class="sxs-lookup"><span data-stu-id="75e9c-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




