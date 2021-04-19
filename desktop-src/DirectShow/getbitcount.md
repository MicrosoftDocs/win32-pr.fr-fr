---
description: La fonction GetBitCount retourne le nombre de bits par pixel utilisé par un sous-type de vidéo spécifié. Cette fonction est valide uniquement pour les sous-types RGB non compressés.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: GetBitCount, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541126"
---
# <a name="getbitcount-function"></a><span data-ttu-id="f277f-104">GetBitCount fonction)</span><span class="sxs-lookup"><span data-stu-id="f277f-104">GetBitCount function</span></span>

<span data-ttu-id="f277f-105">La `GetBitCount` fonction retourne le nombre de bits par pixel utilisé par un sous-type de vidéo spécifié.</span><span class="sxs-lookup"><span data-stu-id="f277f-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="f277f-106">Cette fonction est valide uniquement pour les sous-types RGB non compressés.</span><span class="sxs-lookup"><span data-stu-id="f277f-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f277f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f277f-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="f277f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f277f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f277f-109">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="f277f-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="f277f-110">Pointeur vers un **GUID** de sous-type de vidéo.</span><span class="sxs-lookup"><span data-stu-id="f277f-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f277f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f277f-111">Return value</span></span>

<span data-ttu-id="f277f-112">Retourne le nombre de bits par pixel pour ce sous-type, ou la valeur **USHRT \_ Max** si le sous-type n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="f277f-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f277f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f277f-113">Requirements</span></span>



| <span data-ttu-id="f277f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f277f-114">Requirement</span></span> | <span data-ttu-id="f277f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f277f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f277f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="f277f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f277f-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f277f-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f277f-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f277f-118">Library</span></span><br/> | <dl> <span data-ttu-id="f277f-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f277f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f277f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f277f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f277f-121">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="f277f-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




