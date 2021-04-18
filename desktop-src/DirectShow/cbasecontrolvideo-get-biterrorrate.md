---
description: La \_ méthode obtenir BitErrorRate récupère un taux d’erreur de bit approximatif pour la vidéo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Méthode CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532846"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="66a78-103">Méthode CBaseControlVideo. obten \_ BitErrorRate</span><span class="sxs-lookup"><span data-stu-id="66a78-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="66a78-104">La `get_BitErrorRate` méthode récupère un taux d’erreur de bit approximatif pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="66a78-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66a78-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="66a78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a78-107">*pBitErrorRate*</span><span class="sxs-lookup"><span data-stu-id="66a78-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="66a78-108">Pointeur vers le taux d’erreur binaire (une erreur pour approximativement ce nombre de bits).</span><span class="sxs-lookup"><span data-stu-id="66a78-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a78-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66a78-109">Return value</span></span>

<span data-ttu-id="66a78-110">Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="66a78-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="66a78-111">Notes</span><span class="sxs-lookup"><span data-stu-id="66a78-111">Remarks</span></span>

<span data-ttu-id="66a78-112">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) .</span><span class="sxs-lookup"><span data-stu-id="66a78-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="66a78-113">Elle appelle la méthode [**CBaseControlVideo :: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuelle pure pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="66a78-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a78-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66a78-114">Requirements</span></span>



| <span data-ttu-id="66a78-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66a78-115">Requirement</span></span> | <span data-ttu-id="66a78-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="66a78-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a78-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="66a78-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66a78-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66a78-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66a78-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66a78-119">Library</span></span><br/> | <dl> <span data-ttu-id="66a78-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66a78-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a78-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66a78-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a78-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="66a78-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




