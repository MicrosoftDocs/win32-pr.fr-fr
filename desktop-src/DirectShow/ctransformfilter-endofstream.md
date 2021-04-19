---
description: La méthode EndOfStream indique au filtre qu’aucune donnée supplémentaire n’est attendue à partir de la broche d’entrée.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Méthode CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526044"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="3f491-103">Méthode CTransformFilter. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="3f491-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="3f491-104">La `EndOfStream` méthode informe le filtre qu’aucune donnée supplémentaire n’est attendue à partir de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3f491-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f491-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f491-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="3f491-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f491-106">Parameters</span></span>

<span data-ttu-id="3f491-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3f491-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f491-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f491-108">Return value</span></span>

<span data-ttu-id="3f491-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f491-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f491-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3f491-110">Remarks</span></span>

<span data-ttu-id="3f491-111">La méthode [**CTransformInputPin :: EndOfStream**](ctransforminputpin-endofstream.md) du code confidentiel d’entrée appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3f491-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="3f491-112">Cette méthode fournit la notification de fin de flux en aval.</span><span class="sxs-lookup"><span data-stu-id="3f491-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="3f491-113">Si la classe dérivée utilise un thread de travail pour fournir des exemples de média, elle doit substituer cette méthode et mettre en file d’attente la notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="3f491-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f491-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f491-114">Requirements</span></span>



| <span data-ttu-id="3f491-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f491-115">Requirement</span></span> | <span data-ttu-id="3f491-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f491-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f491-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f491-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3f491-118"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f491-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3f491-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f491-119">Library</span></span><br/> | <dl> <span data-ttu-id="3f491-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3f491-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f491-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f491-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f491-122">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="3f491-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




