---
description: La méthode CheckTime détermine si une heure spécifiée est due.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Méthode CCmdQueue. CheckTime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537126"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="e0567-103">Méthode CCmdQueue. CheckTime</span><span class="sxs-lookup"><span data-stu-id="e0567-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="e0567-104">La `CheckTime` méthode détermine si une heure spécifiée est due.</span><span class="sxs-lookup"><span data-stu-id="e0567-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0567-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0567-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="e0567-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0567-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0567-107">*time*</span><span class="sxs-lookup"><span data-stu-id="e0567-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="e0567-108">Durée à vérifier.</span><span class="sxs-lookup"><span data-stu-id="e0567-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="e0567-109">*bStream*</span><span class="sxs-lookup"><span data-stu-id="e0567-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="e0567-110">**True** si le paramètre de *temps* est une valeur de flux de temps ; **False** si *Time* est une valeur au moment de la présentation.</span><span class="sxs-lookup"><span data-stu-id="e0567-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0567-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0567-111">Return value</span></span>

<span data-ttu-id="e0567-112">Retourne la **valeur true** si l’heure spécifiée n’est pas encore passée.</span><span class="sxs-lookup"><span data-stu-id="e0567-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0567-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0567-113">Requirements</span></span>



| <span data-ttu-id="e0567-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0567-114">Requirement</span></span> | <span data-ttu-id="e0567-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0567-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0567-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0567-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0567-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0567-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0567-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e0567-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0567-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e0567-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0567-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0567-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0567-121">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="e0567-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




