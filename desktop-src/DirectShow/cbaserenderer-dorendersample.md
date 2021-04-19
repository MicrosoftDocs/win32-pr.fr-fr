---
description: La méthode DoRenderSample restitue un exemple.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Méthode CBaseRenderer. DoRenderSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537753"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="f4869-103">Méthode CBaseRenderer. DoRenderSample</span><span class="sxs-lookup"><span data-stu-id="f4869-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="f4869-104">La `DoRenderSample` méthode restitue un exemple.</span><span class="sxs-lookup"><span data-stu-id="f4869-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4869-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4869-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f4869-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4869-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="f4869-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f4869-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f4869-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4869-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4869-109">Return value</span></span>

<span data-ttu-id="f4869-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4869-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4869-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f4869-111">Remarks</span></span>

<span data-ttu-id="f4869-112">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f4869-112">The derived class must implement this method.</span></span> <span data-ttu-id="f4869-113">Le comportement dépend entièrement du type de filtre implémenté.</span><span class="sxs-lookup"><span data-stu-id="f4869-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="f4869-114">Un convertisseur vidéo, par exemple, dessinerait l’image vidéo contenue dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f4869-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4869-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4869-115">Requirements</span></span>



| <span data-ttu-id="f4869-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4869-116">Requirement</span></span> | <span data-ttu-id="f4869-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4869-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4869-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4869-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f4869-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4869-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4869-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4869-120">Library</span></span><br/> | <dl> <span data-ttu-id="f4869-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f4869-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4869-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4869-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4869-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f4869-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




