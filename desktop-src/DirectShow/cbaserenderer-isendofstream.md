---
description: La méthode IsEndOfStream interroge si la notification de fin de flux a été reçue.
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: Méthode CBaseRenderer. IsEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e07afb4dfb10e38d90184ba5747f200d1bc716d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541074"
---
# <a name="cbaserendererisendofstream-method"></a><span data-ttu-id="1603a-103">Méthode CBaseRenderer. IsEndOfStream</span><span class="sxs-lookup"><span data-stu-id="1603a-103">CBaseRenderer.IsEndOfStream method</span></span>

<span data-ttu-id="1603a-104">La `IsEndOfStream` méthode interroge si la notification de fin de flux a été reçue.</span><span class="sxs-lookup"><span data-stu-id="1603a-104">The `IsEndOfStream` method queries whether the end-of-stream notification was received.</span></span>

## <a name="syntax"></a><span data-ttu-id="1603a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1603a-105">Syntax</span></span>


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="1603a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1603a-106">Parameters</span></span>

<span data-ttu-id="1603a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1603a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1603a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1603a-108">Return value</span></span>

<span data-ttu-id="1603a-109">Retourne l’indicateur [**CBaseRenderer :: m \_ bEOS**](cbaserenderer-m-beos.md) .</span><span class="sxs-lookup"><span data-stu-id="1603a-109">Returns the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="1603a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1603a-110">Requirements</span></span>



| <span data-ttu-id="1603a-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1603a-111">Requirement</span></span> | <span data-ttu-id="1603a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1603a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1603a-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="1603a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1603a-114"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1603a-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1603a-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1603a-115">Library</span></span><br/> | <dl> <span data-ttu-id="1603a-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1603a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1603a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1603a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1603a-118">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="1603a-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




