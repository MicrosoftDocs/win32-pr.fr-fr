---
description: Microsoft Media Foundation prend en charge la capture audio et vidéo.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Capture audio/vidéo en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525800"
---
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="a3cda-103">Capture audio/vidéo en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3cda-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="a3cda-104">Microsoft Media Foundation prend en charge la capture audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="a3cda-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="a3cda-105">Les périphériques de capture vidéo sont pris en charge par le pilote de classe UVC et doivent être compatibles avec UVC 1,1.</span><span class="sxs-lookup"><span data-stu-id="a3cda-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="a3cda-106">Les périphériques de capture audio sont pris en charge via l’API de session audio Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="a3cda-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="a3cda-107">Un périphérique de capture est représenté dans Media Foundation par un objet de source multimédia, qui expose l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="a3cda-108">Dans la plupart des cas, l’application n’utilise pas directement cette interface, mais utilise une API de niveau supérieur, telle que le [lecteur source](source-reader.md) , pour contrôler l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="a3cda-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="a3cda-109">Énumérer les périphériques de capture</span><span class="sxs-lookup"><span data-stu-id="a3cda-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="a3cda-110">Pour énumérer les périphériques de capture sur le système, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a3cda-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="a3cda-111">Appelez la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a3cda-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="a3cda-112">Affectez l’une des valeurs suivantes à l’attribut de type de source de l' [ \_ \_ attribut \_ \_ DEVSOURCE MF](mf-devsource-attribute-source-type.md) :</span><span class="sxs-lookup"><span data-stu-id="a3cda-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="a3cda-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3cda-113">Value</span></span>                                                    | <span data-ttu-id="a3cda-114">Description</span><span class="sxs-lookup"><span data-stu-id="a3cda-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="a3cda-115">**TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ AUDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="a3cda-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="a3cda-116">Énumérer les périphériques de capture audio.</span><span class="sxs-lookup"><span data-stu-id="a3cda-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="a3cda-117">**TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="a3cda-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="a3cda-118">Énumérer les périphériques de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="a3cda-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="a3cda-119">Appelez la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="a3cda-120">Cette fonction alloue un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="a3cda-121">Chaque pointeur représente un objet d’activation pour un appareil sur le système.</span><span class="sxs-lookup"><span data-stu-id="a3cda-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="a3cda-122">Appelez la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer une instance de la source du média à partir de l’un des objets d’activation.</span><span class="sxs-lookup"><span data-stu-id="a3cda-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="a3cda-123">L’exemple suivant crée une source de média pour le premier appareil de capture vidéo dans la liste d’énumération :</span><span class="sxs-lookup"><span data-stu-id="a3cda-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



<span data-ttu-id="a3cda-124">Vous pouvez interroger les objets d’activation pour différents attributs, y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a3cda-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="a3cda-125">L’attribut de [ \_ \_ \_ \_ nom convivial de l’attribut DEVSOURCE MF](mf-devsource-attribute-friendly-name.md) contient le nom complet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a3cda-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="a3cda-126">Le nom d’affichage peut être affiché à l’utilisateur, mais il peut ne pas être unique.</span><span class="sxs-lookup"><span data-stu-id="a3cda-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="a3cda-127">Pour les périphériques vidéo, l’attribut de [ \_ \_ \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contient le lien symbolique vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a3cda-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="a3cda-128">Le lien symbolique identifie de façon unique l’appareil sur le système, mais n’est pas une chaîne lisible.</span><span class="sxs-lookup"><span data-stu-id="a3cda-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="a3cda-129">Pour les périphériques audio, l’attribut d' [ \_ ID de point de \_ \_ \_ \_ \_ terminaison \_ AUDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contient l’ID de point de terminaison audio de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a3cda-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="a3cda-130">L’ID de point de terminaison audio est semblable à un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="a3cda-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="a3cda-131">Il identifie de façon unique l’appareil sur le système, mais n’est pas une chaîne lisible.</span><span class="sxs-lookup"><span data-stu-id="a3cda-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="a3cda-132">L’exemple suivant prend un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) et imprime le nom complet de chaque appareil dans la fenêtre de débogage :</span><span class="sxs-lookup"><span data-stu-id="a3cda-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



