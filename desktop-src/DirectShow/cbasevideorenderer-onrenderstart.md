---
description: La méthode OnRenderStart définit des informations pour le rendu.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Méthode CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542235"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="b07ef-103">Méthode CBaseVideoRenderer. OnRenderStart</span><span class="sxs-lookup"><span data-stu-id="b07ef-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="b07ef-104">La `OnRenderStart` méthode définit des informations pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="b07ef-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="b07ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b07ef-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b07ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b07ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b07ef-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="b07ef-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b07ef-108">Pointeur vers l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="b07ef-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b07ef-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b07ef-109">Return value</span></span>

<span data-ttu-id="b07ef-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b07ef-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b07ef-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b07ef-111">Remarks</span></span>

<span data-ttu-id="b07ef-112">Cette fonction membre récupère le temps horloge actuel du système et le stocke dans une variable membre à utiliser lorsque le dessin est terminé.</span><span class="sxs-lookup"><span data-stu-id="b07ef-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="b07ef-113">La fonction effectue également la journalisation des performances.</span><span class="sxs-lookup"><span data-stu-id="b07ef-113">The function also performs performance logging.</span></span> <span data-ttu-id="b07ef-114">Cette fonction membre doit être appelée juste avant le début du dessin.</span><span class="sxs-lookup"><span data-stu-id="b07ef-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="b07ef-115">Cette fonction membre substitue [**CBaseRenderer :: OnRenderStart**](cbaserenderer-onrenderstart.md).</span><span class="sxs-lookup"><span data-stu-id="b07ef-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b07ef-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b07ef-116">Requirements</span></span>



| <span data-ttu-id="b07ef-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b07ef-117">Requirement</span></span> | <span data-ttu-id="b07ef-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b07ef-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07ef-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b07ef-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b07ef-120"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b07ef-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b07ef-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b07ef-121">Library</span></span><br/> | <dl> <span data-ttu-id="b07ef-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b07ef-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b07ef-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b07ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07ef-124">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b07ef-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




