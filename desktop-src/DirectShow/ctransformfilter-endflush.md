---
description: La méthode EndFlush termine une opération de vidage.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Méthode CTransformFilter. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534989"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="1a1d2-103">Méthode CTransformFilter. EndFlush</span><span class="sxs-lookup"><span data-stu-id="1a1d2-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="1a1d2-104">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a1d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a1d2-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1a1d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a1d2-106">Parameters</span></span>

<span data-ttu-id="1a1d2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a1d2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a1d2-108">Return value</span></span>

<span data-ttu-id="1a1d2-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a1d2-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a1d2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1a1d2-110">Remarks</span></span>

<span data-ttu-id="1a1d2-111">À la fin d’une opération de vidage, la méthode [**CTransformInputPin :: EndFlush**](ctransforminputpin-endflush.md) de la broche d’entrée appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="1a1d2-112">Cette méthode passe l' `EndFlush` appel en aval.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="1a1d2-113">Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente avant d’envoyer l' `EndFlush` appel en aval.</span><span class="sxs-lookup"><span data-stu-id="1a1d2-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="1a1d2-114">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1a1d2-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a1d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a1d2-115">Requirements</span></span>



| <span data-ttu-id="1a1d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a1d2-116">Requirement</span></span> | <span data-ttu-id="1a1d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a1d2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1d2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a1d2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1a1d2-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a1d2-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a1d2-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a1d2-120">Library</span></span><br/> | <dl> <span data-ttu-id="1a1d2-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a1d2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a1d2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a1d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1d2-123">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="1a1d2-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




