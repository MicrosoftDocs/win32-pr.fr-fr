---
title: Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau
description: Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 pour les périphériques réseau
- Windows Media Format SDK, DRM 10 pour les périphériques réseau
- ASF (Advanced Systems Format), Windows Media DRM 10 pour les périphériques réseau
- ASF (format avancé des systèmes), Windows Media DRM 10 pour les périphériques réseau
- ASF (Advanced Systems Format), DRM 10 pour les périphériques réseau
- ASF (format de systèmes avancés), DRM 10 pour les périphériques réseau
- gestion des droits numériques (DRM), Windows Media DRM 10 pour les périphériques réseau
- DRM (gestion des droits numériques), Windows Media DRM 10 pour les périphériques réseau
- gestion des droits numériques (DRM), DRM 10 pour les périphériques réseau
- DRM (gestion des droits numériques), DRM 10 pour les périphériques réseau
- Windows Media DRM 10 pour les périphériques réseau, protocoles
- DRM 10 pour les périphériques réseau, protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309886"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a><span data-ttu-id="782f2-115">Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="782f2-115">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>

<span data-ttu-id="782f2-116">Le kit de développement logiciel (SDK) du format Windows Media fournit certaines fonctionnalités pour prendre en charge le protocole de périphérique réseau sécurisé, Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="782f2-116">The Windows Media Format SDK provides some features to support the secure network device protocol, Windows Media DRM 10 for Network Devices.</span></span> <span data-ttu-id="782f2-117">Ce protocole définit les messages envoyés entre un périphérique de lecture multimédia numérique, tel qu’un lecteur vidéo en haut de la série, et l’ordinateur qui sert les données à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="782f2-117">This protocol defines the messages sent between a digital media playback device, such as a set-top video player, and the computer that serves data to the device.</span></span> <span data-ttu-id="782f2-118">Les données multimédia envoyées entre le serveur et l’appareil sont chiffrées pour empêcher l’interception.</span><span class="sxs-lookup"><span data-stu-id="782f2-118">The media data sent between server and device is encrypted to protect it from interception.</span></span>

<span data-ttu-id="782f2-119">La communication entre votre application et les appareils qui prennent en charge Windows Media DRM 10 pour les périphériques réseau peut utiliser les protocoles de mise en réseau que vous préférez.</span><span class="sxs-lookup"><span data-stu-id="782f2-119">The communication between your application and devices that support Windows Media DRM 10 for Network Devices can use whatever networking protocols you prefer.</span></span> <span data-ttu-id="782f2-120">Le kit de développement logiciel (SDK) Windows Media format ne fournit pas d’objets qui effectuent les communications réseau pour vous.</span><span class="sxs-lookup"><span data-stu-id="782f2-120">The Windows Media Format SDK does not provide any objects that perform the network communications for you.</span></span> <span data-ttu-id="782f2-121">Au lieu de cela, les objets de ce SDK traitent les messages de Windows Media DRM 10 pour les périphériques réseau une fois que votre application les a reçus.</span><span class="sxs-lookup"><span data-stu-id="782f2-121">Instead, the objects of this SDK process some Windows Media DRM 10 for Network Devices messages after your application has received them.</span></span>

<span data-ttu-id="782f2-122">Les fonctionnalités qui prennent en charge Windows Media DRM 10 pour les périphériques réseau sont l’inscription des appareils, la détection de proximité et la conversion des fichiers protégés par DRM.</span><span class="sxs-lookup"><span data-stu-id="782f2-122">The features that support Windows Media DRM 10 for Network Devices are device registration, proximity detection, and converting DRM-protected files.</span></span> <span data-ttu-id="782f2-123">Ces fonctionnalités sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="782f2-123">These features are described in the following sections.</span></span>



| <span data-ttu-id="782f2-124">Section</span><span class="sxs-lookup"><span data-stu-id="782f2-124">Section</span></span>                                                                                                                                                                          | <span data-ttu-id="782f2-125">Description</span><span class="sxs-lookup"><span data-stu-id="782f2-125">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="782f2-126">Inscription de l’appareil</span><span class="sxs-lookup"><span data-stu-id="782f2-126">Device Registration</span></span>](device-registration.md)                                                                                                                                   | <span data-ttu-id="782f2-127">Décrit comment traiter les messages de demande d’inscription à partir d’appareils.</span><span class="sxs-lookup"><span data-stu-id="782f2-127">Describes how to process registration request messages from devices.</span></span>                                                                       |
| [<span data-ttu-id="782f2-128">Détection de proximité en cours</span><span class="sxs-lookup"><span data-stu-id="782f2-128">Performing Proximity Detection</span></span>](performing-proximity-detection.md)                                                                                                             | <span data-ttu-id="782f2-129">Décrit le processus de détection de proximité.</span><span class="sxs-lookup"><span data-stu-id="782f2-129">Describes the proximity detection process.</span></span>                                                                                                 |
| [<span data-ttu-id="782f2-130">Conversion d’un fichier de DRM-Protected en un flux Windows Media DRM 10 pour les périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="782f2-130">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | <span data-ttu-id="782f2-131">Décrit comment convertir un fichier protégé par DRM en un flux qui peut être envoyé à un appareil qui utilise Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="782f2-131">Describes how to convert a DRM-protected file to a stream that can be sent to a device that uses Windows Media DRM 10 for Network Devices.</span></span> |



 

> [!Note]  
> <span data-ttu-id="782f2-132">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="782f2-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="782f2-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="782f2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="782f2-134">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="782f2-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




