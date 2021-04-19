---
description: La méthode NotifyEndOfStream publie un \_ événement EC complet dans le gestionnaire de graphique de filtre.
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: Méthode CBaseRenderer. NotifyEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1187705bfa678252237bd95d9a4cb21a0f97d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529926"
---
# <a name="cbaserenderernotifyendofstream-method"></a><span data-ttu-id="d1dac-103">Méthode CBaseRenderer. NotifyEndOfStream</span><span class="sxs-lookup"><span data-stu-id="d1dac-103">CBaseRenderer.NotifyEndOfStream method</span></span>

<span data-ttu-id="d1dac-104">La `NotifyEndOfStream` méthode publie un événement [**EC \_ complet**](ec-complete.md) dans le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="d1dac-104">The `NotifyEndOfStream` method posts an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1dac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1dac-105">Syntax</span></span>


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="d1dac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1dac-106">Parameters</span></span>

<span data-ttu-id="d1dac-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d1dac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1dac-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1dac-108">Return value</span></span>

<span data-ttu-id="d1dac-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1dac-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1dac-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1dac-110">Requirements</span></span>



| <span data-ttu-id="d1dac-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1dac-111">Requirement</span></span> | <span data-ttu-id="d1dac-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1dac-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1dac-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1dac-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d1dac-114"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1dac-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1dac-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1dac-115">Library</span></span><br/> | <dl> <span data-ttu-id="d1dac-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1dac-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1dac-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1dac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1dac-118">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="d1dac-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="d1dac-119">**CBaseRenderer :: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d1dac-119">**CBaseRenderer::EndOfStream**</span></span>](cbaserenderer-endofstream.md)
</dt> <dt>

[<span data-ttu-id="d1dac-120">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d1dac-120">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




