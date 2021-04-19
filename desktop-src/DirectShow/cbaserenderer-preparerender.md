---
description: La méthode PrepareRender est appelée avant que le filtre ne restitue un exemple.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Méthode CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541528"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="95797-103">Méthode CBaseRenderer. PrepareRender</span><span class="sxs-lookup"><span data-stu-id="95797-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="95797-104">La `PrepareRender` méthode est appelée avant que le filtre ne restitue un exemple.</span><span class="sxs-lookup"><span data-stu-id="95797-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="95797-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95797-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="95797-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95797-106">Parameters</span></span>

<span data-ttu-id="95797-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="95797-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95797-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95797-108">Return value</span></span>

<span data-ttu-id="95797-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="95797-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95797-110">Notes</span><span class="sxs-lookup"><span data-stu-id="95797-110">Remarks</span></span>

<span data-ttu-id="95797-111">Le filtre appelle cette méthode avant d’appeler la méthode [**CBaseRenderer :: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) ou la méthode [**CBaseRenderer :: Render**](cbaserenderer-render.md) .</span><span class="sxs-lookup"><span data-stu-id="95797-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="95797-112">`PrepareRender` n’effectue aucune opération dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="95797-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="95797-113">La classe dérivée peut la substituer pour exécuter toutes les actions requises avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="95797-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="95797-114">Par exemple, un convertisseur vidéo peut remplacer cette méthode pour réaliser sa palette.</span><span class="sxs-lookup"><span data-stu-id="95797-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="95797-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95797-115">Requirements</span></span>



| <span data-ttu-id="95797-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95797-116">Requirement</span></span> | <span data-ttu-id="95797-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="95797-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95797-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="95797-118">Header</span></span><br/>  | <dl> <span data-ttu-id="95797-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95797-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95797-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95797-120">Library</span></span><br/> | <dl> <span data-ttu-id="95797-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95797-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95797-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95797-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95797-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="95797-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




