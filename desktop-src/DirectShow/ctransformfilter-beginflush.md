---
description: La méthode BeginFlush commence une opération de vidage.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Méthode CTransformFilter. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520832"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="85424-103">Méthode CTransformFilter. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="85424-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="85424-104">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="85424-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="85424-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85424-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="85424-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85424-106">Parameters</span></span>

<span data-ttu-id="85424-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="85424-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85424-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85424-108">Return value</span></span>

<span data-ttu-id="85424-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85424-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85424-110">Notes</span><span class="sxs-lookup"><span data-stu-id="85424-110">Remarks</span></span>

<span data-ttu-id="85424-111">Au démarrage d’une opération de vidage, la méthode [**CTransformInputPin :: BeginFlush**](ctransforminputpin-beginflush.md) de la broche d’entrée appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="85424-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="85424-112">Cette méthode passe l' `BeginFlush` appel en aval.</span><span class="sxs-lookup"><span data-stu-id="85424-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="85424-113">Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente pendant une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="85424-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="85424-114">Cela peut être effectué dans la `BeginFlush` méthode ou dans la méthode [**EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="85424-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="85424-115">Toutefois, Notez que les appels à `BeginFlush` ne sont pas synchronisés avec le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="85424-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="85424-116">Si la `BeginFlush` méthode ignore les données mises en file d’attente, le filtre doit veiller à ne pas traiter davantage de données entre les `BeginFlush` appels de **EndFlush** et.</span><span class="sxs-lookup"><span data-stu-id="85424-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="85424-117">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="85424-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85424-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85424-118">Requirements</span></span>



| <span data-ttu-id="85424-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85424-119">Requirement</span></span> | <span data-ttu-id="85424-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="85424-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85424-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="85424-121">Header</span></span><br/>  | <dl> <span data-ttu-id="85424-122"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85424-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="85424-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85424-123">Library</span></span><br/> | <dl> <span data-ttu-id="85424-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="85424-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85424-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85424-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85424-126">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="85424-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




