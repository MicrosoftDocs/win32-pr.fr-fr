---
description: La méthode SendNotifyWindow avertit le filtre amont du handle de fenêtre vidéo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Méthode CBaseRenderer. SendNotifyWindow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528686"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="16ccd-103">Méthode CBaseRenderer. SendNotifyWindow</span><span class="sxs-lookup"><span data-stu-id="16ccd-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="16ccd-104">La `SendNotifyWindow` méthode notifie le filtre amont du handle de fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="16ccd-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ccd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16ccd-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="16ccd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16ccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16ccd-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="16ccd-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="16ccd-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie du filtre en amont.</span><span class="sxs-lookup"><span data-stu-id="16ccd-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="16ccd-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="16ccd-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="16ccd-110">Handle vers la fenêtre vidéo, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="16ccd-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16ccd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16ccd-111">Return value</span></span>

<span data-ttu-id="16ccd-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="16ccd-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16ccd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="16ccd-113">Remarks</span></span>

<span data-ttu-id="16ccd-114">Si la broche de sortie du filtre en amont prend en charge l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , cette méthode l’envoie au code d’événement de la [**\_ \_ fenêtre de notification ce**](ec-notify-window.md) en même temps que le handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="16ccd-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="16ccd-115">Les convertisseurs vidéo peuvent substituer leurs méthodes [**CBaseRenderer :: CompleteConnect**](cbaserenderer-completeconnect.md) pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="16ccd-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="16ccd-116">Il fournit un mécanisme pour informer le filtre en amont du handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="16ccd-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="16ccd-117">Si vous procédez ainsi, substituez également la méthode [**CBaseRenderer :: BreakConnect**](cbaserenderer-breakconnect.md) et appelez `SendNotifyWindow` avec un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="16ccd-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="16ccd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16ccd-118">Requirements</span></span>



| <span data-ttu-id="16ccd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16ccd-119">Requirement</span></span> | <span data-ttu-id="16ccd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="16ccd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16ccd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="16ccd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="16ccd-122"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16ccd-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="16ccd-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16ccd-123">Library</span></span><br/> | <dl> <span data-ttu-id="16ccd-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16ccd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16ccd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16ccd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ccd-126">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="16ccd-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




