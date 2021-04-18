---
description: La méthode OnThreadDestroy est appelée lorsque le thread de streaming est sur le point de quitter.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Méthode CSourceStream. OnThreadDestroy (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528885"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="3aaff-103">Méthode CSourceStream. OnThreadDestroy</span><span class="sxs-lookup"><span data-stu-id="3aaff-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="3aaff-104">La `OnThreadDestroy` méthode est appelée lorsque le thread de diffusion en continu est sur le point de quitter.</span><span class="sxs-lookup"><span data-stu-id="3aaff-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aaff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aaff-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="3aaff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aaff-106">Parameters</span></span>

<span data-ttu-id="3aaff-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3aaff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aaff-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3aaff-108">Return value</span></span>

<span data-ttu-id="3aaff-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3aaff-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aaff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3aaff-110">Remarks</span></span>

<span data-ttu-id="3aaff-111">La procédure de thread, [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md), appelle cette méthode avant de quitter.</span><span class="sxs-lookup"><span data-stu-id="3aaff-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="3aaff-112">La méthode n’a aucun effet dans la classe de base ; elle est disponible pour la substitution de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="3aaff-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="3aaff-113">Si la classe dérivée retourne un code d’erreur, le thread se termine avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="3aaff-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aaff-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aaff-114">Requirements</span></span>



| <span data-ttu-id="3aaff-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aaff-115">Requirement</span></span> | <span data-ttu-id="3aaff-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aaff-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aaff-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="3aaff-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3aaff-118"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aaff-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3aaff-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3aaff-119">Library</span></span><br/> | <dl> <span data-ttu-id="3aaff-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3aaff-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aaff-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aaff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aaff-122">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="3aaff-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




