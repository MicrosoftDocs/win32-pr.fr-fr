---
description: La méthode CountSetBits retourne le nombre de bits définis à 1 dans un champ de bits spécifié.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Méthode CImageDisplay. CountSetBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537896"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="33c73-103">Méthode CImageDisplay. CountSetBits</span><span class="sxs-lookup"><span data-stu-id="33c73-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="33c73-104">La `CountSetBits` méthode retourne le nombre de bits définis à 1 dans un champ de bits spécifié.</span><span class="sxs-lookup"><span data-stu-id="33c73-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33c73-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="33c73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33c73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c73-107">*Champ*</span><span class="sxs-lookup"><span data-stu-id="33c73-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="33c73-108">Spécifie un champ de bits comme valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="33c73-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c73-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33c73-109">Return value</span></span>

<span data-ttu-id="33c73-110">Retourne le nombre de bits définis sur 1.</span><span class="sxs-lookup"><span data-stu-id="33c73-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c73-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33c73-111">Requirements</span></span>



| <span data-ttu-id="33c73-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33c73-112">Requirement</span></span> | <span data-ttu-id="33c73-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="33c73-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c73-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="33c73-114">Header</span></span><br/>  | <dl> <span data-ttu-id="33c73-115"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33c73-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33c73-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33c73-116">Library</span></span><br/> | <dl> <span data-ttu-id="33c73-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="33c73-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c73-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33c73-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c73-119">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="33c73-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




