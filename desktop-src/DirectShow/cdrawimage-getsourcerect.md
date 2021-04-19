---
description: La méthode GetSourceRect récupère le rectangle source actuel.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Méthode CDrawImage. GetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528765"
---
# <a name="cdrawimagegetsourcerect-method"></a><span data-ttu-id="b6d4d-103">Méthode CDrawImage. GetSourceRect</span><span class="sxs-lookup"><span data-stu-id="b6d4d-103">CDrawImage.GetSourceRect method</span></span>

<span data-ttu-id="b6d4d-104">La `GetSourceRect` méthode récupère le rectangle source actuel.</span><span class="sxs-lookup"><span data-stu-id="b6d4d-104">The `GetSourceRect` method retrieves the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6d4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6d4d-105">Syntax</span></span>


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="b6d4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6d4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6d4d-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="b6d4d-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="b6d4d-108">Pointeur vers une structure **Rect** qui reçoit le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="b6d4d-108">Pointer to a **RECT** structure that receives the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6d4d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6d4d-109">Return value</span></span>

<span data-ttu-id="b6d4d-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b6d4d-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d4d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6d4d-111">Requirements</span></span>



| <span data-ttu-id="b6d4d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6d4d-112">Requirement</span></span> | <span data-ttu-id="b6d4d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6d4d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d4d-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6d4d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b6d4d-115"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d4d-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6d4d-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6d4d-116">Library</span></span><br/> | <dl> <span data-ttu-id="b6d4d-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d4d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6d4d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6d4d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d4d-119">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="b6d4d-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




