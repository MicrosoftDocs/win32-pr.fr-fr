---
description: Le convertisseur audio de streaming (SAR) est un récepteur multimédia qui restitue l’audio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Convertisseur audio de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516082"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="b2b0d-103">Convertisseur audio de streaming</span><span class="sxs-lookup"><span data-stu-id="b2b0d-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="b2b0d-104">Le convertisseur audio de streaming (SAR) est un récepteur multimédia qui restitue l’audio.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="b2b0d-105">Chaque instance du SAR affiche un flux audio unique.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="b2b0d-106">Pour afficher plusieurs flux, utilisez plusieurs instances du SAR.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="b2b0d-107">Pour créer l’SAR, appelez l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2b0d-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="b2b0d-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="b2b0d-109">Retourne un pointeur vers l’SAR.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="b2b0d-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="b2b0d-111">Retourne un pointeur vers un objet d’activation qui peut être utilisé pour créer le SAR.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="b2b0d-112">La deuxième fonction, qui retourne un objet d’activation, est requise si vous jouez du contenu protégé, car l’objet d’activation doit être sérialisé vers le processus protégé.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="b2b0d-113">Pour obtenir un contenu clair, vous pouvez utiliser l’une ou l’autre fonction.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="b2b0d-114">Le SAR peut recevoir des données audio non compressées dans un format à virgule flottante PCM ou IEEE.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="b2b0d-115">Si la vitesse de lecture est plus rapide ou plus lente que 1 ×, le SAR ajuste automatiquement le pas.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="b2b0d-116">Configuration du convertisseur audio</span><span class="sxs-lookup"><span data-stu-id="b2b0d-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="b2b0d-117">La SAR prend en charge plusieurs attributs de configuration.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="b2b0d-118">Le mécanisme de définition de ces attributs dépend de la fonction que vous appelez pour créer l’SAR.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="b2b0d-119">Si vous utilisez la fonction [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b2b0d-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="b2b0d-120">Créez un nouveau magasin d’attributs en appelant [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="b2b0d-121">Ajoutez les attributs au magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="b2b0d-122">Transmettez le magasin d’attributs à la fonction [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) dans le paramètre *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="b2b0d-123">Si vous utilisez la fonction [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , la fonction retourne un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dans le paramètre *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="b2b0d-124">Utilisez ce pointeur pour ajouter les attributs.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="b2b0d-125">Pour obtenir la liste des attributs de configuration, consultez [attributs de convertisseur audio](audio-renderer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="b2b0d-126">Sélection de l’appareil de point de terminaison audio</span><span class="sxs-lookup"><span data-stu-id="b2b0d-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="b2b0d-127">Un *périphérique de point de terminaison audio* est un périphérique matériel qui restitue ou capture l’audio.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="b2b0d-128">Par exemple, les haut-parleurs, les casques, les microphones et les lecteurs de CD.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="b2b0d-129">Le SAR utilise toujours un périphérique de rendu audio.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="b2b0d-130">Il existe deux façons de sélectionner l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-130">There are two ways to select the device.</span></span>

