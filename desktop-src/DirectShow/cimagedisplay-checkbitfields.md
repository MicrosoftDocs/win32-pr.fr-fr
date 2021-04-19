---
description: La méthode CheckBitFields valide les masques de couleur dans une structure VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Méthode CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532536"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="585b7-103">Méthode CImageDisplay. CheckBitFields</span><span class="sxs-lookup"><span data-stu-id="585b7-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="585b7-104">La `CheckBitFields` méthode valide les masques de couleur dans une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="585b7-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="585b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="585b7-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="585b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="585b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585b7-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="585b7-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="585b7-108">Pointeur vers une structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="585b7-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="585b7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="585b7-109">Return value</span></span>

<span data-ttu-id="585b7-110">Retourne la **valeur true** si les masques de couleur sont valides, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="585b7-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="585b7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="585b7-111">Remarks</span></span>

<span data-ttu-id="585b7-112">Cette méthode vérifie que le masque de couleur pour chaque composant de couleur est compris entre un et huit bits et que chaque masque de couleur est une séquence contiguë de bits.</span><span class="sxs-lookup"><span data-stu-id="585b7-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="585b7-113">Appelez cette méthode uniquement lorsque le membre de bicompression est défini sur les champs de **décompression** bi \_ .</span><span class="sxs-lookup"><span data-stu-id="585b7-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="585b7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="585b7-114">Requirements</span></span>



| <span data-ttu-id="585b7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="585b7-115">Requirement</span></span> | <span data-ttu-id="585b7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="585b7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="585b7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="585b7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="585b7-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="585b7-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="585b7-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="585b7-119">Library</span></span><br/> | <dl> <span data-ttu-id="585b7-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="585b7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="585b7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="585b7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="585b7-122">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="585b7-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