<span data-ttu-id="a3cda-133">Si vous connaissez déjà le lien symbolique pour un périphérique vidéo, il existe une autre façon de créer la source du média pour l’appareil :</span><span class="sxs-lookup"><span data-stu-id="a3cda-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="a3cda-134">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a3cda-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="a3cda-135">Définissez l’attribut de [ \_ \_ \_ \_ type de source](mf-devsource-attribute-source-type.md) de l’attribut MF DEVSOURCE sur le type de source d' **\_ attribut MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="a3cda-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="a3cda-136">Définissez l’attribut de [ \_ \_ \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) sur le lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="a3cda-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="a3cda-137">Appelez la fonction [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="a3cda-138">La première retourne un pointeur [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="a3cda-139">Ce dernier retourne un pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) vers un objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="a3cda-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="a3cda-140">Vous pouvez utiliser l’objet d’activation pour créer la source.</span><span class="sxs-lookup"><span data-stu-id="a3cda-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="a3cda-141">(Un objet d’activation peut être marshalé vers un autre processus, c’est pourquoi il est utile si vous souhaitez créer la source dans un autre processus.</span><span class="sxs-lookup"><span data-stu-id="a3cda-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="a3cda-142">Pour plus d’informations, consultez [objets d’activation](activation-objects.md).)</span><span class="sxs-lookup"><span data-stu-id="a3cda-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="a3cda-143">L’exemple suivant prend le lien symbolique d’un périphérique vidéo et crée une source de média.</span><span class="sxs-lookup"><span data-stu-id="a3cda-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



<span data-ttu-id="a3cda-144">Il existe une méthode équivalente pour créer un périphérique audio à partir de l’ID de point de terminaison audio :</span><span class="sxs-lookup"><span data-stu-id="a3cda-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="a3cda-145">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a3cda-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="a3cda-146">Définissez l’attribut de [ \_ \_ \_ \_ type de source](mf-devsource-attribute-source-type.md) de l’attribut MF DEVSOURCE sur le type de source d' **\_ attribut MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="a3cda-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="a3cda-147">Définissez l’attribut de l’ID de point de terminaison de l’attribut DEVSOURCE de l' [ \_ attribut MF \_ \_ \_ \_ AUDCAP \_ \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) sur l’ID du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a3cda-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="a3cda-148">Appelez la fonction [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="a3cda-149">L’exemple suivant prend un ID de point de terminaison audio et crée une source de média.</span><span class="sxs-lookup"><span data-stu-id="a3cda-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a><span data-ttu-id="a3cda-150">Utiliser un appareil de capture</span><span class="sxs-lookup"><span data-stu-id="a3cda-150">Use a capture device</span></span>

<span data-ttu-id="a3cda-151">Une fois que vous avez créé la source du média pour un appareil de capture, utilisez le [lecteur source](source-reader.md) pour obtenir les données de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a3cda-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="a3cda-152">Le lecteur source fournit des exemples de supports qui contiennent les données audio de capture ou les trames vidéo.</span><span class="sxs-lookup"><span data-stu-id="a3cda-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="a3cda-153">L’étape suivante dépend de votre scénario d’application :</span><span class="sxs-lookup"><span data-stu-id="a3cda-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="a3cda-154">Aperçu vidéo : utilisez Microsoft Direct3D ou Direct2D pour afficher la vidéo.</span><span class="sxs-lookup"><span data-stu-id="a3cda-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="a3cda-155">Capture de fichiers : utilisez le [writer du récepteur](sink-writer.md) pour encoder le fichier.</span><span class="sxs-lookup"><span data-stu-id="a3cda-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="a3cda-156">Aperçu audio : utilisez [WASAPI](/windows/desktop/CoreAudio/wasapi).</span><span class="sxs-lookup"><span data-stu-id="a3cda-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="a3cda-157">Si vous souhaitez combiner la capture audio avec la capture vidéo, utilisez la *source du média d’agrégation*.</span><span class="sxs-lookup"><span data-stu-id="a3cda-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="a3cda-158">La source du média d’agrégation contient une collection de sources de média et combine tous leurs flux dans un objet source de média unique.</span><span class="sxs-lookup"><span data-stu-id="a3cda-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="a3cda-159">Pour créer une instance de la source du média d’agrégation, appelez la fonction [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .</span><span class="sxs-lookup"><span data-stu-id="a3cda-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="a3cda-160">Arrêter l’appareil de capture</span><span class="sxs-lookup"><span data-stu-id="a3cda-160">Shut down the capture device</span></span>

<span data-ttu-id="a3cda-161">Lorsque l’appareil de capture n’est plus nécessaire, vous devez arrêter l’appareil en appelant [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur l’objet [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que vous avez obtenu en appelant [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="a3cda-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="a3cda-162">L’échec de l’appel de **Shutdown** peut entraîner des liaisons de mémoire, car le système peut conserver une référence aux ressources **IMFMediaSource** jusqu’à l’appel de **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="a3cda-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="a3cda-163">Si vous avez alloué une chaîne contenant le lien symbolique vers un appareil de capture, vous devez également libérer cet objet.</span><span class="sxs-lookup"><span data-stu-id="a3cda-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="a3cda-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3cda-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3cda-165">Capture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="a3cda-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
