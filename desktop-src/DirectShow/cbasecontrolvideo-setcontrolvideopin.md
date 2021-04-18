---
description: La méthode SetControlVideoPin définit le code confidentiel utilisé par le filtre.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Méthode CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532764"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="4e1ec-103">Méthode CBaseControlVideo. SetControlVideoPin</span><span class="sxs-lookup"><span data-stu-id="4e1ec-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="4e1ec-104">La `SetControlVideoPin` méthode définit le code confidentiel utilisé par le filtre.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e1ec-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="4e1ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e1ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1ec-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="4e1ec-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4e1ec-108">Pointeur vers le code confidentiel avec lequel l’interface est synchronisée.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1ec-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e1ec-109">Return value</span></span>

<span data-ttu-id="4e1ec-110">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1ec-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4e1ec-111">Remarks</span></span>

<span data-ttu-id="4e1ec-112">L’interface peut être appelée uniquement lorsque le filtre a été connecté avec succès.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="4e1ec-113">L’objet est passé par cette méthode au code confidentiel avec lequel il est synchronisé ; dans la plupart des cas, il détermine si le code confidentiel est connecté lorsqu’il a une méthode d’interface appelée et retourne VFW \_ E \_ non \_ connecté en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4e1ec-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1ec-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e1ec-114">Requirements</span></span>



| <span data-ttu-id="4e1ec-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e1ec-115">Requirement</span></span> | <span data-ttu-id="4e1ec-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e1ec-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1ec-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e1ec-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4e1ec-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e1ec-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e1ec-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e1ec-119">Library</span></span><br/> | <dl> <span data-ttu-id="4e1ec-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e1ec-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1ec-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e1ec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1ec-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="4e1ec-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




