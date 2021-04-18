---
description: La méthode OnRenderEnd est appelée après le rendu d’un exemple.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Méthode CBaseRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540691"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="0445a-103">Méthode CBaseRenderer. OnRenderEnd</span><span class="sxs-lookup"><span data-stu-id="0445a-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="0445a-104">La `OnRenderEnd` méthode est appelée après le rendu d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="0445a-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="0445a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0445a-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="0445a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0445a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0445a-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="0445a-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0445a-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="0445a-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0445a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0445a-109">Return value</span></span>

<span data-ttu-id="0445a-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0445a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0445a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0445a-111">Remarks</span></span>

<span data-ttu-id="0445a-112">La méthode [**CBaseRenderer :: Render**](cbaserenderer-render.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0445a-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="0445a-113">Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer ; par exemple, pour collecter des données de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="0445a-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="0445a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0445a-114">Requirements</span></span>



| <span data-ttu-id="0445a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0445a-115">Requirement</span></span> | <span data-ttu-id="0445a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0445a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0445a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0445a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0445a-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0445a-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0445a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0445a-119">Library</span></span><br/> | <dl> <span data-ttu-id="0445a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0445a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0445a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0445a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0445a-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="0445a-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




