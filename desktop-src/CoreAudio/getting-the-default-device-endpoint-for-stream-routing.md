---
description: Dans Windows 7, les API de plateforme de haut niveau qui utilisent des API audio de base, telles que Media Foundation, DirectSound et les API Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison audio par défaut.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtention du point de terminaison de l’appareil pour le routage du flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861206"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="5ce7b-103">Obtention du point de terminaison de l’appareil pour le routage du flux</span><span class="sxs-lookup"><span data-stu-id="5ce7b-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="5ce7b-104">Dans Windows 7, les API de plateforme de haut niveau qui utilisent des API audio de base, telles que Media Foundation, DirectSound et les API Wave, implémentent la fonctionnalité de routage de flux en gérant le basculement de flux d’un appareil existant vers un nouveau point de terminaison audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="5ce7b-105">Les applications multimédias qui utilisent ces API (par exemple, une application activant un objet **IDirectSound** ou **IBaseFilter** sur un objet [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) utilisent le comportement de routage de flux sans aucune modification de la source.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="5ce7b-106">Les API de haut niveau implémentent le routage de flux pour le point de terminaison d’appareil obtenu par le biais de [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="5ce7b-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="5ce7b-107">Si une application est diffusée sur l’appareil par défaut, la fonctionnalité de routage de flux fonctionne comme défini.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="5ce7b-108">Les flux ne sont pas basculés vers le nouvel appareil s’ils sont récupérés par un autre mécanisme, même s’ils sont identiques à ceux du périphérique par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="5ce7b-109">Une application multimédia qui utilise des API audio de base directement (client WASAPI) peut fournir une implémentation de routage de flux personnalisée pour tout périphérique de rendu ou de capture.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="5ce7b-110">Un client WASAPI peut répliquer le implémentation fourni par les API de haut niveau en le limitant aux flux ouverts sur les appareils qui sont définis en tant qu’appareil par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="5ce7b-111">Pour obtenir une référence au point de terminaison de l’appareil par défaut, le client doit appeler [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="5ce7b-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="5ce7b-112">Dans cet appel, le client doit indiquer s’il requiert un pointeur vers le périphérique de rendu par défaut ou l’appareil de capture par défaut en spécifiant le paramètre de *flux* de données.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="5ce7b-113">Le client doit également spécifier le rôle approprié pour le point de terminaison dans l’attribut **ERole** (**eConsole** ou **eCommunications**).</span><span class="sxs-lookup"><span data-stu-id="5ce7b-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="5ce7b-114">N’utilisez pas **eMultimedia**.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="5ce7b-115">Si l’application est diffusée sur un autre appareil, l’application peut l’extraire en spécifiant une chaîne d’ID de point de terminaison (en appelant [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span><span class="sxs-lookup"><span data-stu-id="5ce7b-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="5ce7b-116">Une fois l’appareil identifié, le client WASAPI peut fournir l’implémentation du routage de flux en gérant les notifications d’appareil et de session audio envoyées pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5ce7b-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="5ce7b-117">Pour plus d’informations sur ces notifications, consultez [notifications pertinentes pour le routage de flux](relevant-device-notifications-for-stream-routing.md).</span><span class="sxs-lookup"><span data-stu-id="5ce7b-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ce7b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ce7b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce7b-119">À propos de l’API MMDevice</span><span class="sxs-lookup"><span data-stu-id="5ce7b-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="5ce7b-120">À propos de WASAPI</span><span class="sxs-lookup"><span data-stu-id="5ce7b-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="5ce7b-121">Routage de flux</span><span class="sxs-lookup"><span data-stu-id="5ce7b-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



