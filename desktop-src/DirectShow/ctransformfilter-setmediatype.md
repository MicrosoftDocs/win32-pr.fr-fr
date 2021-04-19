---
description: La méthode SetMediaType est appelée lorsque le type de média est défini sur l’un des codes confidentiels du filtre.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Méthode CTransformFilter. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529947"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="f258b-103">Méthode CTransformFilter. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="f258b-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="f258b-104">La `SetMediaType` méthode est appelée lorsque le type de média est défini sur l’un des codes confidentiels du filtre.</span><span class="sxs-lookup"><span data-stu-id="f258b-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="f258b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f258b-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="f258b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f258b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f258b-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="f258b-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="f258b-108">Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant un code confidentiel sur le filtre (entrée ou sortie).</span><span class="sxs-lookup"><span data-stu-id="f258b-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="f258b-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="f258b-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f258b-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="f258b-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f258b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f258b-111">Return value</span></span>

<span data-ttu-id="f258b-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f258b-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f258b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f258b-113">Remarks</span></span>

<span data-ttu-id="f258b-114">Les méthodes [**CTransformInputPin :: SetMediaType**](ctransforminputpin-setmediatype.md) et [**CTransformOutputPin :: SetMediaType**](ctransformoutputpin-setmediatype.md) appellent cette méthode quand le type de média d’un pin est défini.</span><span class="sxs-lookup"><span data-stu-id="f258b-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="f258b-115">Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="f258b-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f258b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f258b-116">Requirements</span></span>



| <span data-ttu-id="f258b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f258b-117">Requirement</span></span> | <span data-ttu-id="f258b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f258b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f258b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f258b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f258b-120"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f258b-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f258b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f258b-121">Library</span></span><br/> | <dl> <span data-ttu-id="f258b-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f258b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f258b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f258b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f258b-124">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f258b-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




