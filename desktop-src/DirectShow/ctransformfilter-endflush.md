---
description: 'Méthode CTransformFilter. EndFlush : la méthode EndFlush termine une opération de vidage.'
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
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085058"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="4f2c8-103">Méthode CTransformFilter. EndFlush</span><span class="sxs-lookup"><span data-stu-id="4f2c8-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="4f2c8-104">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="4f2c8-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f2c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f2c8-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="4f2c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f2c8-106">Parameters</span></span>

<span data-ttu-id="4f2c8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4f2c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f2c8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f2c8-108">Return value</span></span>

<span data-ttu-id="4f2c8-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f2c8-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f2c8-110">Notes </span><span class="sxs-lookup"><span data-stu-id="4f2c8-110">Remarks</span></span>

<span data-ttu-id="4f2c8-111">À la fin d’une opération de vidage, la méthode [**CTransformInputPin :: EndFlush**](ctransforminputpin-endflush.md) de la broche d’entrée appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4f2c8-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="4f2c8-112">Cette méthode passe l' `EndFlush` appel en aval.</span><span class="sxs-lookup"><span data-stu-id="4f2c8-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="4f2c8-113">Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente avant d’envoyer l' `EndFlush` appel en aval.</span><span class="sxs-lookup"><span data-stu-id="4f2c8-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="4f2c8-114">Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="4f2c8-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f2c8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f2c8-115">Requirements</span></span>



| <span data-ttu-id="4f2c8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f2c8-116">Requirement</span></span> | <span data-ttu-id="4f2c8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f2c8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2c8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f2c8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4f2c8-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f2c8-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4f2c8-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f2c8-120">Library</span></span><br/> | <dl> <span data-ttu-id="4f2c8-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4f2c8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f2c8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f2c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2c8-123">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="4f2c8-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




