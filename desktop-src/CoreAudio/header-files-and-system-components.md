---
description: Fichiers d’en-tête et composants système
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Fichiers d’en-tête et composants système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424289"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="e13a3-103">Fichiers d’en-tête et composants système</span><span class="sxs-lookup"><span data-stu-id="e13a3-103">Header Files and System Components</span></span>

<span data-ttu-id="e13a3-104">Le tableau suivant répertorie les fichiers d’en-tête qui contiennent les définitions d’interface des quatre principaux composants audio.</span><span class="sxs-lookup"><span data-stu-id="e13a3-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



| <span data-ttu-id="e13a3-105">Composant audio principal</span><span class="sxs-lookup"><span data-stu-id="e13a3-105">Core Audio component</span></span>                         | <span data-ttu-id="e13a3-106">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e13a3-106">Header file</span></span>                  |
|----------------------------------------------|------------------------------|
| [<span data-ttu-id="e13a3-107">API MMDevice</span><span class="sxs-lookup"><span data-stu-id="e13a3-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="e13a3-108">MMDeviceAPI. h</span><span class="sxs-lookup"><span data-stu-id="e13a3-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="e13a3-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="e13a3-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="e13a3-110">Audioclient. h, Audiopolicy. h</span><span class="sxs-lookup"><span data-stu-id="e13a3-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="e13a3-111">API DeviceTopology</span><span class="sxs-lookup"><span data-stu-id="e13a3-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="e13a3-112">Devicetopology. h</span><span class="sxs-lookup"><span data-stu-id="e13a3-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="e13a3-113">API EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="e13a3-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="e13a3-114">Endpointvolume. h</span><span class="sxs-lookup"><span data-stu-id="e13a3-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="e13a3-115">Un autre fichier d’en-tête, Audiosessiontypes. h, définit les constantes utilisées par WASAPI.</span><span class="sxs-lookup"><span data-stu-id="e13a3-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="e13a3-116">Ces fichiers d’en-tête se trouvent dans le répertoire% MSSdk% \\ include, où% MSSdk% est le répertoire racine de l’installation SDK Windows sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e13a3-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="e13a3-117">Chaque API du tableau précédent se compose d’un ensemble d’interfaces COM associées.</span><span class="sxs-lookup"><span data-stu-id="e13a3-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="e13a3-118">Étant donné que certains aspects de la diffusion audio dépendent de la faible latence et de la synchronisation précise, les implémentations des API MMDevice, WASAPI, DeviceTopology et EndpointVolume n’utilisent pas l’infrastructure Microsoft .NET ou l’environnement d’exécution managé.</span><span class="sxs-lookup"><span data-stu-id="e13a3-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="e13a3-119">Les API audio de base sont implémentées dans les composants système en mode utilisateur Audioses.dll et Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="e13a3-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="e13a3-120">Les applications clientes n’accèdent pas directement aux points d’entrée de ces dll.</span><span class="sxs-lookup"><span data-stu-id="e13a3-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="e13a3-121">Au lieu de cela, les clients appellent la fonction **CoCreateInstance** ou **CoCreateInstanceEx** pour obtenir l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) de l’objet de classe MMDeviceEnumerator.</span><span class="sxs-lookup"><span data-stu-id="e13a3-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="e13a3-122">Cet objet énumère les [périphériques de point de terminaison audio](audio-endpoint-devices.md) dans le système.</span><span class="sxs-lookup"><span data-stu-id="e13a3-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="e13a3-123">L’interface **IMMDeviceEnumerator** fait partie de l’API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="e13a3-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="e13a3-124">À partir de cette interface, les clients peuvent obtenir directement ou indirectement les autres interfaces de l’API MMDevice, y compris l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="e13a3-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="e13a3-125">**IMMDevice** représente un périphérique de point de terminaison audio particulier.</span><span class="sxs-lookup"><span data-stu-id="e13a3-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="e13a3-126">Par le biais de **IMMDevice**, les clients peuvent obtenir directement ou indirectement les interfaces spécifiques à l’appareil dans WASAPI, l’API DeviceTopology et l’API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="e13a3-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="e13a3-127">Pour plus d’informations sur **CoCreateInstance** et **CoCreateInstanceEx**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="e13a3-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="e13a3-128">Pour plus d’informations sur l’accès aux interfaces dans les API audio de base, consultez [énumération des périphériques audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="e13a3-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e13a3-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e13a3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e13a3-130">À propos des API audio Windows Core</span><span class="sxs-lookup"><span data-stu-id="e13a3-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



