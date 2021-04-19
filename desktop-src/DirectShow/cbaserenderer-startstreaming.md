---
description: La méthode StartStreaming lance la diffusion en continu lorsque le filtre passe à l’État en cours d’exécution.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Méthode CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530357"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="702ca-103">Méthode CBaseRenderer. StartStreaming</span><span class="sxs-lookup"><span data-stu-id="702ca-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="702ca-104">La `StartStreaming` méthode lance la diffusion en continu lorsque le filtre passe à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="702ca-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="702ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="702ca-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="702ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="702ca-106">Parameters</span></span>

<span data-ttu-id="702ca-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="702ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="702ca-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="702ca-108">Return value</span></span>

<span data-ttu-id="702ca-109">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="702ca-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="702ca-110">Notes</span><span class="sxs-lookup"><span data-stu-id="702ca-110">Remarks</span></span>

<span data-ttu-id="702ca-111">Si le filtre a un exemple, il planifie l’exemple de rendu.</span><span class="sxs-lookup"><span data-stu-id="702ca-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="702ca-112">Dans le cas contraire, si une notification de fin de flux est en attente, le filtre envoie un événement [**EC \_ complet**](ec-complete.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="702ca-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="702ca-113">Cette méthode appelle la méthode [**CBaseRenderer :: OnStartStreaming**](cbaserenderer-onstartstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="702ca-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="702ca-114">Cette méthode ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="702ca-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="702ca-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="702ca-115">Requirements</span></span>



| <span data-ttu-id="702ca-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="702ca-116">Requirement</span></span> | <span data-ttu-id="702ca-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="702ca-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="702ca-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="702ca-118">Header</span></span><br/>  | <dl> <span data-ttu-id="702ca-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="702ca-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="702ca-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="702ca-120">Library</span></span><br/> | <dl> <span data-ttu-id="702ca-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="702ca-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="702ca-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="702ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702ca-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="702ca-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




