---
description: La méthode GetResult récupère la liste d’arguments résultante, s’il en existe une.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: CDeferredCommand. GetResult, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543361"
---
# <a name="cdeferredcommandgetresult-method"></a><span data-ttu-id="119e7-103">CDeferredCommand. GetResult, méthode</span><span class="sxs-lookup"><span data-stu-id="119e7-103">CDeferredCommand.GetResult method</span></span>

<span data-ttu-id="119e7-104">La `GetResult` méthode récupère la liste d’arguments résultante, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="119e7-104">The `GetResult` method retrieves the resulting argument list, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="119e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="119e7-105">Syntax</span></span>


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a><span data-ttu-id="119e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="119e7-106">Parameters</span></span>

<span data-ttu-id="119e7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="119e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="119e7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="119e7-108">Return value</span></span>

<span data-ttu-id="119e7-109">Retourne un pointeur vers un **Variant** contenant la liste d’arguments de la méthode, si elle existe.</span><span class="sxs-lookup"><span data-stu-id="119e7-109">Returns a pointer to a **VARIANT** containing the method's argument list, if it exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="119e7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="119e7-110">Requirements</span></span>



| <span data-ttu-id="119e7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="119e7-111">Requirement</span></span> | <span data-ttu-id="119e7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="119e7-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="119e7-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="119e7-113">Header</span></span><br/>  | <dl> <span data-ttu-id="119e7-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="119e7-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="119e7-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="119e7-115">Library</span></span><br/> | <dl> <span data-ttu-id="119e7-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="119e7-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119e7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="119e7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119e7-118">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="119e7-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




