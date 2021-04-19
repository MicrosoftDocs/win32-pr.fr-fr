---
description: La méthode DisconnectInternal interrompt la connexion de code confidentiel actuelle.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Méthode CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529881"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="64fb2-103">Méthode CBasePin. DisconnectInternal</span><span class="sxs-lookup"><span data-stu-id="64fb2-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="64fb2-104">La `DisconnectInternal` méthode interrompt la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="64fb2-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="64fb2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64fb2-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="64fb2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64fb2-106">Parameters</span></span>

<span data-ttu-id="64fb2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="64fb2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64fb2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64fb2-108">Return value</span></span>

<span data-ttu-id="64fb2-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64fb2-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="64fb2-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="64fb2-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="64fb2-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="64fb2-111">Return code</span></span>                                                                                         | <span data-ttu-id="64fb2-112">Description</span><span class="sxs-lookup"><span data-stu-id="64fb2-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64fb2-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="64fb2-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="64fb2-114">Le pin n’était pas connecté.</span><span class="sxs-lookup"><span data-stu-id="64fb2-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="64fb2-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64fb2-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="64fb2-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="64fb2-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="64fb2-117"><dt>**VFW \_ E \_ non \_ arrêté**</dt></span><span class="sxs-lookup"><span data-stu-id="64fb2-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="64fb2-118">Le filtre est actif et le code confidentiel ne prend pas en charge la reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="64fb2-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="64fb2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="64fb2-119">Remarks</span></span>

<span data-ttu-id="64fb2-120">La méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) délègue le processus de déconnexion à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="64fb2-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="64fb2-121">Cette méthode appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="64fb2-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="64fb2-122">Elle libère également le décompte de références sur l’autre code confidentiel, qui est détenu par la variable membre [**\_ connectée CBasePin :: m**](cbasepin-m-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="64fb2-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="64fb2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64fb2-123">Requirements</span></span>



| <span data-ttu-id="64fb2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64fb2-124">Requirement</span></span> | <span data-ttu-id="64fb2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="64fb2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64fb2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="64fb2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="64fb2-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64fb2-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="64fb2-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64fb2-128">Library</span></span><br/> | <dl> <span data-ttu-id="64fb2-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="64fb2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64fb2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64fb2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64fb2-131">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="64fb2-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




