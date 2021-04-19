---
description: La méthode SetReconnectWhenActive spécifie si le code PIN prend en charge les reconnexions dynamiques.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Méthode CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542220"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="95805-103">Méthode CBasePin. SetReconnectWhenActive</span><span class="sxs-lookup"><span data-stu-id="95805-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="95805-104">La `SetReconnectWhenActive` méthode spécifie si le code PIN prend en charge les reconnexions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="95805-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="95805-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95805-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="95805-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95805-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95805-107">*bCanReconnect*</span><span class="sxs-lookup"><span data-stu-id="95805-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="95805-108">Valeur booléenne qui spécifie si le code confidentiel peut se reconnecter dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="95805-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="95805-109">Si la **valeur est true**, le code confidentiel peut se reconnecter dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="95805-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95805-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95805-110">Return value</span></span>

<span data-ttu-id="95805-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="95805-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95805-112">Notes</span><span class="sxs-lookup"><span data-stu-id="95805-112">Remarks</span></span>

<span data-ttu-id="95805-113">Par défaut, vous devez arrêter un filtre avant de reconnecter l’un de ses pin.</span><span class="sxs-lookup"><span data-stu-id="95805-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="95805-114">Si le code pin peut se reconnecter alors que le filtre est actif, appelez cette méthode avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="95805-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="95805-115">Pour plus d’informations, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="95805-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95805-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95805-116">Requirements</span></span>



| <span data-ttu-id="95805-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95805-117">Requirement</span></span> | <span data-ttu-id="95805-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="95805-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95805-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="95805-119">Header</span></span><br/>  | <dl> <span data-ttu-id="95805-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95805-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95805-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95805-121">Library</span></span><br/> | <dl> <span data-ttu-id="95805-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95805-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95805-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95805-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95805-124">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="95805-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




