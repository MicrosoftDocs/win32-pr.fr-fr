---
description: La méthode CheckReady interroge si une transition d’État est terminée.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Méthode CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520986"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="b3f45-103">Méthode CBaseRenderer. CheckReady</span><span class="sxs-lookup"><span data-stu-id="b3f45-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="b3f45-104">La `CheckReady` méthode demande si une transition d’État est terminée.</span><span class="sxs-lookup"><span data-stu-id="b3f45-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3f45-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="b3f45-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3f45-106">Parameters</span></span>

<span data-ttu-id="b3f45-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b3f45-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3f45-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3f45-108">Return value</span></span>

<span data-ttu-id="b3f45-109">Retourne la **valeur true** si la transition d’État est terminée, ou **false** si le filtre est toujours en cours de transition vers un nouvel État.</span><span class="sxs-lookup"><span data-stu-id="b3f45-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f45-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3f45-110">Requirements</span></span>



| <span data-ttu-id="b3f45-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3f45-111">Requirement</span></span> | <span data-ttu-id="b3f45-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f45-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f45-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3f45-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b3f45-114"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3f45-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3f45-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3f45-115">Library</span></span><br/> | <dl> <span data-ttu-id="b3f45-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3f45-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f45-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3f45-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f45-118">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b3f45-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="b3f45-119">**CBaseRenderer :: nochapy**</span><span class="sxs-lookup"><span data-stu-id="b3f45-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="b3f45-120">**CBaseRenderer :: prêt**</span><span class="sxs-lookup"><span data-stu-id="b3f45-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




