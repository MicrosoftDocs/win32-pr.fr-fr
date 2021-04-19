---
description: La méthode IsFlushing interroge le fait que le filtre est en cours de vidage.
ms.assetid: 366b6162-7a2c-4882-8774-8b4bf83012b4
title: Méthode CBaseInputPin. IsFlushing (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsFlushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5af91e78d10f480596b8e0820ee6de4c4df2998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539596"
---
# <a name="cbaseinputpinisflushing-method"></a><span data-ttu-id="1ee22-103">Méthode CBaseInputPin. IsFlushing</span><span class="sxs-lookup"><span data-stu-id="1ee22-103">CBaseInputPin.IsFlushing method</span></span>

<span data-ttu-id="1ee22-104">La `IsFlushing` méthode demande si le filtre est en cours de vidage.</span><span class="sxs-lookup"><span data-stu-id="1ee22-104">The `IsFlushing` method queries whether the filter is currently flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ee22-105">Syntax</span></span>


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a><span data-ttu-id="1ee22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ee22-106">Parameters</span></span>

<span data-ttu-id="1ee22-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1ee22-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ee22-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ee22-108">Return value</span></span>

<span data-ttu-id="1ee22-109">Retourne la variable de membre [**CBaseInputPin :: m \_ bFlushing**](cbaseinputpin-m-bflushing.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee22-109">Returns the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee22-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ee22-110">Requirements</span></span>



| <span data-ttu-id="1ee22-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ee22-111">Requirement</span></span> | <span data-ttu-id="1ee22-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ee22-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee22-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ee22-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1ee22-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee22-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1ee22-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ee22-115">Library</span></span><br/> | <dl> <span data-ttu-id="1ee22-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee22-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee22-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ee22-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee22-118">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1ee22-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




