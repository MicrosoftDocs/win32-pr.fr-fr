---
description: À partir de la liste des types de média, la méthode TryMediaTypes tente de terminer une connexion à l’aide de l’un de ces types.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Méthode CBasePin. TryMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523581"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="7210d-103">Méthode CBasePin. TryMediaTypes</span><span class="sxs-lookup"><span data-stu-id="7210d-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="7210d-104">À partir d’une liste de types de média, la `TryMediaTypes` méthode tente de terminer une connexion à l’aide de l’un de ces types.</span><span class="sxs-lookup"><span data-stu-id="7210d-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7210d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7210d-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="7210d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7210d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7210d-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="7210d-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7210d-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin de réception.</span><span class="sxs-lookup"><span data-stu-id="7210d-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7210d-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="7210d-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7210d-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui limite les types de média possibles, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="7210d-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7210d-111">*pEnum*</span><span class="sxs-lookup"><span data-stu-id="7210d-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="7210d-112">Pointeur vers une interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , utilisé pour énumérer la liste des types de média.</span><span class="sxs-lookup"><span data-stu-id="7210d-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7210d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7210d-113">Return value</span></span>

<span data-ttu-id="7210d-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7210d-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7210d-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7210d-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7210d-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7210d-116">Return code</span></span>                                                                                                  | <span data-ttu-id="7210d-117">Description</span><span class="sxs-lookup"><span data-stu-id="7210d-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="7210d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7210d-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="7210d-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7210d-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="7210d-120"><dt>**VFW \_ E \_ aucun \_ \_ type acceptable**</dt></span><span class="sxs-lookup"><span data-stu-id="7210d-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="7210d-121">Impossible de trouver un type de média acceptable.</span><span class="sxs-lookup"><span data-stu-id="7210d-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7210d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="7210d-122">Remarks</span></span>

<span data-ttu-id="7210d-123">Pour chaque type de média retourné par l’interface **IEnumMediaTypes** , cette méthode tente une connexion en appelant la méthode [**CBasePin :: AttemptConnection**](cbasepin-attemptconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="7210d-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="7210d-124">Si le paramètre *VPM* est non **null**, le code PIN ignore les types de média qui ne correspondent pas à ce type.</span><span class="sxs-lookup"><span data-stu-id="7210d-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="7210d-125">Le paramètre *VPM* peut spécifier un type de média partiel.</span><span class="sxs-lookup"><span data-stu-id="7210d-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="7210d-126">Un type de média partiel a une valeur de GUID \_ null pour le type principal, le sous-type ou le format.</span><span class="sxs-lookup"><span data-stu-id="7210d-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="7210d-127">La \_ valeur null GUID correspond à n’importe quel type, similaire à une valeur « caractère générique ».</span><span class="sxs-lookup"><span data-stu-id="7210d-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7210d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7210d-128">Requirements</span></span>



| <span data-ttu-id="7210d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7210d-129">Requirement</span></span> | <span data-ttu-id="7210d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7210d-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7210d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7210d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7210d-132"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7210d-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7210d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7210d-133">Library</span></span><br/> | <dl> <span data-ttu-id="7210d-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7210d-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7210d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7210d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7210d-136">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="7210d-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




