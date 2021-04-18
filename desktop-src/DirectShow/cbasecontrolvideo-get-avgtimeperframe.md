---
description: La \_ méthode obtenir AvgTimePerFrame récupère le temps moyen par frame.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Méthode CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540264"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="00bb1-103">Méthode CBaseControlVideo. obten \_ AvgTimePerFrame</span><span class="sxs-lookup"><span data-stu-id="00bb1-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="00bb1-104">La `get_AvgTimePerFrame` méthode récupère le temps moyen par frame.</span><span class="sxs-lookup"><span data-stu-id="00bb1-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="00bb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00bb1-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="00bb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00bb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00bb1-107">*pAvgTimePerFrame*</span><span class="sxs-lookup"><span data-stu-id="00bb1-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="00bb1-108">Pointeur vers le temps moyen par frame.</span><span class="sxs-lookup"><span data-stu-id="00bb1-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00bb1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00bb1-109">Return value</span></span>

<span data-ttu-id="00bb1-110">Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="00bb1-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="00bb1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="00bb1-111">Remarks</span></span>

<span data-ttu-id="00bb1-112">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) .</span><span class="sxs-lookup"><span data-stu-id="00bb1-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="00bb1-113">Elle appelle la fonction membre pure [**CBaseControlVideo :: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="00bb1-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="00bb1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00bb1-114">Requirements</span></span>



| <span data-ttu-id="00bb1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00bb1-115">Requirement</span></span> | <span data-ttu-id="00bb1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="00bb1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00bb1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="00bb1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="00bb1-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00bb1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00bb1-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00bb1-119">Library</span></span><br/> | <dl> <span data-ttu-id="00bb1-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00bb1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00bb1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00bb1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00bb1-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="00bb1-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




