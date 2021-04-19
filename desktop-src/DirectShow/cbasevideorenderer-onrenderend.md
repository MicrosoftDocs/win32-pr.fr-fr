---
description: La méthode OnRenderEnd effectue un lissage pour les cas où le temps de rendu varie en raison des interruptions.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Méthode CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523475"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="ec42b-103">Méthode CBaseVideoRenderer. OnRenderEnd</span><span class="sxs-lookup"><span data-stu-id="ec42b-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="ec42b-104">La `OnRenderEnd` méthode effectue un lissage pour les cas où le temps de rendu varie en raison des interruptions.</span><span class="sxs-lookup"><span data-stu-id="ec42b-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec42b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec42b-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="ec42b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec42b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec42b-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="ec42b-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ec42b-108">Pointeur vers l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="ec42b-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec42b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec42b-109">Return value</span></span>

<span data-ttu-id="ec42b-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ec42b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec42b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ec42b-111">Remarks</span></span>

<span data-ttu-id="ec42b-112">Cette fonction membre doit être appelée juste après le dessin d’une image.</span><span class="sxs-lookup"><span data-stu-id="ec42b-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="ec42b-113">Cette fonction membre substitue [**CBaseRenderer :: OnRenderEnd**](cbaserenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="ec42b-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec42b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec42b-114">Requirements</span></span>



| <span data-ttu-id="ec42b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec42b-115">Requirement</span></span> | <span data-ttu-id="ec42b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec42b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec42b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec42b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ec42b-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec42b-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec42b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec42b-119">Library</span></span><br/> | <dl> <span data-ttu-id="ec42b-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec42b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec42b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec42b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec42b-122">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="ec42b-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




