---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Annule l’inscription d’une notification que vous avez inscrite précédemment pour.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382447"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="dce1d-103">IDXCoreAdapterFactory :: UnregisterEventNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="dce1d-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="dce1d-104">Annule l’inscription d’une notification que vous avez inscrite précédemment pour.</span><span class="sxs-lookup"><span data-stu-id="dce1d-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="dce1d-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="dce1d-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dce1d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dce1d-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="dce1d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dce1d-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="dce1d-108">eventCookie</span><span class="sxs-lookup"><span data-stu-id="dce1d-108">eventCookie</span></span>

<span data-ttu-id="dce1d-109">Type : **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="dce1d-109">Type: **uint32_t**</span></span>

<span data-ttu-id="dce1d-110">Valeur de cookie (retournée quand vous avez appelé [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) qui représente une inscription antérieure pour laquelle vous souhaitez annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="dce1d-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="dce1d-111">Retours</span><span class="sxs-lookup"><span data-stu-id="dce1d-111">Returns</span></span>

<span data-ttu-id="dce1d-112">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="dce1d-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="dce1d-113">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="dce1d-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="dce1d-114">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="dce1d-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="dce1d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dce1d-115">Return value</span></span>|<span data-ttu-id="dce1d-116">Description</span><span class="sxs-lookup"><span data-stu-id="dce1d-116">Description</span></span>|
|-|-|
|<span data-ttu-id="dce1d-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dce1d-117">E_INVALIDARG</span></span>|<span data-ttu-id="dce1d-118">La valeur de *eventCookie* n’est pas un cookie valide représentant une inscription antérieure.</span><span class="sxs-lookup"><span data-stu-id="dce1d-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dce1d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="dce1d-119">Remarks</span></span>

<span data-ttu-id="dce1d-120">**UnregisterEventNotification** retourne uniquement une fois que tous les rappels en attente/en cours pour cette inscription sont terminés.</span><span class="sxs-lookup"><span data-stu-id="dce1d-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="dce1d-121">DXCore garantit qu’aucun nouveau rappel ne se produira pour cette inscription après que **UnregisterEventNotification** a retourné.</span><span class="sxs-lookup"><span data-stu-id="dce1d-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="dce1d-122">Toutefois, pour éviter un blocage, si vous appelez **UnregisterEventNotification** à partir de votre rappel, **UnregisterEventNotification** n’attend pas que le rappel actif se termine.</span><span class="sxs-lookup"><span data-stu-id="dce1d-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dce1d-123">Avant de détruire l’objet DXCore représenté par l’argument *dxCoreObject* passé à [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), vous devez utiliser la valeur cookie pour annuler l’inscription de cet objet dans les notifications en appelant **UnregisterEventNotification**.</span><span class="sxs-lookup"><span data-stu-id="dce1d-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="dce1d-124">Si vous ne le faites pas, une exception irrécupérable est générée lorsque la situation est détectée.</span><span class="sxs-lookup"><span data-stu-id="dce1d-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="dce1d-125">Une fois que vous annulez l’inscription d’une valeur de cookie, cette valeur peut ensuite être retournée par une inscription suivante</span><span class="sxs-lookup"><span data-stu-id="dce1d-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="dce1d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dce1d-126">See also</span></span>

<span data-ttu-id="dce1d-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [à l’aide de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="dce1d-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>