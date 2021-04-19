---
description: La méthode StopStreaming interrompt la diffusion en continu lorsque le filtre sort de l’État en cours d’exécution.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Méthode CBaseRenderer. StopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525644"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="05c1d-103">Méthode CBaseRenderer. StopStreaming</span><span class="sxs-lookup"><span data-stu-id="05c1d-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="05c1d-104">La `StopStreaming` méthode interrompt la diffusion en continu lorsque le filtre sort de l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="05c1d-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05c1d-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="05c1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05c1d-106">Parameters</span></span>

<span data-ttu-id="05c1d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="05c1d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05c1d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05c1d-108">Return value</span></span>

<span data-ttu-id="05c1d-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05c1d-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c1d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="05c1d-110">Remarks</span></span>

<span data-ttu-id="05c1d-111">Cette méthode appelle la méthode [**CBaseRenderer :: OnStopStreaming**](cbaserenderer-onstopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="05c1d-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="05c1d-112">Cette méthode ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="05c1d-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c1d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05c1d-113">Requirements</span></span>



| <span data-ttu-id="05c1d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05c1d-114">Requirement</span></span> | <span data-ttu-id="05c1d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="05c1d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c1d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="05c1d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="05c1d-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05c1d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05c1d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05c1d-118">Library</span></span><br/> | <dl> <span data-ttu-id="05c1d-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05c1d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c1d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05c1d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c1d-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="05c1d-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




