---
description: 'La méthode WaitForReceiveToComplete attend la fin de la méthode CBaseRenderer :: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Méthode CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522772"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="92f73-103">Méthode CBaseRenderer. WaitForReceiveToComplete</span><span class="sxs-lookup"><span data-stu-id="92f73-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="92f73-104">La `WaitForReceiveToComplete` méthode attend la fin de la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="92f73-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="92f73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92f73-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="92f73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92f73-106">Parameters</span></span>

<span data-ttu-id="92f73-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="92f73-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92f73-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92f73-108">Return value</span></span>

<span data-ttu-id="92f73-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="92f73-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92f73-110">Notes</span><span class="sxs-lookup"><span data-stu-id="92f73-110">Remarks</span></span>

<span data-ttu-id="92f73-111">Les méthodes [**CBaseRenderer :: Stop**](cbaserenderer-stop.md) et [**CBaseRenderer :: BeginFlush**](cbaserenderer-beginflush.md) appellent cette méthode pour synchroniser le changement d’État avec la méthode de **réception** .</span><span class="sxs-lookup"><span data-stu-id="92f73-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="92f73-112">Plus précisément, cette méthode distribue les messages pendant qu’elle attend que l’indicateur [**CBaseRenderer :: m \_ BInReceive**](cbaserenderer-m-binreceive.md) devienne **false**.</span><span class="sxs-lookup"><span data-stu-id="92f73-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="92f73-113">L’indicateur devient **true** dans la méthode [**CBaseRenderer ::P reparereceive**](cbaserenderer-preparereceive.md) et bascule vers **false** après que la méthode **Receive** a appelé la méthode [**CBaseRenderer ::P reparerender**](cbaserenderer-preparerender.md) .</span><span class="sxs-lookup"><span data-stu-id="92f73-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="92f73-114">La classe dérivée peut utiliser **PrepareRender** pour définir la palette.</span><span class="sxs-lookup"><span data-stu-id="92f73-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="92f73-115">L’attente de la fin de l’exécution de **PrepareRender** garantit que les messages de changement de palette sont distribués avant le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="92f73-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="92f73-116">Cela évite un blocage potentiel.</span><span class="sxs-lookup"><span data-stu-id="92f73-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="92f73-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92f73-117">Requirements</span></span>



| <span data-ttu-id="92f73-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92f73-118">Requirement</span></span> | <span data-ttu-id="92f73-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="92f73-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92f73-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="92f73-120">Header</span></span><br/>  | <dl> <span data-ttu-id="92f73-121"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92f73-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92f73-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="92f73-122">Library</span></span><br/> | <dl> <span data-ttu-id="92f73-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="92f73-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92f73-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92f73-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92f73-125">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="92f73-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




