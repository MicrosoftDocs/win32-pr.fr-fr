---
description: 'Méthode CBaseMediaFilter. StreamTime : la méthode StreamTime récupère le temps de flux actuel.'
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Méthode CBaseMediaFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096247"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="f1678-103">Méthode CBaseMediaFilter. StreamTime</span><span class="sxs-lookup"><span data-stu-id="f1678-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="f1678-104">La `StreamTime` méthode récupère le temps de flux actuel.</span><span class="sxs-lookup"><span data-stu-id="f1678-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1678-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1678-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="f1678-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1678-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1678-107">*rtStream* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="f1678-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f1678-108">Référence à un objet [**CRefTime**](creftime.md) qui reçoit le temps de flux actuel.</span><span class="sxs-lookup"><span data-stu-id="f1678-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1678-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1678-109">Return value</span></span>

<span data-ttu-id="f1678-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1678-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f1678-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f1678-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="f1678-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f1678-112">Return code</span></span>                                                                                      | <span data-ttu-id="f1678-113">Description</span><span class="sxs-lookup"><span data-stu-id="f1678-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="f1678-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1678-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="f1678-115">Réussite.</span><span class="sxs-lookup"><span data-stu-id="f1678-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="f1678-116"><dt>**VFW \_ E \_ pas d' \_ horloge**</dt></span><span class="sxs-lookup"><span data-stu-id="f1678-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="f1678-117">Aucune horloge de référence n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f1678-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1678-118">Notes </span><span class="sxs-lookup"><span data-stu-id="f1678-118">Remarks</span></span>

<span data-ttu-id="f1678-119">Le temps de flux est défini comme le temps de référence actuel (comme indiqué par l’horloge de référence) moins l’heure de début (spécifiée par [**CBaseMediaFilter :: m \_ tStart**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="f1678-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="f1678-120">L’horodatage d’un exemple de média spécifie l’heure du flux de temps quand il doit être rendu.</span><span class="sxs-lookup"><span data-stu-id="f1678-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="f1678-121">Si un échantillon dont l’horodatage est inférieur à l’heure actuelle du flux n’a pas encore été affiché, il est tardif.</span><span class="sxs-lookup"><span data-stu-id="f1678-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1678-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1678-122">Requirements</span></span>



| <span data-ttu-id="f1678-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1678-123">Requirement</span></span> | <span data-ttu-id="f1678-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1678-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1678-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1678-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f1678-126"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1678-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1678-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1678-127">Library</span></span><br/> | <dl> <span data-ttu-id="f1678-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1678-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1678-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1678-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1678-130">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f1678-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




