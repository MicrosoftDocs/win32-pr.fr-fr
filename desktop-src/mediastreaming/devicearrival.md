---
title: Événement DeviceArrival
description: Se produit lorsqu’un nouvel appareil est ajouté à la liste des appareils retournés par la méthode CachedDevices.
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- API de diffusion de contenu multimédia d’événements DeviceArrival
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79fbdd68ae6c77c6a0f3e7bbd3cf976b5d056987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725396"
---
# <a name="devicearrival-event"></a><span data-ttu-id="9fddc-104">Événement DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="9fddc-104">DeviceArrival event</span></span>

<span data-ttu-id="9fddc-105">Se produit lorsqu’un nouvel appareil est ajouté à la liste des appareils retournés par la méthode [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="9fddc-105">Occurs when a new device is added to the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fddc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fddc-106">Syntax</span></span>


```C++
void DeviceArrival();
```



## <a name="parameters"></a><span data-ttu-id="9fddc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fddc-107">Parameters</span></span>

<span data-ttu-id="9fddc-108">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9fddc-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fddc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fddc-109">Return value</span></span>

<span data-ttu-id="9fddc-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9fddc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fddc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9fddc-111">Remarks</span></span>

<span data-ttu-id="9fddc-112">Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) à l’aide de la méthode [**Add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="9fddc-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival) method.</span></span> <span data-ttu-id="9fddc-113">Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) .</span><span class="sxs-lookup"><span data-stu-id="9fddc-113">To unregister the event handler, use the [**remove\_DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) method.</span></span>

 

 