---
title: Comment inscrire un appareil auprès de l’hôte de l’appareil
description: Vous pouvez inscrire un appareil en cours d’exécution ou un périphérique non en cours d’exécution.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029249"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="4649c-103">Comment inscrire un appareil auprès de l’hôte de l’appareil</span><span class="sxs-lookup"><span data-stu-id="4649c-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="4649c-104">Vous pouvez inscrire un appareil en cours d’exécution ou un périphérique non en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4649c-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="4649c-105">Inscription d’un appareil en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="4649c-105">Registering a Running Device</span></span>

<span data-ttu-id="4649c-106">Les appareils sont inscrits à l’aide de l’interface [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) .</span><span class="sxs-lookup"><span data-stu-id="4649c-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="4649c-107">Seuls les administrateurs sont autorisés à inscrire des appareils en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4649c-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="4649c-108">Pour inscrire un appareil disposant d’un objet contrôle d’appareil en cours d’exécution, une application doit appeler [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), en passant ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="4649c-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="4649c-109">Texte de la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4649c-109">The text of the device's description.</span></span>
-   <span data-ttu-id="4649c-110">Pointeur **IUnknown** vers l’objet de contrôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4649c-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="4649c-111">Chaîne d’initialisation qui est transmise à la méthode [**IUPnPDeviceControl :: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) de l’objet de contrôle de périphérique.</span><span class="sxs-lookup"><span data-stu-id="4649c-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="4649c-112">Emplacement du répertoire de ressources.</span><span class="sxs-lookup"><span data-stu-id="4649c-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="4649c-113">Durée de vie de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4649c-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="4649c-114">Le paramètre d’ID d’appareil (paramètre OUT), qui est la valeur de retour de cet appel ; un pointeur vers l’ID d’appareil est retourné en C++.</span><span class="sxs-lookup"><span data-stu-id="4649c-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="4649c-115">Inscription d’un appareil non en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="4649c-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="4649c-116">Par défaut, seuls les administrateurs et les utilisateurs interactifs sont autorisés à inscrire des appareils non en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4649c-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="4649c-117">Pour inscrire un appareil auprès d’un objet de contrôle d’appareil qui n’est pas en cours d’exécution, l’application utilise la méthode [**IUPnPRegistrar :: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .</span><span class="sxs-lookup"><span data-stu-id="4649c-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="4649c-118">Pour inscrire un appareil par programme avec un objet de contrôle de périphérique non en cours d’exécution, l’application doit appeler [**IUPnPRegistrar :: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) et lui transmettre les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4649c-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="4649c-119">Texte de la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4649c-119">The text of the device's description.</span></span>
-   <span data-ttu-id="4649c-120">ProgID de l’objet de contrôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4649c-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="4649c-121">Chaîne d’initialisation qui est transmise à la méthode [**IUPnPDeviceControl :: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) de l’objet de contrôle de périphérique.</span><span class="sxs-lookup"><span data-stu-id="4649c-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="4649c-122">ID de conteneur.</span><span class="sxs-lookup"><span data-stu-id="4649c-122">A container ID.</span></span>
-   <span data-ttu-id="4649c-123">Emplacement du répertoire de ressources.</span><span class="sxs-lookup"><span data-stu-id="4649c-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="4649c-124">Durée de vie de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4649c-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="4649c-125">Le paramètre d’ID d’appareil (paramètre OUT), qui est la valeur de retour de cet appel ; un pointeur vers l’ID d’appareil est retourné en C++.</span><span class="sxs-lookup"><span data-stu-id="4649c-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="4649c-126">Les inscriptions des appareils non exécutés peuvent être configurées pour être conservées au cours des démarrages du système (les appareils ne sont pas publiés durant la phase d’arrêt).</span><span class="sxs-lookup"><span data-stu-id="4649c-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="4649c-127">Par conséquent, s’ils sont configurés de cette façon, les appareils sont publiés et annoncés à chaque démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4649c-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




