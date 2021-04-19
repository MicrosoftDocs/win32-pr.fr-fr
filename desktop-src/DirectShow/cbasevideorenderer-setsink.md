---
description: La méthode SetSink définit l’objet IQualityControl qui recevra les messages de qualité.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Méthode CBaseVideoRenderer. SetSink (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530414"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="b3ae4-103">Méthode CBaseVideoRenderer. SetSink</span><span class="sxs-lookup"><span data-stu-id="b3ae4-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="b3ae4-104">La `SetSink` méthode définit l’objet [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) qui recevra les messages de qualité.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ae4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3ae4-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="b3ae4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3ae4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ae4-107">*piqc*</span><span class="sxs-lookup"><span data-stu-id="b3ae4-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="b3ae4-108">Pointeur vers l’objet [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) auquel les notifications doivent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ae4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3ae4-109">Return value</span></span>

<span data-ttu-id="b3ae4-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3ae4-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ae4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b3ae4-111">Remarks</span></span>

<span data-ttu-id="b3ae4-112">Cette fonction membre implémente la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) sur le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b3ae4-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ae4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3ae4-113">Requirements</span></span>



| <span data-ttu-id="b3ae4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3ae4-114">Requirement</span></span> | <span data-ttu-id="b3ae4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3ae4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ae4-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3ae4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b3ae4-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3ae4-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3ae4-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3ae4-118">Library</span></span><br/> | <dl> <span data-ttu-id="b3ae4-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3ae4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ae4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3ae4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ae4-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b3ae4-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




