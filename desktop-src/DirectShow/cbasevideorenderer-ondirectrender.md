---
description: La méthode OnDirectRender collecte les informations de minutage qui contrôlent la synchronisation et le contrôle de qualité.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Méthode CBaseVideoRenderer. OnDirectRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532575"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="f7b22-103">Méthode CBaseVideoRenderer. OnDirectRender</span><span class="sxs-lookup"><span data-stu-id="f7b22-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="f7b22-104">La méthode **OnDirectRender** collecte les informations de minutage qui contrôlent la synchronisation et le contrôle de qualité.</span><span class="sxs-lookup"><span data-stu-id="f7b22-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b22-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="f7b22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7b22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b22-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="f7b22-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b22-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="f7b22-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b22-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7b22-109">Return value</span></span>

<span data-ttu-id="f7b22-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f7b22-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7b22-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7b22-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b22-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f7b22-112">Remarks</span></span>

<span data-ttu-id="f7b22-113">Appelez cette méthode à la place de [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) et [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="f7b22-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="f7b22-114">Cette méthode est utilisée par le convertisseur vidéo DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f7b22-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b22-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7b22-115">Requirements</span></span>



| <span data-ttu-id="f7b22-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b22-116">Requirement</span></span> | <span data-ttu-id="f7b22-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b22-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b22-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7b22-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f7b22-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7b22-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7b22-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7b22-120">Library</span></span><br/> | <dl> <span data-ttu-id="f7b22-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f7b22-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b22-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7b22-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b22-123">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f7b22-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




