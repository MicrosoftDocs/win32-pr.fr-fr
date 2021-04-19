---
description: La méthode Init Initialise le thread de streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Méthode CSourceStream.Init (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542643"
---
# <a name="csourcestreaminit-method"></a><span data-ttu-id="b0417-103">Méthode CSourceStream.Init</span><span class="sxs-lookup"><span data-stu-id="b0417-103">CSourceStream.Init method</span></span>

<span data-ttu-id="b0417-104">La `Init` méthode initialise le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="b0417-104">The `Init` method initializes the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0417-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0417-105">Syntax</span></span>


```C++
HRESULT Init();
```



## <a name="parameters"></a><span data-ttu-id="b0417-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0417-106">Parameters</span></span>

<span data-ttu-id="b0417-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b0417-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0417-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0417-108">Return value</span></span>

<span data-ttu-id="b0417-109">Retourne S \_ ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0417-109">Returns S\_OK, or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0417-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b0417-110">Remarks</span></span>

<span data-ttu-id="b0417-111">Cette méthode doit être la première demande de thread envoyée à la méthode [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="b0417-111">This method must be the first thread request sent to the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method.</span></span> <span data-ttu-id="b0417-112">La méthode [**CSourceStream :: active**](csourcestream-active.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b0417-112">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0417-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0417-113">Requirements</span></span>



| <span data-ttu-id="b0417-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0417-114">Requirement</span></span> | <span data-ttu-id="b0417-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0417-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0417-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0417-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b0417-117"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0417-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b0417-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0417-118">Library</span></span><br/> | <dl> <span data-ttu-id="b0417-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0417-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0417-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0417-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0417-121">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="b0417-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




