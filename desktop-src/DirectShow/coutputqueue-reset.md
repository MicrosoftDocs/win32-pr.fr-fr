---
description: La méthode reset réinitialise l’objet afin qu’il puisse recevoir plus de données.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: COutputQueue. Reset, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535854"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="545c7-103">COutputQueue. Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="545c7-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="545c7-104">La `Reset` méthode réinitialise l’objet afin qu’il puisse recevoir plus de données.</span><span class="sxs-lookup"><span data-stu-id="545c7-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="545c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="545c7-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="545c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="545c7-106">Parameters</span></span>

<span data-ttu-id="545c7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="545c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="545c7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="545c7-108">Return value</span></span>

<span data-ttu-id="545c7-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="545c7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="545c7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="545c7-110">Remarks</span></span>

<span data-ttu-id="545c7-111">Cette méthode réinitialise la variable de membre [**COutputQueue :: m \_ HR**](coutputqueue-m-hr.md) sur S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="545c7-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="545c7-112">L’objet peut recevoir à nouveau des exemples de supports. par exemple, après une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="545c7-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="545c7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="545c7-113">Requirements</span></span>



| <span data-ttu-id="545c7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="545c7-114">Requirement</span></span> | <span data-ttu-id="545c7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="545c7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="545c7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="545c7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="545c7-117"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="545c7-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="545c7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="545c7-118">Library</span></span><br/> | <dl> <span data-ttu-id="545c7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="545c7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545c7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="545c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545c7-121">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="545c7-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




