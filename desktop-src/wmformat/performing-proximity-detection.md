---
title: Détection de proximité en cours
description: Détection de proximité en cours
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media Format SDK, détection de proximité
- Windows Media Format SDK, détection de proximité
- ASF (Advanced Systems Format), en effectuant la détection de proximité
- ASF (format avancé des systèmes), exécution de la détection de proximité
- ASF (Advanced Systems Format), détection de proximité
- ASF (format de systèmes avancés), détection de proximité
- gestion des droits numériques (DRM), réalisation de la détection de proximité
- DRM (Digital Rights Management), réalisation de la détection de proximité
- gestion des droits numériques (DRM), détection de proximité
- DRM (gestion des droits numériques), détection de proximité
- détection de proximité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381465"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="1fd91-114">Détection de proximité en cours</span><span class="sxs-lookup"><span data-stu-id="1fd91-114">Performing Proximity Detection</span></span>

<span data-ttu-id="1fd91-115">Avant de pouvoir diffuser en continu des données chiffrées sur un appareil inscrit dans le protocole Windows Media DRM 10 pour les périphériques réseau, vous devez effectuer un processus appelé détection de proximité (également appelé validation).</span><span class="sxs-lookup"><span data-stu-id="1fd91-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="1fd91-116">Ce processus implique l’envoi de messages à l’appareil et la réception de réponses.</span><span class="sxs-lookup"><span data-stu-id="1fd91-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="1fd91-117">Le temps nécessaire à la réception d’une réponse est utilisé pour déterminer si l’appareil est suffisamment « proche » de l’ordinateur sur le réseau pour recevoir des données sécurisées.</span><span class="sxs-lookup"><span data-stu-id="1fd91-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="1fd91-118">En confirmant que l’appareil est physiquement proche de l’ordinateur client sur le réseau, vous pouvez empêcher l’usurpation d’identité et d’autres accès non autorisés.</span><span class="sxs-lookup"><span data-stu-id="1fd91-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="1fd91-119">Lorsque la détection de proximité s’est terminée avec succès, l’appareil est considéré comme valide.</span><span class="sxs-lookup"><span data-stu-id="1fd91-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="1fd91-120">Vous pouvez vérifier si un appareil est valide en appelant la méthode [**IWMRegisteredDevice :: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) .</span><span class="sxs-lookup"><span data-stu-id="1fd91-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="1fd91-121">Les appareils doivent être validés toutes les 48 heures.</span><span class="sxs-lookup"><span data-stu-id="1fd91-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="1fd91-122">Un appareil qui a été validé plus de 48 heures avant l’exécution de votre programme doit être revalidé en effectuant à nouveau le processus de détection de proximité.</span><span class="sxs-lookup"><span data-stu-id="1fd91-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="1fd91-123">Pour effectuer la détection de proximité, vous devez établir des communications avec l’appareil, puis appeler la méthode [**IWMProximityDetection :: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) .</span><span class="sxs-lookup"><span data-stu-id="1fd91-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="1fd91-124">Le processus de détection est exécuté de façon asynchrone par les composants DRM internes du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1fd91-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="1fd91-125">Votre application doit inclure une implémentation de l’interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) pour traiter les messages de détection de proximité.</span><span class="sxs-lookup"><span data-stu-id="1fd91-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="1fd91-126">Deux messages sont envoyés par le processus de détection de proximité : un message de résultat et un message d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="1fd91-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="1fd91-127">Le message de résultat, le \_ résultat de proximité WMT \_ , est envoyé lorsque le processus de détection est terminé.</span><span class="sxs-lookup"><span data-stu-id="1fd91-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="1fd91-128">Le paramètre *HR* de la méthode de rappel [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indique si l’appareil est suffisamment proche de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="1fd91-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="1fd91-129">Si le paramètre *HR* du message de résultat indique une réussite, le paramètre *PValue* contient une **valeur DWORD** qui spécifie la latence mesurée sur le périphérique en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="1fd91-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="1fd91-130">Le message d’achèvement, la \_ proximité WMT \_ terminée, est envoyé lorsque la détection est finalisée.</span><span class="sxs-lookup"><span data-stu-id="1fd91-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="1fd91-131">Vous ne devez libérer l’interface [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) qu’après avoir reçu ce message.</span><span class="sxs-lookup"><span data-stu-id="1fd91-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="1fd91-132">Lorsque la détection de proximité d’un appareil est réussie, la base de données d’inscription des appareils est automatiquement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="1fd91-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="1fd91-133">Les appels suivants à [**IWMRegisteredDevice :: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) retournent la **valeur TRUE** jusqu’à 48 heures, et l’appareil doit être revalidé.</span><span class="sxs-lookup"><span data-stu-id="1fd91-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="1fd91-134">**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="1fd91-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd91-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fd91-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd91-136">**Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau**</span><span class="sxs-lookup"><span data-stu-id="1fd91-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




