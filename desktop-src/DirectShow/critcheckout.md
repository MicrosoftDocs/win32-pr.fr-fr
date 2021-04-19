---
description: Retourne la valeur FALSe si le thread actuel est le propriétaire de la section critique spécifiée.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: CritCheckOut, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523574"
---
# <a name="critcheckout-function"></a><span data-ttu-id="b7d40-103">CritCheckOut fonction)</span><span class="sxs-lookup"><span data-stu-id="b7d40-103">CritCheckOut function</span></span>

<span data-ttu-id="b7d40-104">Retourne la **valeur false** si le thread actuel est le propriétaire de la section critique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b7d40-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7d40-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="b7d40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7d40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d40-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="b7d40-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="b7d40-108">Pointeur vers une section critique [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d40-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d40-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7d40-109">Return value</span></span>

<span data-ttu-id="b7d40-110">Dans les versions Debug, retourne **false** si le thread actuel est le propriétaire de cette section critique, ou **true** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b7d40-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="b7d40-111">Dans les versions commerciales, retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="b7d40-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d40-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b7d40-112">Remarks</span></span>

<span data-ttu-id="b7d40-113">Cette fonction est l’inverse de la fonction [**CritCheckIn**](critcheckin.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d40-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="b7d40-114">Si **CritCheckIn** retourne la **valeur true**, **CritCheckOut** retourne la **valeur false**, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="b7d40-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d40-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7d40-115">Requirements</span></span>



| <span data-ttu-id="b7d40-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7d40-116">Requirement</span></span> | <span data-ttu-id="b7d40-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7d40-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d40-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7d40-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d40-119"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7d40-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b7d40-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7d40-120">Library</span></span><br/> | <dl> <span data-ttu-id="b7d40-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7d40-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d40-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7d40-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d40-123">Fonctions de débogage des sections critiques</span><span class="sxs-lookup"><span data-stu-id="b7d40-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




