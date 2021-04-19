---
description: La \_ méthode put StopTime définit l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaPosition ::p ut \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Méthode CPosPassThru.put_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543952"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="057ff-104">CPosPassThru. put \_ StopTime, méthode</span><span class="sxs-lookup"><span data-stu-id="057ff-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="057ff-105">La `put_StopTime` méthode définit l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="057ff-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="057ff-106">Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="057ff-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="057ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="057ff-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="057ff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="057ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="057ff-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="057ff-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="057ff-110">Heure d’arrêt en tant que valeur **double** , en secondes.</span><span class="sxs-lookup"><span data-stu-id="057ff-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="057ff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="057ff-111">Return value</span></span>

<span data-ttu-id="057ff-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="057ff-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="057ff-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="057ff-113">Requirements</span></span>



| <span data-ttu-id="057ff-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="057ff-114">Requirement</span></span> | <span data-ttu-id="057ff-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="057ff-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="057ff-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="057ff-116">Header</span></span><br/>  | <dl> <span data-ttu-id="057ff-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="057ff-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="057ff-118">Library</span></span><br/> | <dl> <span data-ttu-id="057ff-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="057ff-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="057ff-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="057ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057ff-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="057ff-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




