---
description: À propos de l’API MMDevice
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: À propos de l’API MMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748780"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="fcc67-103">À propos de l’API MMDevice</span><span class="sxs-lookup"><span data-stu-id="fcc67-103">About MMDevice API</span></span>

<span data-ttu-id="fcc67-104">L’API Windows Multimedia Device (MMDevice) permet aux clients audio de découvrir des [périphériques de point de terminaison audio](audio-endpoint-devices.md), de déterminer leurs fonctionnalités et de créer des instances de pilote pour ces appareils.</span><span class="sxs-lookup"><span data-stu-id="fcc67-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="fcc67-105">Le fichier d’en-tête MMDeviceAPI. h définit les interfaces dans l’API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="fcc67-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="fcc67-106">L’API MMDevice est constituée de plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="fcc67-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="fcc67-107">La première est l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="fcc67-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="fcc67-108">Pour accéder aux interfaces dans l’API MMDevice, un client obtient une référence à l’interface **IMMDeviceEnumerator** d’un objet d’énumérateur d’appareil en appelant la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , comme indiqué dans le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="fcc67-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="fcc67-109">Dans le fragment de code précédent, CLSID \_ MMDeviceEnumerator et IID \_ IMMDeviceEnumerator sont les valeurs GUID jointes en tant qu’attributs à l’objet de classe **MMDeviceEnumerator** et à l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="fcc67-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="fcc67-110">L’appel [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) passe ces valeurs par référence.</span><span class="sxs-lookup"><span data-stu-id="fcc67-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="fcc67-111">`hr`La variable est de type **HRESULT** et `pEnumerator` la variable est un pointeur vers l’interface **IMMDeviceEnumerator** d’un objet d’énumérateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="fcc67-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="fcc67-112">**IMMDeviceEnumerator** fournit des méthodes pour énumérer les appareils de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="fcc67-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="fcc67-113">Pour plus d’informations sur l’opérateur **\_ \_ uuidof** , la fonction **CoCreateInstance** et les \_ constantes CLSCTX *xxx* , consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fcc67-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="fcc67-114">Par le biais de l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , le client peut obtenir des références aux autres interfaces dans l’API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="fcc67-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="fcc67-115">L’API MMDevice implémente les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="fcc67-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="fcc67-116">Interface</span><span class="sxs-lookup"><span data-stu-id="fcc67-116">Interface</span></span>                                          | <span data-ttu-id="fcc67-117">Description</span><span class="sxs-lookup"><span data-stu-id="fcc67-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="fcc67-118">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="fcc67-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="fcc67-119">Représente un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="fcc67-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="fcc67-120">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="fcc67-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="fcc67-121">Représente une collection de périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="fcc67-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="fcc67-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="fcc67-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="fcc67-123">Fournit des méthodes pour énumérer des périphériques audio.</span><span class="sxs-lookup"><span data-stu-id="fcc67-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="fcc67-124">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="fcc67-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="fcc67-125">Représente un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="fcc67-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="fcc67-126">En outre, les clients de l’API MMDevice qui requièrent la notification des modifications d’État dans les appareils de point de terminaison audio doivent implémenter l’interface suivante.</span><span class="sxs-lookup"><span data-stu-id="fcc67-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="fcc67-127">Interface</span><span class="sxs-lookup"><span data-stu-id="fcc67-127">Interface</span></span>                                              | <span data-ttu-id="fcc67-128">Description</span><span class="sxs-lookup"><span data-stu-id="fcc67-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcc67-129">**IMMNotificationClient**</span><span class="sxs-lookup"><span data-stu-id="fcc67-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="fcc67-130">Fournit des notifications lorsqu’un périphérique de point de terminaison audio est ajouté ou supprimé, lorsque l’État ou les propriétés d’un appareil change ou lorsqu’un changement du rôle par défaut est affecté à un appareil.</span><span class="sxs-lookup"><span data-stu-id="fcc67-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fcc67-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcc67-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcc67-132">Périphériques de point de terminaison audio</span><span class="sxs-lookup"><span data-stu-id="fcc67-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="fcc67-133">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="fcc67-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
