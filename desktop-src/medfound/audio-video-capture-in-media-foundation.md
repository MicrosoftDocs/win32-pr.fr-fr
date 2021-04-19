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
# <a name="audiovideo-capture-in-media-foundation"></a>Capture audio/vidéo en Media Foundation

Microsoft Media Foundation prend en charge la capture audio et vidéo. Les périphériques de capture vidéo sont pris en charge par le pilote de classe UVC et doivent être compatibles avec UVC 1,1. Les périphériques de capture audio sont pris en charge via l’API de session audio Windows (WASAPI).

Un périphérique de capture est représenté dans Media Foundation par un objet de source multimédia, qui expose l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . Dans la plupart des cas, l’application n’utilise pas directement cette interface, mais utilise une API de niveau supérieur, telle que le [lecteur source](source-reader.md) , pour contrôler l’appareil de capture.

## <a name="enumerate-capture-devices"></a>Énumérer les périphériques de capture

Pour énumérer les périphériques de capture sur le système, procédez comme suit :

1.  Appelez la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.
2.  Affectez l’une des valeurs suivantes à l’attribut de type de source de l' [ \_ \_ attribut \_ \_ DEVSOURCE MF](mf-devsource-attribute-source-type.md) :

    | Valeur                                                    | Description                      |
    |----------------------------------------------------------|----------------------------------|
    | **TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ AUDCAP \_ GUID** | Énumérer les périphériques de capture audio. |
    | **TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ GUID** | Énumérer les périphériques de capture vidéo. |

    

     

3.  Appelez la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Cette fonction alloue un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Chaque pointeur représente un objet d’activation pour un appareil sur le système.
4.  Appelez la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer une instance de la source du média à partir de l’un des objets d’activation.

L’exemple suivant crée une source de média pour le premier appareil de capture vidéo dans la liste d’énumération :


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



Vous pouvez interroger les objets d’activation pour différents attributs, y compris les éléments suivants :

-   L’attribut de [ \_ \_ \_ \_ nom convivial de l’attribut DEVSOURCE MF](mf-devsource-attribute-friendly-name.md) contient le nom complet de l’appareil. Le nom d’affichage peut être affiché à l’utilisateur, mais il peut ne pas être unique.
-   Pour les périphériques vidéo, l’attribut de [ \_ \_ \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contient le lien symbolique vers l’appareil. Le lien symbolique identifie de façon unique l’appareil sur le système, mais n’est pas une chaîne lisible.
-   Pour les périphériques audio, l’attribut d' [ \_ ID de point de \_ \_ \_ \_ \_ terminaison \_ AUDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contient l’ID de point de terminaison audio de l’appareil. L’ID de point de terminaison audio est semblable à un lien symbolique. Il identifie de façon unique l’appareil sur le système, mais n’est pas une chaîne lisible.

L’exemple suivant prend un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) et imprime le nom complet de chaque appareil dans la fenêtre de débogage :


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



Si vous connaissez déjà le lien symbolique pour un périphérique vidéo, il existe une autre façon de créer la source du média pour l’appareil :

1.  Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.
2.  Définissez l’attribut de [ \_ \_ \_ \_ type de source](mf-devsource-attribute-source-type.md) de l’attribut MF DEVSOURCE sur le type de source d' **\_ attribut MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ GUID**.
3.  Définissez l’attribut de [ \_ \_ \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) sur le lien symbolique.
4.  Appelez la fonction [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . La première retourne un pointeur [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . Ce dernier retourne un pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) vers un objet d’activation. Vous pouvez utiliser l’objet d’activation pour créer la source. (Un objet d’activation peut être marshalé vers un autre processus, c’est pourquoi il est utile si vous souhaitez créer la source dans un autre processus. Pour plus d’informations, consultez [objets d’activation](activation-objects.md).)

L’exemple suivant prend le lien symbolique d’un périphérique vidéo et crée une source de média.


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



Il existe une méthode équivalente pour créer un périphérique audio à partir de l’ID de point de terminaison audio :

1.  Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs.
2.  Définissez l’attribut de [ \_ \_ \_ \_ type de source](mf-devsource-attribute-source-type.md) de l’attribut MF DEVSOURCE sur le type de source d' **\_ attribut MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**.
3.  Définissez l’attribut de l’ID de point de terminaison de l’attribut DEVSOURCE de l' [ \_ attribut MF \_ \_ \_ \_ AUDCAP \_ \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) sur l’ID du point de terminaison.
4.  Appelez la fonction [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

L’exemple suivant prend un ID de point de terminaison audio et crée une source de média.


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



## <a name="use-a-capture-device"></a>Utiliser un appareil de capture

Une fois que vous avez créé la source du média pour un appareil de capture, utilisez le [lecteur source](source-reader.md) pour obtenir les données de l’appareil. Le lecteur source fournit des exemples de supports qui contiennent les données audio de capture ou les trames vidéo. L’étape suivante dépend de votre scénario d’application :

-   Aperçu vidéo : utilisez Microsoft Direct3D ou Direct2D pour afficher la vidéo.
-   Capture de fichiers : utilisez le [writer du récepteur](sink-writer.md) pour encoder le fichier.
-   Aperçu audio : utilisez [WASAPI](/windows/desktop/CoreAudio/wasapi).

Si vous souhaitez combiner la capture audio avec la capture vidéo, utilisez la *source du média d’agrégation*. La source du média d’agrégation contient une collection de sources de média et combine tous leurs flux dans un objet source de média unique. Pour créer une instance de la source du média d’agrégation, appelez la fonction [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .

## <a name="shut-down-the-capture-device"></a>Arrêter l’appareil de capture

Lorsque l’appareil de capture n’est plus nécessaire, vous devez arrêter l’appareil en appelant [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur l’objet [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que vous avez obtenu en appelant [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). L’échec de l’appel de **Shutdown** peut entraîner des liaisons de mémoire, car le système peut conserver une référence aux ressources **IMFMediaSource** jusqu’à l’appel de **Shutdown** .


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Si vous avez alloué une chaîne contenant le lien symbolique vers un appareil de capture, vous devez également libérer cet objet.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture audio/vidéo](audio-video-capture.md)
</dt> </dl>

 

 
