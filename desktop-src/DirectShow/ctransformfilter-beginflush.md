---
description: 'Méthode CTransformFilter. BeginFlush : la méthode BeginFlush commence une opération de vidage.'
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
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085157"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="c62a8-103">Méthode CTransformFilter. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="c62a8-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="c62a8-104">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="c62a8-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c62a8-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="c62a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c62a8-106">Parameters</span></span>

<span data-ttu-id="c62a8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c62a8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c62a8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c62a8-108">Return value</span></span>

<span data-ttu-id="c62a8-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c62a8-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62a8-110">Notes </span><span class="sxs-lookup"><span data-stu-id="c62a8-110">Remarks</span></span>

<span data-ttu-id="c62a8-111">Au démarrage d’une opération de vidage, la méthode [**CTransformInputPin :: BeginFlush**](ctransforminputpin-beginflush.md) de la broche d’entrée appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c62a8-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="c62a8-112">Cette méthode passe l' `BeginFlush` appel en aval.</span><span class="sxs-lookup"><span data-stu-id="c62a8-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="c62a8-113">Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente pendant une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="c62a8-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="c62a8-114">Cela peut être effectué dans la `BeginFlush` méthode ou dans la méthode [**EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="c62a8-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="c62a8-115">Toutefois, Notez que les appels à `BeginFlush` ne sont pas synchronisés avec le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="c62a8-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="c62a8-116">Si la `BeginFlush` méthode ignore les données mises en file d’attente, le filtre doit veiller à ne pas traiter davantage de données entre les `BeginFlush` appels de **EndFlush** et.</span><span class="sxs-lookup"><span data-stu-id="c62a8-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="c62a8-117">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c62a8-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c62a8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c62a8-118">Requirements</span></span>



| <span data-ttu-id="c62a8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c62a8-119">Requirement</span></span> | <span data-ttu-id="c62a8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c62a8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62a8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c62a8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c62a8-122"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c62a8-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c62a8-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c62a8-123">Library</span></span><br/> | <dl> <span data-ttu-id="c62a8-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c62a8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62a8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c62a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62a8-126">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="c62a8-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




