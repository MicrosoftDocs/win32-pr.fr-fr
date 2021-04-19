---
description: La méthode OnThreadStartPlay est appelée au début de la méthode CSourceStream ::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Méthode CSourceStream. OnThreadStartPlay (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541586"
---
# <a name="csourcestreamonthreadstartplay-method"></a><span data-ttu-id="6cb15-103">Méthode CSourceStream. OnThreadStartPlay</span><span class="sxs-lookup"><span data-stu-id="6cb15-103">CSourceStream.OnThreadStartPlay method</span></span>

<span data-ttu-id="6cb15-104">La `OnThreadStartPlay` méthode est appelée au début de la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="6cb15-104">The `OnThreadStartPlay` method is called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cb15-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a><span data-ttu-id="6cb15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cb15-106">Parameters</span></span>

<span data-ttu-id="6cb15-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6cb15-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cb15-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cb15-108">Return value</span></span>

<span data-ttu-id="6cb15-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6cb15-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb15-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6cb15-110">Remarks</span></span>

<span data-ttu-id="6cb15-111">Cette méthode n’a aucun effet dans la classe de base ; elle est disponible pour la substitution de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="6cb15-111">This method does nothing in the base class; it is available for the derived class to override.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb15-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cb15-112">Requirements</span></span>



| <span data-ttu-id="6cb15-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cb15-113">Requirement</span></span> | <span data-ttu-id="6cb15-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cb15-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb15-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cb15-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6cb15-116"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb15-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6cb15-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cb15-117">Library</span></span><br/> | <dl> <span data-ttu-id="6cb15-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb15-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb15-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cb15-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb15-120">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="6cb15-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




