---
description: La méthode IncrementPaletteVersion incrémente la version de la palette. Appelez cette méthode si le type de média passe à un nouveau format en palette.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Méthode CDrawImage. IncrementPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541704"
---
# <a name="cdrawimageincrementpaletteversion-method"></a><span data-ttu-id="684ad-104">Méthode CDrawImage. IncrementPaletteVersion</span><span class="sxs-lookup"><span data-stu-id="684ad-104">CDrawImage.IncrementPaletteVersion method</span></span>

<span data-ttu-id="684ad-105">La `IncrementPaletteVersion` méthode incrémente la version de la palette.</span><span class="sxs-lookup"><span data-stu-id="684ad-105">The `IncrementPaletteVersion` method increments the palette version.</span></span> <span data-ttu-id="684ad-106">Appelez cette méthode si le type de média passe à un nouveau format en palette.</span><span class="sxs-lookup"><span data-stu-id="684ad-106">Call this method if the media type changes to a new palettized format.</span></span>

## <a name="syntax"></a><span data-ttu-id="684ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="684ad-107">Syntax</span></span>


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="684ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="684ad-108">Parameters</span></span>

<span data-ttu-id="684ad-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="684ad-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="684ad-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="684ad-110">Return value</span></span>

<span data-ttu-id="684ad-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="684ad-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="684ad-112">Notes</span><span class="sxs-lookup"><span data-stu-id="684ad-112">Remarks</span></span>

<span data-ttu-id="684ad-113">Cette méthode incrémente la valeur de la variable membre **m \_ PaletteVersion** .</span><span class="sxs-lookup"><span data-stu-id="684ad-113">This method increments the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="684ad-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="684ad-114">Requirements</span></span>



| <span data-ttu-id="684ad-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="684ad-115">Requirement</span></span> | <span data-ttu-id="684ad-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="684ad-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="684ad-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="684ad-117">Header</span></span><br/>  | <dl> <span data-ttu-id="684ad-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="684ad-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="684ad-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="684ad-119">Library</span></span><br/> | <dl> <span data-ttu-id="684ad-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="684ad-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684ad-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="684ad-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684ad-122">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="684ad-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="684ad-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="684ad-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="684ad-124">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="684ad-124">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




