---
description: 'La \_ méthode obtenir PrerollTime récupère la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode IMediaPosition :: obten \_ PrerollTime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Méthode CPosPassThru.get_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545468"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="48ed7-104">Méthode CPosPassThru. obten \_ PrerollTime</span><span class="sxs-lookup"><span data-stu-id="48ed7-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="48ed7-105">La `get_PrerollTime` méthode récupère la quantité de données qui seront placées en file d’attente avant la position de début.</span><span class="sxs-lookup"><span data-stu-id="48ed7-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="48ed7-106">Cette méthode implémente la méthode [**IMediaPosition :: obten \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="48ed7-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ed7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48ed7-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="48ed7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48ed7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ed7-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="48ed7-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="48ed7-110">Pointeur vers une variable qui reçoit le temps de préroll, en secondes.</span><span class="sxs-lookup"><span data-stu-id="48ed7-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48ed7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48ed7-111">Return value</span></span>

<span data-ttu-id="48ed7-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="48ed7-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="48ed7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48ed7-113">Requirements</span></span>



| <span data-ttu-id="48ed7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48ed7-114">Requirement</span></span> | <span data-ttu-id="48ed7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="48ed7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48ed7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="48ed7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="48ed7-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48ed7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48ed7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48ed7-118">Library</span></span><br/> | <dl> <span data-ttu-id="48ed7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48ed7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48ed7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48ed7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ed7-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="48ed7-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




