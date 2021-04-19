---
description: La méthode OnRenderStart est appelée quand le rendu est sur le le début.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Méthode CBaseRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535982"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="5bd1d-103">Méthode CBaseRenderer. OnRenderStart</span><span class="sxs-lookup"><span data-stu-id="5bd1d-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="5bd1d-104">La `OnRenderStart` méthode est appelée lorsque le rendu est sur le le début.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bd1d-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="5bd1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bd1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd1d-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="5bd1d-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5bd1d-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd1d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bd1d-109">Return value</span></span>

<span data-ttu-id="5bd1d-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd1d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5bd1d-111">Remarks</span></span>

<span data-ttu-id="5bd1d-112">La méthode [**CBaseRenderer :: Render**](cbaserenderer-render.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="5bd1d-113">Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer ; par exemple, pour collecter des données de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="5bd1d-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd1d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bd1d-114">Requirements</span></span>



| <span data-ttu-id="5bd1d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bd1d-115">Requirement</span></span> | <span data-ttu-id="5bd1d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bd1d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd1d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bd1d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5bd1d-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd1d-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5bd1d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5bd1d-119">Library</span></span><br/> | <dl> <span data-ttu-id="5bd1d-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd1d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd1d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd1d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd1d-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="5bd1d-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




