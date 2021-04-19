---
description: La méthode pause signale au thread de streaming qu’il devient actif.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Méthode CSourceStream. pause (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541296"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="202c8-103">CSourceStream. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="202c8-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="202c8-104">La `Pause` méthode signale au thread de streaming qu’il devient actif.</span><span class="sxs-lookup"><span data-stu-id="202c8-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="202c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="202c8-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="202c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="202c8-106">Parameters</span></span>

<span data-ttu-id="202c8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="202c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="202c8-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="202c8-108">Return value</span></span>

<span data-ttu-id="202c8-109">Retourne S \_ OK ou E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="202c8-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="202c8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="202c8-110">Remarks</span></span>

<span data-ttu-id="202c8-111">La méthode [**CSourceStream :: active**](csourcestream-active.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="202c8-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="202c8-112">Quand la méthode [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md) reçoit cette demande, elle appelle la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="202c8-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="202c8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="202c8-113">Requirements</span></span>



| <span data-ttu-id="202c8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="202c8-114">Requirement</span></span> | <span data-ttu-id="202c8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="202c8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202c8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="202c8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="202c8-117"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="202c8-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="202c8-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="202c8-118">Library</span></span><br/> | <dl> <span data-ttu-id="202c8-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="202c8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202c8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="202c8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202c8-121">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="202c8-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




