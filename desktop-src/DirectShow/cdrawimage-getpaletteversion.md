---
description: La méthode GetPaletteVersion récupère la version actuelle de la palette.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Méthode CDrawImage. GetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535385"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="ee088-103">Méthode CDrawImage. GetPaletteVersion</span><span class="sxs-lookup"><span data-stu-id="ee088-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="ee088-104">La `GetPaletteVersion` méthode récupère la version actuelle de la palette.</span><span class="sxs-lookup"><span data-stu-id="ee088-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee088-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee088-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="ee088-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee088-106">Parameters</span></span>

<span data-ttu-id="ee088-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee088-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee088-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee088-108">Return value</span></span>

<span data-ttu-id="ee088-109">Retourne la valeur de la variable membre **m \_ PaletteVersion** .</span><span class="sxs-lookup"><span data-stu-id="ee088-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee088-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ee088-110">Remarks</span></span>

<span data-ttu-id="ee088-111">La valeur retournée par cette méthode s’applique uniquement lorsque l’allocateur est un objet [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="ee088-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee088-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee088-112">Requirements</span></span>



| <span data-ttu-id="ee088-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee088-113">Requirement</span></span> | <span data-ttu-id="ee088-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee088-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee088-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee088-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ee088-116"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee088-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee088-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee088-117">Library</span></span><br/> | <dl> <span data-ttu-id="ee088-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ee088-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee088-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee088-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee088-120">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="ee088-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="ee088-121">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="ee088-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="ee088-122">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="ee088-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




