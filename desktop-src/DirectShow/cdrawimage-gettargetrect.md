---
description: La méthode GetTargetRect récupère le rectangle de destination actuel.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Méthode CDrawImage. GetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528489"
---
# <a name="cdrawimagegettargetrect-method"></a><span data-ttu-id="611ee-103">Méthode CDrawImage. GetTargetRect</span><span class="sxs-lookup"><span data-stu-id="611ee-103">CDrawImage.GetTargetRect method</span></span>

<span data-ttu-id="611ee-104">La `GetTargetRect` méthode récupère le rectangle de destination actuel.</span><span class="sxs-lookup"><span data-stu-id="611ee-104">The `GetTargetRect` method retrieves the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="611ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="611ee-105">Syntax</span></span>


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="611ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="611ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="611ee-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="611ee-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="611ee-108">Pointeur vers une structure **Rect** qui reçoit le rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="611ee-108">Pointer to a **RECT** structure that receives the target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="611ee-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="611ee-109">Return value</span></span>

<span data-ttu-id="611ee-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="611ee-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="611ee-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="611ee-111">Requirements</span></span>



| <span data-ttu-id="611ee-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="611ee-112">Requirement</span></span> | <span data-ttu-id="611ee-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="611ee-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611ee-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="611ee-114">Header</span></span><br/>  | <dl> <span data-ttu-id="611ee-115"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="611ee-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="611ee-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="611ee-116">Library</span></span><br/> | <dl> <span data-ttu-id="611ee-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="611ee-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="611ee-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="611ee-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611ee-119">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="611ee-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




