---
description: Cet article explique comment mettre à jour une implémentation de WASAPI pour tirer parti du routage de flux automatique.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Routage de flux automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950835"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="da7de-103">Routage de flux automatique</span><span class="sxs-lookup"><span data-stu-id="da7de-103">Automatic Stream Routing</span></span>

<span data-ttu-id="da7de-104">Cet article explique comment mettre à jour une implémentation de WASAPI pour tirer parti du routage de flux automatique.</span><span class="sxs-lookup"><span data-stu-id="da7de-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="da7de-105">À compter de Windows 7, chaque fois que le périphérique audio par défaut change, le flux de lecture audio d’une application est transféré en toute transparence du périphérique audio par défaut précédent vers le nouveau périphérique audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="da7de-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="da7de-106">Ce transfert se produit automatiquement sans code d’application supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="da7de-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="da7de-107">Toutefois, avant Windows 10, version 1607, les applications qui utilisaient l’API de session audio Windows (WASAPI) de bas niveau ne pouvaient pas participer à cette fonctionnalité de routage de flux automatisé.</span><span class="sxs-lookup"><span data-stu-id="da7de-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="da7de-108">Les applications utilisant WASAPI devaient implémenter leur propre forme de routage de flux en ajoutant du code supplémentaire pour détecter l’arrivée et la suppression des périphériques audio et basculer le flux vers ces appareils, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="da7de-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="da7de-109">Les applications qui utilisent des WASAPI qui n’implémentent pas leur propre mécanisme de routage de flux sur l’arrivée ou la suppression d’un appareil a risqué de fournir une expérience utilisateur moins que idéale.</span><span class="sxs-lookup"><span data-stu-id="da7de-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="da7de-110">Depuis la version 1607 de Windows 10, les applications qui utilisent WASAPI peuvent tirer parti du routage de flux automatique.</span><span class="sxs-lookup"><span data-stu-id="da7de-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="da7de-111">Si votre application utilise WASAPI, il est vivement recommandé de mettre à jour votre application pour tirer parti de cette nouvelle fonctionnalité en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="da7de-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="da7de-112">Windows 10, version 1607, définit deux nouveaux GUID qui peuvent être utilisés pour activer un rendu audio ou une interface de capture avec routage de flux automatique, le [ \_ \_ rendu audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids) et la [ \_ \_ capture audio DEVINTERFACE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span><span class="sxs-lookup"><span data-stu-id="da7de-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="da7de-113">Obtenir une représentation sous forme de chaîne de ces GUID en appelant [**échec stringfromiid**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span><span class="sxs-lookup"><span data-stu-id="da7de-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="da7de-114">L’exemple suivant illustre cet appel pour le GUID de rendu audio.</span><span class="sxs-lookup"><span data-stu-id="da7de-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="da7de-115">Activez le point de terminaison audio en passant la chaîne d’identificateur à la fonction WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) .</span><span class="sxs-lookup"><span data-stu-id="da7de-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="da7de-116">L’exemple suivant passe dans l’identificateur de rendu audio obtenu à l’étape 1 :</span><span class="sxs-lookup"><span data-stu-id="da7de-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="da7de-117">Libérez la mémoire allouée pour conserver l’identificateur de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="da7de-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="da7de-118">Une fois que vous avez modifié votre application pour activer l’interface audio de la manière décrite ci-dessus, elle participera à la fonctionnalité de routage de flux automatique.</span><span class="sxs-lookup"><span data-stu-id="da7de-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="da7de-119">Pour illustrer le routage automatique du flux, utilisez un ordinateur portable ou une tablette équipée de haut-parleurs internes pour lire les données audio.</span><span class="sxs-lookup"><span data-stu-id="da7de-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="da7de-120">Vous devez entendre la lecture audio via les intervenants internes de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="da7de-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="da7de-121">Pendant la lecture audio, connectez une paire de casque.</span><span class="sxs-lookup"><span data-stu-id="da7de-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="da7de-122">Vous devez maintenant entendre la lecture audio dans le casque.</span><span class="sxs-lookup"><span data-stu-id="da7de-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="da7de-123">Ensuite, débranchez le casque et l’audio doivent automatiquement être redirigés vers les haut-parleurs internes.</span><span class="sxs-lookup"><span data-stu-id="da7de-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da7de-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da7de-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da7de-125">Routage de flux</span><span class="sxs-lookup"><span data-stu-id="da7de-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="da7de-126">**MediaDevice.GetDefaultAudioRenderId**</span><span class="sxs-lookup"><span data-stu-id="da7de-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="da7de-127">**MediaDevice.GetDefaultAudioCaptureId**</span><span class="sxs-lookup"><span data-stu-id="da7de-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="da7de-128">**ActivateAudioInterfaceAsync**</span><span class="sxs-lookup"><span data-stu-id="da7de-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
