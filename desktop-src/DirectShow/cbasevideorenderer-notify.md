---
description: La méthode Notify reçoit une notification indiquant qu’une modification de qualité est demandée.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: CBaseVideoRenderer. Notify, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532817"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="61ccf-103">CBaseVideoRenderer. Notify, méthode</span><span class="sxs-lookup"><span data-stu-id="61ccf-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="61ccf-104">La `Notify` méthode reçoit une notification indiquant qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="61ccf-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ccf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61ccf-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="61ccf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61ccf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ccf-107">*pSelf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61ccf-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ccf-108">Pointeur vers le filtre qui envoie la notification de qualité.</span><span class="sxs-lookup"><span data-stu-id="61ccf-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="61ccf-109">*q* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61ccf-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ccf-110">Structure de notification de qualité.</span><span class="sxs-lookup"><span data-stu-id="61ccf-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61ccf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61ccf-111">Return value</span></span>

<span data-ttu-id="61ccf-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61ccf-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61ccf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="61ccf-113">Remarks</span></span>

<span data-ttu-id="61ccf-114">Cette fonction membre implémente la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) sur le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="61ccf-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="61ccf-115">Elle est appelée, généralement par le gestionnaire de graphe de filtre, lorsque la qualité doit être coupée.</span><span class="sxs-lookup"><span data-stu-id="61ccf-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="61ccf-116">Cela peut se produire lorsque la qualité de la lecture audio a été augmentée jusqu’au point que la qualité de la lecture de la vidéo doit être réduite.</span><span class="sxs-lookup"><span data-stu-id="61ccf-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="61ccf-117">`Notify` définit le membre de données **m \_ trThrottle** sur une valeur de délai à insérer entre les frames par [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="61ccf-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61ccf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61ccf-118">Requirements</span></span>



| <span data-ttu-id="61ccf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61ccf-119">Requirement</span></span> | <span data-ttu-id="61ccf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="61ccf-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ccf-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="61ccf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="61ccf-122"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61ccf-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61ccf-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61ccf-123">Library</span></span><br/> | <dl> <span data-ttu-id="61ccf-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="61ccf-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61ccf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61ccf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ccf-126">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="61ccf-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




