---
description: La méthode IsStopped détermine si le filtre contenant ce code PIN est arrêté.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Méthode CBasePin. IsStopped (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525640"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="e109c-103">Méthode CBasePin. IsStopped</span><span class="sxs-lookup"><span data-stu-id="e109c-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="e109c-104">La `IsStopped` méthode détermine si le filtre contenant ce code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e109c-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="e109c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e109c-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="e109c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e109c-106">Parameters</span></span>

<span data-ttu-id="e109c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e109c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e109c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e109c-108">Return value</span></span>

<span data-ttu-id="e109c-109">Retourne la **valeur true** si le filtre est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e109c-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="e109c-110">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="e109c-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e109c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e109c-111">Remarks</span></span>

<span data-ttu-id="e109c-112">N’appelez pas cette méthode à partir de dans la méthode du constructeur **CBasePin** , car le filtre n’est peut-être pas encore initialisé.</span><span class="sxs-lookup"><span data-stu-id="e109c-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="e109c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e109c-113">Requirements</span></span>



| <span data-ttu-id="e109c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e109c-114">Requirement</span></span> | <span data-ttu-id="e109c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e109c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e109c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e109c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e109c-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e109c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e109c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e109c-118">Library</span></span><br/> | <dl> <span data-ttu-id="e109c-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e109c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e109c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e109c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e109c-121">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="e109c-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




