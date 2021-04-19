---
description: Récupère le handle d’événement. Cet opérateur n’est pas pris en charge en tant que L-value.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Méthode de HANDLE CAMEvent. Operator (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72193e89f415aabebfea4288fcdb986ccf8d73bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525434"
---
# <a name="cameventoperator-handle-method"></a><span data-ttu-id="49e36-104">CAMEvent. Operator, méthode de HANDLE</span><span class="sxs-lookup"><span data-stu-id="49e36-104">CAMEvent.operator HANDLE method</span></span>

<span data-ttu-id="49e36-105">Récupère le handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="49e36-105">Retrieves the event handle.</span></span> <span data-ttu-id="49e36-106">Cet opérateur n’est pas pris en charge en tant que L-value.</span><span class="sxs-lookup"><span data-stu-id="49e36-106">This operator is not supported as an L-value.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e36-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49e36-107">Syntax</span></span>


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a><span data-ttu-id="49e36-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49e36-108">Parameters</span></span>

<span data-ttu-id="49e36-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="49e36-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49e36-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49e36-110">Return value</span></span>

<span data-ttu-id="49e36-111">Retourne la variable de membre [**CAMEvent :: m \_ hEvent**](camevent-m-hevent.md) .</span><span class="sxs-lookup"><span data-stu-id="49e36-111">Returns the [**CAMEvent::m\_hEvent**](camevent-m-hevent.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e36-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49e36-112">Requirements</span></span>



| <span data-ttu-id="49e36-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49e36-113">Requirement</span></span> | <span data-ttu-id="49e36-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="49e36-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e36-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="49e36-115">Header</span></span><br/>  | <dl> <span data-ttu-id="49e36-116"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49e36-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="49e36-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49e36-117">Library</span></span><br/> | <dl> <span data-ttu-id="49e36-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49e36-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e36-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49e36-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e36-120">**CAMEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="49e36-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




