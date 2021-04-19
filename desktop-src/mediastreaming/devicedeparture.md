---
title: Événement DeviceDeparture
description: Se produit lorsqu’un nouvel appareil est supprimé de la liste des appareils retournés par la méthode CachedDevices.
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- API de diffusion de contenu multimédia d’événements DeviceDeparture
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511683"
---
# <a name="devicedeparture-event"></a><span data-ttu-id="ceace-104">Événement DeviceDeparture</span><span class="sxs-lookup"><span data-stu-id="ceace-104">DeviceDeparture event</span></span>

<span data-ttu-id="ceace-105">Se produit lorsqu’un nouvel appareil est supprimé de la liste des appareils retournés par la méthode [**CachedDevices**](idevicecontroller-cacheddevices.md) .</span><span class="sxs-lookup"><span data-stu-id="ceace-105">Occurs when a new device is removed from the list of devices returned by the [**CachedDevices**](idevicecontroller-cacheddevices.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceace-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ceace-106">Syntax</span></span>


```C++
void DeviceDeparture();
```



## <a name="parameters"></a><span data-ttu-id="ceace-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ceace-107">Parameters</span></span>

<span data-ttu-id="ceace-108">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ceace-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ceace-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ceace-109">Return value</span></span>

<span data-ttu-id="ceace-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ceace-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceace-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ceace-111">Remarks</span></span>

<span data-ttu-id="ceace-112">Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) à l’aide de la méthode [**Add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="ceace-112">To handle notifications from this event, register a [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85)) event handler function using the [**add\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture) method.</span></span> <span data-ttu-id="ceace-113">Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) .</span><span class="sxs-lookup"><span data-stu-id="ceace-113">To unregister the event handler, use the [**remove\_DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) method.</span></span>

 

 