---
description: La méthode Disconnect interrompt la connexion de code confidentiel actuelle. Cette méthode implémente la méthode IPin ::D éconnecter.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: CBasePin. Disconnect, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540336"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="656b3-104">CBasePin. Disconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="656b3-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="656b3-105">La `Disconnect` méthode interrompt la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="656b3-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="656b3-106">Cette méthode implémente la méthode [**IPIN ::D éconnecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="656b3-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="656b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="656b3-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="656b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="656b3-108">Parameters</span></span>

<span data-ttu-id="656b3-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="656b3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="656b3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="656b3-110">Return value</span></span>

<span data-ttu-id="656b3-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="656b3-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="656b3-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="656b3-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="656b3-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="656b3-113">Return code</span></span>                                                                                         | <span data-ttu-id="656b3-114">Description</span><span class="sxs-lookup"><span data-stu-id="656b3-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="656b3-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="656b3-116">Le pin n’était pas connecté.</span><span class="sxs-lookup"><span data-stu-id="656b3-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="656b3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="656b3-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="656b3-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="656b3-119"><dt>**VFW \_ E \_ non \_ arrêté**</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="656b3-120">Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="656b3-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="656b3-121">Notes</span><span class="sxs-lookup"><span data-stu-id="656b3-121">Remarks</span></span>

<span data-ttu-id="656b3-122">La classe de base délègue la majeure partie du travail à la méthode [**CBasePin ::D isconnectinternal**](cbasepin-disconnectinternal.md) .</span><span class="sxs-lookup"><span data-stu-id="656b3-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="656b3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="656b3-123">Requirements</span></span>



| <span data-ttu-id="656b3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="656b3-124">Requirement</span></span> | <span data-ttu-id="656b3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="656b3-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656b3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="656b3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="656b3-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="656b3-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="656b3-128">Library</span></span><br/> | <dl> <span data-ttu-id="656b3-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656b3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="656b3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656b3-131">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="656b3-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




