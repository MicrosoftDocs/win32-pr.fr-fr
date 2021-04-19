---
description: La méthode OnThreadCreate est appelée lors de l’initialisation du thread de streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Méthode CSourceStream. OnThreadCreate (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539952"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="d9c82-103">Méthode CSourceStream. OnThreadCreate</span><span class="sxs-lookup"><span data-stu-id="d9c82-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="d9c82-104">La `OnThreadCreate` méthode est appelée lorsque le thread de streaming est initialisé.</span><span class="sxs-lookup"><span data-stu-id="d9c82-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9c82-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="d9c82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9c82-106">Parameters</span></span>

<span data-ttu-id="d9c82-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d9c82-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9c82-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9c82-108">Return value</span></span>

<span data-ttu-id="d9c82-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9c82-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9c82-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d9c82-110">Remarks</span></span>

<span data-ttu-id="d9c82-111">La procédure de thread, [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md), appelle cette méthode lorsqu’elle reçoit pour la première fois une demande [**CSourceStream :: init**](csourcestream-init.md) .</span><span class="sxs-lookup"><span data-stu-id="d9c82-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="d9c82-112">La méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="d9c82-112">The method does nothing in the base class.</span></span> <span data-ttu-id="d9c82-113">La classe dérivée peut substituer cette méthode pour effectuer des initialisations de thread.</span><span class="sxs-lookup"><span data-stu-id="d9c82-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="d9c82-114">Si la classe dérivée retourne un code d’erreur, le thread se termine avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="d9c82-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c82-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9c82-115">Requirements</span></span>



| <span data-ttu-id="d9c82-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9c82-116">Requirement</span></span> | <span data-ttu-id="d9c82-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9c82-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c82-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9c82-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d9c82-119"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9c82-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d9c82-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9c82-120">Library</span></span><br/> | <dl> <span data-ttu-id="d9c82-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d9c82-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c82-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9c82-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c82-123">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="d9c82-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




