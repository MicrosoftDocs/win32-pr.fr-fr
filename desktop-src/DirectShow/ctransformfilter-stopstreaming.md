---
description: La méthode StopStreaming est appelée lorsque le filtre bascule à l’état arrêté.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Méthode CTransformFilter. StopStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541619"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="54044-103">Méthode CTransformFilter. StopStreaming</span><span class="sxs-lookup"><span data-stu-id="54044-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="54044-104">La `StopStreaming` méthode est appelée lorsque le filtre bascule à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="54044-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="54044-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54044-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="54044-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54044-106">Parameters</span></span>

<span data-ttu-id="54044-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="54044-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54044-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54044-108">Return value</span></span>

<span data-ttu-id="54044-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54044-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="54044-110">Notes</span><span class="sxs-lookup"><span data-stu-id="54044-110">Remarks</span></span>

<span data-ttu-id="54044-111">Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="54044-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="54044-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54044-112">Requirements</span></span>



| <span data-ttu-id="54044-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54044-113">Requirement</span></span> | <span data-ttu-id="54044-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="54044-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54044-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="54044-115">Header</span></span><br/>  | <dl> <span data-ttu-id="54044-116"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54044-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="54044-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54044-117">Library</span></span><br/> | <dl> <span data-ttu-id="54044-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="54044-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54044-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54044-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54044-120">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="54044-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




