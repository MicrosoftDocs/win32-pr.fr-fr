---
description: La méthode StartStreaming est appelée lorsque le filtre passe à l’état suspendu.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Méthode CTransformFilter. StartStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543876"
---
# <a name="ctransformfilterstartstreaming-method"></a><span data-ttu-id="99523-103">Méthode CTransformFilter. StartStreaming</span><span class="sxs-lookup"><span data-stu-id="99523-103">CTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="99523-104">La `StartStreaming` méthode est appelée lorsque le filtre passe à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="99523-104">The `StartStreaming` method is called when the filter switches to the paused state.</span></span>

## <a name="syntax"></a><span data-ttu-id="99523-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99523-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="99523-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99523-106">Parameters</span></span>

<span data-ttu-id="99523-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="99523-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99523-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99523-108">Return value</span></span>

<span data-ttu-id="99523-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99523-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="99523-110">Notes</span><span class="sxs-lookup"><span data-stu-id="99523-110">Remarks</span></span>

<span data-ttu-id="99523-111">Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="99523-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="99523-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99523-112">Requirements</span></span>



| <span data-ttu-id="99523-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99523-113">Requirement</span></span> | <span data-ttu-id="99523-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="99523-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99523-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="99523-115">Header</span></span><br/>  | <dl> <span data-ttu-id="99523-116"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99523-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99523-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99523-117">Library</span></span><br/> | <dl> <span data-ttu-id="99523-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99523-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99523-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99523-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99523-120">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="99523-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




