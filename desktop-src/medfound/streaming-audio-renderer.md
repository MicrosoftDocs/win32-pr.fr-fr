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
# <a name="streaming-audio-renderer"></a>Convertisseur audio de streaming

Le convertisseur audio de streaming (SAR) est un récepteur multimédia qui restitue l’audio. Chaque instance du SAR affiche un flux audio unique. Pour afficher plusieurs flux, utilisez plusieurs instances du SAR.

Pour créer l’SAR, appelez l’une des fonctions suivantes :

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Retourne un pointeur vers l’SAR.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Retourne un pointeur vers un objet d’activation qui peut être utilisé pour créer le SAR.

La deuxième fonction, qui retourne un objet d’activation, est requise si vous jouez du contenu protégé, car l’objet d’activation doit être sérialisé vers le processus protégé. Pour obtenir un contenu clair, vous pouvez utiliser l’une ou l’autre fonction.

Le SAR peut recevoir des données audio non compressées dans un format à virgule flottante PCM ou IEEE. Si la vitesse de lecture est plus rapide ou plus lente que 1 ×, le SAR ajuste automatiquement le pas.

## <a name="configuring-the-audio-renderer"></a>Configuration du convertisseur audio

La SAR prend en charge plusieurs attributs de configuration. Le mécanisme de définition de ces attributs dépend de la fonction que vous appelez pour créer l’SAR. Si vous utilisez la fonction [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , procédez comme suit :

1.  Créez un nouveau magasin d’attributs en appelant [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Ajoutez les attributs au magasin d’attributs.
3.  Transmettez le magasin d’attributs à la fonction [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) dans le paramètre *pAudioAttributes* .

Si vous utilisez la fonction [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , la fonction retourne un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dans le paramètre *ppActivate* . Utilisez ce pointeur pour ajouter les attributs.

Pour obtenir la liste des attributs de configuration, consultez [attributs de convertisseur audio](audio-renderer-attributes.md).

## <a name="selecting-the-audio-endpoint-device"></a>Sélection de l’appareil de point de terminaison audio

Un *périphérique de point de terminaison audio* est un périphérique matériel qui restitue ou capture l’audio. Par exemple, les haut-parleurs, les casques, les microphones et les lecteurs de CD. Le SAR utilise toujours un périphérique de rendu audio. Il existe deux façons de sélectionner l’appareil.

La première approche consiste à énumérer les périphériques de rendu audio sur le système, à l’aide de l’interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Cette interface est documentée dans la documentation de l’API audio principale.

1.  Créez l’objet énumérateur d’appareil.
2.  Utilisez l’énumérateur d’appareil pour énumérer les périphériques de rendu audio. Chaque appareil est représenté par un pointeur vers l’interface [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .
3.  Sélectionnez un appareil, en fonction des propriétés de l’appareil ou de la sélection de l’utilisateur.
4.  Appelez [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour récupérer l’identificateur de l’appareil.
5.  Définissez l’identificateur d’appareil en tant que valeur de l’attribut ID de point de terminaison de l' [**\_ \_ attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .

Au lieu d’énumérer les appareils, vous pouvez spécifier le périphérique audio par son *rôle*. Un rôle audio identifie une catégorie générale d’utilisation. Par exemple, le rôle de *console* est défini pour les jeux et les notifications système, tandis que le rôle *multimédia* est défini pour la musique et les films. Chaque rôle est associé à un périphérique de rendu audio, et l’utilisateur peut modifier ces attributions. Si vous spécifiez un rôle d’appareil, le SAR utilise le périphérique audio affecté à ce rôle. Pour spécifier le rôle d’appareil, définissez l’attribut de [**\_ rôle de point de \_ terminaison d’attribut de convertisseur \_ \_ \_ audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .

Les deux attributs répertoriés dans cette section s’excluent mutuellement. Si vous ne définissez pas l’un d’eux, le SAR utilise le périphérique audio affecté au rôle **eConsole** .

Le code suivant énumère les périphériques de rendu audio et attribue le premier périphérique de la liste à la région SAR. Cet exemple utilise la fonction [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) pour créer l’SAR.


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



Pour créer l’objet d’activation pour le SAR, modifiez le code qui s’affiche après l’appel à [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) en procédant comme suit :


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



## <a name="selecting-the-audio-session"></a>Sélection de la session audio

Une session audio est un groupe de flux audio associés qu’une application peut gérer collectivement. L’application peut contrôler le niveau de volume et l’état de silence de chaque session. Les sessions sont identifiées par un GUID. Pour spécifier la session audio pour le SAR, utilisez l’attribut d’ID de session de l' [ \_ \_ attribut de convertisseur \_ \_ \_ audio MF](mf-audio-renderer-attribute-session-id-attribute.md) . Si vous ne définissez pas cet attribut, le SAR rejoint la session par défaut pour ce processus, identifiée par le **GUID \_ null**.

Par défaut, une session audio est spécifique au processus, ce qui signifie qu’elle contient uniquement des flux du processus appelant. Pour joindre une session inter-processus, définissez l' [attribut \_ \_ \_ \_ indicateurs d’attribut de convertisseur audio MF](mf-audio-renderer-attribute-flags-attribute.md) avec les **indicateurs d’attribut de \_ rendu audio MF \_ \_ \_ \_ CROSSPROCESS**.

Après avoir créé l’SAR, vous utilisez l’interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pour joindre la session à un groupe de sessions, toutes contrôlées par le même contrôle de volume dans le panneau de configuration. Vous pouvez également utiliser cette interface pour définir le nom d’affichage et l’icône qui s’affichent dans le contrôle du volume.

## <a name="controlling-volume-levels"></a>Contrôle des niveaux de volume

Pour contrôler le niveau de volume maître de tous les flux dans la session audio de l’SAR, utilisez l’interface [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) . Pour contrôler le volume d’un flux individuel, ou pour contrôler le volume de canaux individuels dans un flux, utilisez l’interface [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) . Les deux interfaces sont obtenues en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Vous pouvez appeler **GetService** directement sur le SAR ou l’appeler sur la session multimédia. Les niveaux de volume sont exprimés en tant que valeurs d’atténuation. Pour chaque canal, le niveau d’atténuation est le produit du volume maître et du volume de canal.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> </dl>

 

 
