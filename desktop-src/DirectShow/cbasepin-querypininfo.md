---
description: 'La méthode QueryPinInfo récupère des informations sur le code confidentiel. Cette méthode implémente la méthode IPin :: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Méthode CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524017"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="8bf6d-104">Méthode CBasePin. QueryPinInfo</span><span class="sxs-lookup"><span data-stu-id="8bf6d-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="8bf6d-105">La `QueryPinInfo` méthode récupère des informations sur le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="8bf6d-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="8bf6d-106">Cette méthode implémente la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="8bf6d-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf6d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bf6d-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8bf6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bf6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf6d-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="8bf6d-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf6d-110">Pointeur vers une structure d' [**\_ informations de code confidentiel**](/windows/win32/api/strmif/ns-strmif-pin_info) qui reçoit les informations de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="8bf6d-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf6d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8bf6d-111">Return value</span></span>

<span data-ttu-id="8bf6d-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="8bf6d-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf6d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8bf6d-113">Remarks</span></span>

<span data-ttu-id="8bf6d-114">Cette méthode utilise la variable membre [**CBasePin :: m \_ pname**](cbasepin-m-pname.md) pour le membre **achName** de la structure d’informations sur le code confidentiel \_ .</span><span class="sxs-lookup"><span data-stu-id="8bf6d-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="8bf6d-115">Lorsque la méthode est retournée, si le membre **pFilter** de la structure info de code confidentiel \_ est non **null**, il a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="8bf6d-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="8bf6d-116">Veillez à libérer l’interface lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="8bf6d-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf6d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bf6d-117">Requirements</span></span>



| <span data-ttu-id="8bf6d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bf6d-118">Requirement</span></span> | <span data-ttu-id="8bf6d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bf6d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf6d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bf6d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8bf6d-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf6d-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8bf6d-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8bf6d-122">Library</span></span><br/> | <dl> <span data-ttu-id="8bf6d-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf6d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf6d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bf6d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf6d-125">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="8bf6d-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




