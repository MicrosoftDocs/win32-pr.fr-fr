---
description: La méthode Run bascule en mode Running afin que les commandes qui sont différées par l’heure du flux de temps puissent être exécutées.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: CCmdQueue. Run, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528774"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="57f73-103">CCmdQueue. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="57f73-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="57f73-104">La `Run` méthode bascule en mode d’exécution afin que les commandes qui sont différées par l’heure du flux de temps puissent être exécutées.</span><span class="sxs-lookup"><span data-stu-id="57f73-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57f73-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="57f73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57f73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f73-107">*tStreamTimeOffset*</span><span class="sxs-lookup"><span data-stu-id="57f73-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="57f73-108">Heure du décalage.</span><span class="sxs-lookup"><span data-stu-id="57f73-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f73-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57f73-109">Return value</span></span>

<span data-ttu-id="57f73-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="57f73-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="57f73-111">Notes</span><span class="sxs-lookup"><span data-stu-id="57f73-111">Remarks</span></span>

<span data-ttu-id="57f73-112">En mode exécution, le mappage flux-temps-durée-présentation est connu.</span><span class="sxs-lookup"><span data-stu-id="57f73-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f73-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57f73-113">Requirements</span></span>



| <span data-ttu-id="57f73-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57f73-114">Requirement</span></span> | <span data-ttu-id="57f73-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="57f73-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57f73-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="57f73-116">Header</span></span><br/>  | <dl> <span data-ttu-id="57f73-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57f73-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57f73-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="57f73-118">Library</span></span><br/> | <dl> <span data-ttu-id="57f73-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="57f73-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f73-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57f73-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f73-121">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="57f73-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




