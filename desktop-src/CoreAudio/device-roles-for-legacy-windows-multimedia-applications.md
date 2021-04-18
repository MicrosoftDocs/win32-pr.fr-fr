---
description: Rôles d’appareil pour les applications multimédias Windows héritées
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Rôles d’appareil pour les applications multimédias Windows héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522888"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="80d9e-103">Rôles d’appareil pour les applications multimédias Windows héritées</span><span class="sxs-lookup"><span data-stu-id="80d9e-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="80d9e-104">L’API MMDevice prend en charge les rôles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="80d9e-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="80d9e-105">Toutefois, l’interface utilisateur de Windows Vista n’implémente pas la prise en charge de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="80d9e-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="80d9e-106">La prise en charge de l’interface utilisateur pour les rôles d’appareil peut être implémentée dans une future version de Windows.</span><span class="sxs-lookup"><span data-stu-id="80d9e-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="80d9e-107">Pour plus d’informations, consultez [rôles de périphérique dans Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="80d9e-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="80d9e-108">Les fonctions **waveOutXxx** et **waveInXxx** Windows Multimedia héritées ne permettent pas à une application de sélectionner l’appareil de [point de terminaison audio](audio-endpoint-devices.md) que l’utilisateur a affecté à un [rôle d’appareil](device-roles.md)particulier.</span><span class="sxs-lookup"><span data-stu-id="80d9e-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="80d9e-109">Toutefois, dans Windows Vista, les API audio de base peuvent être utilisées conjointement avec une application multimédia Windows pour activer la sélection des appareils en fonction du rôle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80d9e-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="80d9e-110">Par exemple, à l’aide de l' [API MMDevice](mmdevice-api.md), une application **waveOutXxx** peut identifier l’appareil de point de terminaison audio qui est affecté à un rôle, identifier l’appareil de sortie de forme d’onde correspondant et appeler la fonction **waveOutOpen** pour ouvrir une instance de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80d9e-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="80d9e-111">Pour plus d’informations sur **waveOutXxx** et **waveInXxx**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="80d9e-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="80d9e-112">L’exemple de code suivant montre comment obtenir l’ID de périphérique de la forme d’onde pour le périphérique de point de terminaison de rendu affecté à un rôle d’appareil particulier :</span><span class="sxs-lookup"><span data-stu-id="80d9e-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



<span data-ttu-id="80d9e-113">Dans l’exemple de code précédent, la fonction GetWaveOutId accepte un rôle d’appareil (eConsole, eMultimedia ou eCommunications) comme paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="80d9e-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="80d9e-114">Le deuxième paramètre est un pointeur par l’intermédiaire duquel la fonction écrit l’ID de périphérique de la forme d’onde pour le périphérique de sortie de forme d’onde affecté au rôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="80d9e-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="80d9e-115">L’application peut ensuite appeler **waveOutOpen** avec cet ID pour ouvrir l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80d9e-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="80d9e-116">La boucle principale de l’exemple de code précédent contient deux appels à la fonction **waveOutMessage** .</span><span class="sxs-lookup"><span data-stu-id="80d9e-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="80d9e-117">Le premier appel envoie un \_ message DRV QUERYFUNCTIONINSTANCEIDSIZE pour récupérer la taille, en octets, de la [chaîne d’ID de point de terminaison](endpoint-id-strings.md) de l’appareil de forme d’onde identifiée par le paramètre *waveOutId* .</span><span class="sxs-lookup"><span data-stu-id="80d9e-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="80d9e-118">(La chaîne ID du point de terminaison identifie le périphérique de point de terminaison audio sous-jacent de l’abstraction de l’appareil de forme d’onde.) La taille signalée par cet appel comprend l’espace pour le caractère null de fin à la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="80d9e-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="80d9e-119">Le programme peut utiliser les informations de taille pour allouer une mémoire tampon suffisamment grande pour contenir l’intégralité de la chaîne d’ID de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="80d9e-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="80d9e-120">Le deuxième appel à **waveOutMessage** envoie un \_ message QUERYFUNCTIONINSTANCEID DRV pour récupérer la chaîne d’ID d’appareil de l’appareil de sortie Waveform.</span><span class="sxs-lookup"><span data-stu-id="80d9e-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="80d9e-121">L’exemple de code compare cette chaîne à la chaîne d’ID de périphérique de l’appareil de point de terminaison audio avec le rôle d’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="80d9e-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="80d9e-122">Si les chaînes correspondent, la fonction écrit l’ID de périphérique de la forme d’onde à l’emplacement désigné par le paramètre *pWaveOutId*.</span><span class="sxs-lookup"><span data-stu-id="80d9e-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="80d9e-123">L’appelant peut utiliser cet ID pour ouvrir l’appareil de sortie de forme d’onde qui a le rôle d’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="80d9e-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="80d9e-124">Windows Vista prend en charge les \_ messages DRV QUERYFUNCTIONINSTANCEIDSIZE et DRV \_ QUERYFUNCTIONINSTANCEID.</span><span class="sxs-lookup"><span data-stu-id="80d9e-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="80d9e-125">Ils ne sont pas pris en charge dans les versions antérieures de Windows, notamment Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="80d9e-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="80d9e-126">La fonction de l’exemple de code précédent obtient l’ID de périphérique de la forme d’onde pour un périphérique de rendu, mais, avec quelques modifications, il peut être adapté pour obtenir l’ID de périphérique de la forme d’onde pour un périphérique de capture.</span><span class="sxs-lookup"><span data-stu-id="80d9e-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="80d9e-127">L’application peut ensuite appeler **waveInOpen** avec cet ID pour ouvrir l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80d9e-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="80d9e-128">Pour modifier l’exemple de code précédent afin d’obtenir l’ID de périphérique de la forme d’onde pour le périphérique de point de terminaison de capture audio qui est affecté à un rôle particulier, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="80d9e-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="80d9e-129">Remplacez tous les appels de fonction **waveOutXxx** de l’exemple précédent par les appels de fonction **waveInXxx** correspondants.</span><span class="sxs-lookup"><span data-stu-id="80d9e-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="80d9e-130">Remplacez le type de handle HWAVEOUT par HWAVEIN.</span><span class="sxs-lookup"><span data-stu-id="80d9e-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="80d9e-131">Remplacez la constante d’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ERender par eCapture.</span><span class="sxs-lookup"><span data-stu-id="80d9e-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="80d9e-132">Dans Windows Vista, les fonctions **waveOutOpen** et **waveInOpen** attribuent toujours les flux audio qu’ils créent à la session par défaut : la session spécifique au processus qui est identifiée par la valeur GUID de la session GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="80d9e-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80d9e-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80d9e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d9e-134">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="80d9e-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



