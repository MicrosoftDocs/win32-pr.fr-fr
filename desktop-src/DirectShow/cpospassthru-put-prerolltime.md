---
description: La \_ méthode put PrerollTime définit la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode IMediaPosition ::p ut \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Méthode CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544340"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="de023-104">CPosPassThru. put \_ PrerollTime, méthode</span><span class="sxs-lookup"><span data-stu-id="de023-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="de023-105">La `put_PrerollTime` méthode définit la quantité de données qui seront placées en file d’attente avant la position de début.</span><span class="sxs-lookup"><span data-stu-id="de023-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="de023-106">Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="de023-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de023-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de023-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="de023-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de023-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de023-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="de023-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="de023-110">Durée du préroll, en secondes.</span><span class="sxs-lookup"><span data-stu-id="de023-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de023-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de023-111">Return value</span></span>

<span data-ttu-id="de023-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="de023-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="de023-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de023-113">Requirements</span></span>



| <span data-ttu-id="de023-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de023-114">Requirement</span></span> | <span data-ttu-id="de023-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="de023-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de023-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="de023-116">Header</span></span><br/>  | <dl> <span data-ttu-id="de023-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de023-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de023-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="de023-118">Library</span></span><br/> | <dl> <span data-ttu-id="de023-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de023-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de023-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de023-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de023-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="de023-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