<span data-ttu-id="b2b0d-131">La première approche consiste à énumérer les périphériques de rendu audio sur le système, à l’aide de l’interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="b2b0d-132">Cette interface est documentée dans la documentation de l’API audio principale.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="b2b0d-133">Créez l’objet énumérateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="b2b0d-134">Utilisez l’énumérateur d’appareil pour énumérer les périphériques de rendu audio.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="b2b0d-135">Chaque appareil est représenté par un pointeur vers l’interface [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="b2b0d-136">Sélectionnez un appareil, en fonction des propriétés de l’appareil ou de la sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="b2b0d-137">Appelez [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour récupérer l’identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="b2b0d-138">Définissez l’identificateur d’appareil en tant que valeur de l’attribut ID de point de terminaison de l' [**\_ \_ attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="b2b0d-139">Au lieu d’énumérer les appareils, vous pouvez spécifier le périphérique audio par son *rôle*.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="b2b0d-140">Un rôle audio identifie une catégorie générale d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="b2b0d-141">Par exemple, le rôle de *console* est défini pour les jeux et les notifications système, tandis que le rôle *multimédia* est défini pour la musique et les films.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="b2b0d-142">Chaque rôle est associé à un périphérique de rendu audio, et l’utilisateur peut modifier ces attributions.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="b2b0d-143">Si vous spécifiez un rôle d’appareil, le SAR utilise le périphérique audio affecté à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="b2b0d-144">Pour spécifier le rôle d’appareil, définissez l’attribut de [**\_ rôle de point de \_ terminaison d’attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="b2b0d-145">Les deux attributs répertoriés dans cette section s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="b2b0d-146">Si vous ne définissez pas l’un d’eux, le SAR utilise le périphérique audio affecté au rôle **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="b2b0d-147">Le code suivant énumère les périphériques de rendu audio et attribue le premier périphérique de la liste à la région SAR.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="b2b0d-148">Cet exemple utilise la fonction [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) pour créer l’SAR.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="b2b0d-149">Pour créer l’objet d’activation pour le SAR, modifiez le code qui s’affiche après l’appel à [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="b2b0d-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="b2b0d-150">Sélection de la session audio</span><span class="sxs-lookup"><span data-stu-id="b2b0d-150">Selecting the Audio Session</span></span>

<span data-ttu-id="b2b0d-151">Une session audio est un groupe de flux audio associés qu’une application peut gérer collectivement.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="b2b0d-152">L’application peut contrôler le niveau de volume et l’état de silence de chaque session.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="b2b0d-153">Les sessions sont identifiées par un GUID.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="b2b0d-154">Pour spécifier la session audio pour le SAR, utilisez l’attribut d’ID de session de l' [ \_ \_ attribut de convertisseur \_ \_ \_ audio MF](mf-audio-renderer-attribute-session-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="b2b0d-155">Si vous ne définissez pas cet attribut, le SAR rejoint la session par défaut pour ce processus, identifiée par le **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="b2b0d-156">Par défaut, une session audio est spécifique au processus, ce qui signifie qu’elle contient uniquement des flux du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="b2b0d-157">Pour joindre une session inter-processus, définissez l' [attribut \_ \_ \_ \_ indicateurs d’attribut de convertisseur audio MF](mf-audio-renderer-attribute-flags-attribute.md) avec les **indicateurs d’attribut de \_ rendu audio MF \_ \_ \_ \_ CROSSPROCESS**.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="b2b0d-158">Après avoir créé l’SAR, vous utilisez l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pour joindre la session à un groupe de sessions, toutes contrôlées par le même contrôle de volume dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="b2b0d-159">Vous pouvez également utiliser cette interface pour définir le nom d’affichage et l’icône qui s’affichent dans le contrôle du volume.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="b2b0d-160">Contrôle des niveaux de volume</span><span class="sxs-lookup"><span data-stu-id="b2b0d-160">Controlling Volume Levels</span></span>

<span data-ttu-id="b2b0d-161">Pour contrôler le niveau de volume maître de tous les flux dans la session audio de l’SAR, utilisez l’interface [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="b2b0d-162">Pour contrôler le volume d’un flux individuel, ou pour contrôler le volume de canaux individuels dans un flux, utilisez l’interface [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) .</span><span class="sxs-lookup"><span data-stu-id="b2b0d-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="b2b0d-163">Les deux interfaces sont obtenues en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span><span class="sxs-lookup"><span data-stu-id="b2b0d-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="b2b0d-164">Vous pouvez appeler **GetService** directement sur le SAR ou l’appeler sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="b2b0d-165">Les niveaux de volume sont exprimés en tant que valeurs d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="b2b0d-166">Pour chaque canal, le niveau d’atténuation est le produit du volume maître et du volume de canal.</span><span class="sxs-lookup"><span data-stu-id="b2b0d-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2b0d-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2b0d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2b0d-168">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="b2b0d-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
