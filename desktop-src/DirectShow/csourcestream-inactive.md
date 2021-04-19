---
description: 'La méthode inactive indique au code confidentiel que le filtre n’est plus actif. Cette méthode remplace la méthode CBasePin :: inactive. Si le thread de diffusion en continu est actif, cette méthode l’arrête et attend que le thread se termine.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Méthode CSourceStream. inactive (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537508"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="a3b03-105">CSourceStream. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="a3b03-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="a3b03-106">La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="a3b03-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="a3b03-107">Cette méthode remplace la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b03-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="a3b03-108">Si le thread de diffusion en continu est actif, cette méthode l’arrête et attend que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="a3b03-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b03-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3b03-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="a3b03-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3b03-110">Parameters</span></span>

<span data-ttu-id="a3b03-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3b03-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3b03-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3b03-112">Return value</span></span>

<span data-ttu-id="a3b03-113">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3b03-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b03-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3b03-114">Requirements</span></span>



| <span data-ttu-id="a3b03-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3b03-115">Requirement</span></span> | <span data-ttu-id="a3b03-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3b03-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b03-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3b03-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3b03-118"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3b03-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a3b03-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3b03-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3b03-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a3b03-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3b03-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3b03-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b03-122">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="a3b03-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




