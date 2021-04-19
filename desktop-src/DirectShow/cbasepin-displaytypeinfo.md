---
description: La méthode DisplayTypeInfo affiche les informations sur le type de média pendant le débogage.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Méthode CBasePin. DisplayTypeInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521600"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="10a37-103">Méthode CBasePin. DisplayTypeInfo</span><span class="sxs-lookup"><span data-stu-id="10a37-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="10a37-104">La `DisplayTypeInfo` méthode affiche les informations sur le type de média pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="10a37-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10a37-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="10a37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a37-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="10a37-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="10a37-108">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="10a37-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="10a37-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="10a37-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="10a37-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="10a37-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a37-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10a37-111">Return value</span></span>

<span data-ttu-id="10a37-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="10a37-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10a37-113">Notes</span><span class="sxs-lookup"><span data-stu-id="10a37-113">Remarks</span></span>

<span data-ttu-id="10a37-114">Dans les versions Debug, cette méthode appelle la fonction [**DbgLog**](dbglog.md) pour afficher le type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="10a37-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="10a37-115">Dans les versions commerciales, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="10a37-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a37-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10a37-116">Requirements</span></span>



| <span data-ttu-id="10a37-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10a37-117">Requirement</span></span> | <span data-ttu-id="10a37-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="10a37-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a37-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="10a37-119">Header</span></span><br/>  | <dl> <span data-ttu-id="10a37-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10a37-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="10a37-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10a37-121">Library</span></span><br/> | <dl> <span data-ttu-id="10a37-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10a37-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10a37-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a37-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a37-124">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="10a37-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




