---
description: 'Méthode CTransformOutputPin. GetMediaType : la méthode GetMediaType récupère un type de média préféré, par valeur d’index.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Méthode CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094897"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="16347-103">Méthode CTransformOutputPin. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="16347-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="16347-104">La `GetMediaType` méthode récupère un type de média préféré, par valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="16347-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="16347-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16347-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="16347-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16347-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16347-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="16347-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="16347-108">Valeur d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="16347-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="16347-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="16347-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="16347-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="16347-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16347-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="16347-111">Return value</span></span>

<span data-ttu-id="16347-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16347-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="16347-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="16347-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="16347-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="16347-114">Return code</span></span>                                                                                            | <span data-ttu-id="16347-115">Description</span><span class="sxs-lookup"><span data-stu-id="16347-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="16347-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16347-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="16347-117">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="16347-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="16347-118"><dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt></span><span class="sxs-lookup"><span data-stu-id="16347-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="16347-119">Index hors limites</span><span class="sxs-lookup"><span data-stu-id="16347-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16347-120">Notes </span><span class="sxs-lookup"><span data-stu-id="16347-120">Remarks</span></span>

<span data-ttu-id="16347-121">Cette méthode remplace la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="16347-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="16347-122">Si la broche d’entrée du filtre n’est pas connectée, la méthode retourne VFW \_ s \_ n’a plus d' \_ \_ éléments.</span><span class="sxs-lookup"><span data-stu-id="16347-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="16347-123">Sinon, elle appelle la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) du filtre pour récupérer le type de média.</span><span class="sxs-lookup"><span data-stu-id="16347-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="16347-124">La méthode **CTransformFilter :: GetMediaType** est virtuelle pure ; la classe dérivée du filtre doit être substituée.</span><span class="sxs-lookup"><span data-stu-id="16347-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="16347-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16347-125">Requirements</span></span>



| <span data-ttu-id="16347-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16347-126">Requirement</span></span> | <span data-ttu-id="16347-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="16347-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16347-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="16347-128">Header</span></span><br/>  | <dl> <span data-ttu-id="16347-129"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16347-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16347-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16347-130">Library</span></span><br/> | <dl> <span data-ttu-id="16347-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="16347-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




