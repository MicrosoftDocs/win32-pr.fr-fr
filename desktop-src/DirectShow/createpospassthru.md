---
description: La fonction CreatePosPassThru crée un objet CPosPassThru ou un objet CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: CreatePosPassThru, fonction (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526391"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="59989-103">CreatePosPassThru fonction)</span><span class="sxs-lookup"><span data-stu-id="59989-103">CreatePosPassThru function</span></span>

<span data-ttu-id="59989-104">La `CreatePosPassThru` fonction crée un objet [**CPosPassThru**](cpospassthru.md) ou un objet [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="59989-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="59989-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59989-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="59989-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59989-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59989-107">*pAgg*</span><span class="sxs-lookup"><span data-stu-id="59989-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="59989-108">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="59989-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="59989-109">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="59989-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="59989-110">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="59989-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59989-111">*bRenderer*</span><span class="sxs-lookup"><span data-stu-id="59989-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="59989-112">Valeur booléenne qui spécifie si le filtre est un convertisseur.</span><span class="sxs-lookup"><span data-stu-id="59989-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="59989-113">Utilisez la valeur **true** si le filtre est un convertisseur, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="59989-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="59989-114">Si la valeur est **true**, cette méthode crée une instance de la classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="59989-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="59989-115">Si la valeur est **false**, la méthode crée une instance de la classe **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="59989-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="59989-116">*pPin*</span><span class="sxs-lookup"><span data-stu-id="59989-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="59989-117">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) sur la broche d’entrée du filtre.</span><span class="sxs-lookup"><span data-stu-id="59989-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="59989-118">*ppPassThru*</span><span class="sxs-lookup"><span data-stu-id="59989-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="59989-119">Adresse d’une variable qui reçoit un pointeur vers l’interface **IUnknown** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="59989-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59989-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59989-120">Return value</span></span>

<span data-ttu-id="59989-121">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="59989-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="59989-122">Sinon, retourne une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="59989-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="59989-123">Notes</span><span class="sxs-lookup"><span data-stu-id="59989-123">Remarks</span></span>

<span data-ttu-id="59989-124">Cette méthode utilise l’interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) pour créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="59989-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="59989-125">L’objet est chargé dynamiquement à partir de Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="59989-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="59989-126">Si la fonction est réussie, l’interface **IUnknown** retournée a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="59989-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="59989-127">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="59989-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="59989-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59989-128">Requirements</span></span>



| <span data-ttu-id="59989-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59989-129">Requirement</span></span> | <span data-ttu-id="59989-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="59989-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59989-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="59989-131">Header</span></span><br/>  | <dl> <span data-ttu-id="59989-132"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59989-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59989-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59989-133">Library</span></span><br/> | <dl> <span data-ttu-id="59989-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59989-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59989-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59989-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59989-136">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="59989-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




