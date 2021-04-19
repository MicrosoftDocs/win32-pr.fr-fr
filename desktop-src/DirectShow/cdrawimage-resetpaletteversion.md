---
description: La méthode ResetPaletteVersion réinitialise la version de la palette. Appelez cette méthode si le code confidentiel du filtre propriétaire se reconnecte.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Méthode CDrawImage. ResetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537972"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="2b114-104">Méthode CDrawImage. ResetPaletteVersion</span><span class="sxs-lookup"><span data-stu-id="2b114-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="2b114-105">La `ResetPaletteVersion` méthode réinitialise la version de la palette.</span><span class="sxs-lookup"><span data-stu-id="2b114-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="2b114-106">Appelez cette méthode si le code confidentiel du filtre propriétaire se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="2b114-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b114-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b114-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="2b114-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b114-108">Parameters</span></span>

<span data-ttu-id="2b114-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2b114-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b114-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b114-110">Return value</span></span>

<span data-ttu-id="2b114-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2b114-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b114-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2b114-112">Remarks</span></span>

<span data-ttu-id="2b114-113">Cette méthode définit la valeur de **m \_ PaletteVersion** sur une constante prédéfinie, **\_ version** de la palette.</span><span class="sxs-lookup"><span data-stu-id="2b114-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b114-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b114-114">Requirements</span></span>



| <span data-ttu-id="2b114-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b114-115">Requirement</span></span> | <span data-ttu-id="2b114-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b114-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b114-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b114-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2b114-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b114-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b114-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b114-119">Library</span></span><br/> | <dl> <span data-ttu-id="2b114-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2b114-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b114-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b114-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b114-122">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="2b114-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="2b114-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="2b114-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="2b114-124">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="2b114-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




