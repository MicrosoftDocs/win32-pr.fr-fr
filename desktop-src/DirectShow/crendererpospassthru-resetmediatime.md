---
description: La méthode ResetMediaTime réinitialise les horodatages mis en cache à zéro.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Méthode CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540421"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="5ae9a-103">Méthode CRendererPosPassThru. ResetMediaTime</span><span class="sxs-lookup"><span data-stu-id="5ae9a-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="5ae9a-104">La `ResetMediaTime` méthode réinitialise les horodatages mis en cache à zéro.</span><span class="sxs-lookup"><span data-stu-id="5ae9a-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae9a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ae9a-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="5ae9a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ae9a-106">Parameters</span></span>

<span data-ttu-id="5ae9a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ae9a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ae9a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ae9a-108">Return value</span></span>

<span data-ttu-id="5ae9a-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ae9a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae9a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5ae9a-110">Remarks</span></span>

<span data-ttu-id="5ae9a-111">Le filtre doit appeler cette méthode chaque fois que les horodatages mis en cache par la méthode [**CRendererPosPassThru :: RegisterMediaTime**](crendererpospassthru-registermediatime.md) deviennent non valides.</span><span class="sxs-lookup"><span data-stu-id="5ae9a-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="5ae9a-112">En particulier, il doit appeler cette méthode en réponse aux méthodes [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) et [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="5ae9a-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="5ae9a-113">Une fois cette méthode appelée, la méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) retourne zéro pour les heures de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="5ae9a-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae9a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ae9a-114">Requirements</span></span>



| <span data-ttu-id="5ae9a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ae9a-115">Requirement</span></span> | <span data-ttu-id="5ae9a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ae9a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae9a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ae9a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5ae9a-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae9a-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ae9a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ae9a-119">Library</span></span><br/> | <dl> <span data-ttu-id="5ae9a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae9a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




