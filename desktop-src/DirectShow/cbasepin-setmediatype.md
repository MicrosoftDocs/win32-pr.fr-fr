---
description: La méthode SetMediaType définit le type de média pour la connexion.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Méthode CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528903"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="d962b-103">Méthode CBasePin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="d962b-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="d962b-104">La `SetMediaType` méthode définit le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="d962b-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d962b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d962b-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d962b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d962b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d962b-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="d962b-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d962b-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="d962b-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d962b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d962b-109">Return value</span></span>

<span data-ttu-id="d962b-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d962b-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d962b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d962b-111">Remarks</span></span>

<span data-ttu-id="d962b-112">Cette méthode établit le format d’une connexion de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d962b-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="d962b-113">Avant d’appeler cette méthode, le code PIN appelle la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) pour déterminer si le type de média est acceptable.</span><span class="sxs-lookup"><span data-stu-id="d962b-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="d962b-114">Par conséquent, le paramètre *VPM* est supposé être un type de média acceptable.</span><span class="sxs-lookup"><span data-stu-id="d962b-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="d962b-115">Dans la classe de base, cette méthode définit la variable de membre [**CBasePin :: m \_ MT**](cbasepin-m-mt.md) et retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d962b-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="d962b-116">Une classe dérivée peut substituer cette méthode si elle requiert une notification lorsque le type de média est défini.</span><span class="sxs-lookup"><span data-stu-id="d962b-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d962b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d962b-117">Requirements</span></span>



| <span data-ttu-id="d962b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d962b-118">Requirement</span></span> | <span data-ttu-id="d962b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d962b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d962b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d962b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d962b-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d962b-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d962b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d962b-122">Library</span></span><br/> | <dl> <span data-ttu-id="d962b-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d962b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d962b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d962b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d962b-125">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="d962b-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




