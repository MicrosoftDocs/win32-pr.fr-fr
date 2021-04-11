---
description: Ce didacticiel montre comment utiliser l’API de transcodage pour encoder un fichier MP4 à l’aide de H. 264 pour le flux vidéo et AAC pour le flux audio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Didacticiel : encodage d’un fichier MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202247"
---
# <a name="tutorial-encoding-an-mp4-file"></a>Didacticiel : encodage d’un fichier MP4

Ce didacticiel montre comment utiliser l' [API de transcodage](transcode-api.md) pour encoder un fichier MP4 à l’aide de H. 264 pour le flux vidéo et AAC pour le flux audio.

-   [En-têtes et fichiers de bibliothèque](#headers-and-library-files)
-   [Définir les profils d’encodage](#define-the-encoding-profiles)
-   [Écrire la fonction wmain](#write-the-wmain-function)
-   [Encoder le fichier](#encode-the-file)
    -   [Créer la source du média](#create-the-media-source)
    -   [Obtient la durée de la source](#get-the-source-duration)
    -   [Créer le profil de transcodage](#create-the-transcode-profile)
    -   [Exécuter la session d’encodage](#run-the-encoding-session)
-   [Assistance de session multimédia](#media-session-helper)
-   [Rubriques connexes](#related-topics)

## <a name="headers-and-library-files"></a>En-têtes et fichiers de bibliothèque

Incluez les fichiers d’en-tête suivants.


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



Liez les fichiers de bibliothèque suivants.


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>Définir les profils d’encodage

L’une des approches de l’encodage consiste à définir une liste de profils d’encodage cibles connus à l’avance. Pour ce didacticiel, nous prenons une approche relativement simple et stockons une liste de formats d’encodage pour la vidéo H. 264 et l’audio AAC.

Pour H. 264, les attributs de format les plus importants sont le profil H. 264, la fréquence d’images, la taille de trame et la vitesse de transmission encodée. Le tableau suivant contient une liste de formats d’encodage H. 264.


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



Les profils H. 264 sont spécifiés à l’aide de l’énumération [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) . Vous pouvez également spécifier le niveau H. 264, mais le Microsoft Media Foundation de l' [**encodeur vidéo h. 264**](h-264-video-encoder.md) peut dériver le niveau approprié pour un flux vidéo donné. il est donc recommandé de ne pas remplacer le niveau sélectionné de l’encodeur. Pour le contenu entrelacé, vous devez également spécifier le mode entrelacé (voir entrelacement de [vidéos](video-interlacing.md)).

Pour l’audio AAC, les attributs de format les plus importants sont le taux d’échantillonnage audio, le nombre de canaux, le nombre de bits par échantillon et la vitesse de transmission encodée. Si vous le souhaitez, vous pouvez définir l’indication du niveau de profil audio AAC. Pour plus d’informations, consultez l' [**encodeur AAC**](aac-encoder.md). Le tableau suivant contient une liste de formats d’encodage AAC.


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> Les `H264ProfileInfo` `AACProfileInfo` structures et définies ici ne font pas partie de l’API Media Foundation.

 

## <a name="write-the-wmain-function"></a>Écrire la fonction wmain

Le code suivant montre le point d’entrée pour l’application console.


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



La `wmain` fonction effectue les opérations suivantes :

1.  Appelle la fonction [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.
2.  Appelle la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser Media Foundation.
3.  Appelle la fonction définie par l’application `EncodeFile` . Cette fonction transcode le fichier d’entrée dans le fichier de sortie et s’affiche dans la section suivante.
4.  Appelle la fonction [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter Media Foundation.
5.  Appelez la fonction [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) pour désinitialiser la bibliothèque com.

## <a name="encode-the-file"></a>Encoder le fichier

Le code suivant illustre la `EncodeFile` fonction, qui effectue le transcodage. Cette fonction se compose principalement d’appels à d’autres fonctions définies par l’application, qui sont présentées plus loin dans cette rubrique.


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



La `EncodeFile` fonction effectue les étapes suivantes.

1.  Crée une source de média pour le fichier d’entrée, à l’aide de l’URL ou du chemin d’accès du fichier d’entrée. (Consultez [créer la source du média](#create-the-media-source).)
2.  Obtient la durée du fichier d’entrée. (Consultez [obtenir la durée de la source](#get-the-source-duration).)
3.  Créez le profil de transcodage. (Consultez [créer le profil de transcodage](#create-the-transcode-profile).)
4.  Appelez [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) pour créer la topologie de transcodage partielle.
5.  Créez un objet d’assistance qui gère la session multimédia. (Voir Media session Helper).
6.  Exécutez la session d’encodage et attendez qu’elle se termine. (Consultez [exécuter la session d’encodage](#run-the-encoding-session).)
7.  Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) pour arrêter la source du média.
8.  Mise en sortie des pointeurs d’interface. Ce code utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface. Une autre option consiste à utiliser une classe de pointeur intelligent COM, telle que **CComPtr**.

### <a name="create-the-media-source"></a>Créer la source du média

La source du média est l’objet qui lit et analyse le fichier d’entrée. Pour créer la source du média, transmettez l’URL du fichier d’entrée au programme de [résolution source](source-resolver.md). Le code suivant montre comment procéder.


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Pour plus d’informations, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).

### <a name="get-the-source-duration"></a>Obtient la durée de la source

Bien que cela ne soit pas obligatoire, il est utile d’interroger la source du média pendant la durée du fichier d’entrée. Cette valeur peut être utilisée pour suivre la progression de l’encodage. La durée est stockée dans l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) du descripteur de présentation. Récupérez le descripteur de présentation en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a>Créer le profil de transcodage

Le profil de transcodage décrit les paramètres d’encodage. Pour plus d’informations sur la création d’un profil de transcodage, consultez [utilisation de l’API de transcodage](fast-transcode-objects.md). Pour créer le profil, procédez comme suit.

1.  Appelez [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) pour créer le profil vide.
2.  Créez un type de média pour le flux audio AAC. Ajoutez-le au profil en appelant [**IMFTranscodeProfile :: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).
3.  Créez un type de média pour le flux vidéo H. 264. Ajoutez-le au profil en appelant [**IMFTranscodeProfile :: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).
4.  Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs pour les attributs de niveau conteneur.
5.  Définissez l' [attribut \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) . Il s’agit du seul attribut requis au niveau du conteneur. Pour la sortie de fichier MP4, définissez cet attribut sur **MFTranscodeContainerType \_ MPEG4**.
6.  Appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) pour définir les attributs au niveau du conteneur.

Le code suivant illustre ces étapes.


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



Pour spécifier les attributs du flux vidéo H. 264, créez un magasin d’attributs et définissez les attributs suivants :



| Attribut                                                       | Description                      |
|-----------------------------------------------------------------|---------------------------------|
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)              | Définissez sur **MFVideoFormat \_ H264 –**. |
| [**\_Profil de \_ MPEG2 \_ MT pour MF**](mf-mt-mpeg2-profile-attribute.md) | Profil H. 264.                  |
| [**\_taille de \_ trame MF MF \_**](mf-mt-frame-size-attribute.md)       | Taille du frame.                     |
| [**\_fréquence d' \_ images MF MF \_**](mf-mt-frame-rate-attribute.md)       | Fréquence d’images.                     |
| [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)     | Vitesse de transmission encodée.               |



 

Pour spécifier les attributs du flux audio AAC, créez un magasin d’attributs et définissez les attributs suivants :



| Attribut                                                                                      | Description                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                             | Définir sur **MFAudioFormat \_ AAC**            |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)        | Taux d’échantillonnage audio.                       |
| [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)              | Bits par échantillon audio.                   |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                     | Nombre de canaux audio.                |
| [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Vitesse de transmission encodée.                        |
| [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)               | défini sur 1.                                |
| [\_indication du \_ \_ niveau de \_ profil \_ audio MF MT AAC \_](mf-mt-aac-audio-profile-level-indication.md) | Indication du niveau de profil AAC (facultatif). |



 

Le code suivant crée les attributs du flux vidéo.


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Le code suivant crée les attributs de flux audio.


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Notez que l’API de transcodage ne requiert pas de véritable type de média, bien qu’elle utilise des attributs de type de média. En particulier, l’attribut de [**\_ \_ \_ type principal MF MT**](mf-mt-major-type-attribute.md) n’est pas obligatoire, car les méthodes [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) et [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) impliquent le type majeur. Toutefois, il est également valide de passer un type de média réel à ces méthodes. (L’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) hérite de [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)

### <a name="run-the-encoding-session"></a>Exécuter la session d’encodage

Le code suivant exécute la session d’encodage. Elle utilise la classe d’assistance de session multimédia, qui est présentée dans la section suivante.


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a>Assistance de session multimédia

La [session multimédia](media-session.md) est décrite plus en détail dans la section [Media Foundation architecture](media-foundation-architecture.md) de cette documentation. La session multimédia utilise un modèle d’événement asynchrone. Dans une application GUI, vous devez répondre aux événements de session sans bloquer le thread d’interface utilisateur pour attendre l’événement suivant. Le didacticiel [Comment lire des fichiers multimédias non protégés](how-to-play-unprotected-media-files.md) montre comment effectuer cette opération dans une application de lecture. Pour l’encodage, le principe est le même, mais moins d’événements sont pertinents :



| Événement                                  | Description                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MESessionEnded](mesessionended.md)   | Déclenché lorsque l’encodage est terminé.                                                                                                                            |
| [MESessionClosed](mesessionclosed.md) | Déclenché lorsque la méthode [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se termine. Une fois cet événement déclenché, il est possible d’arrêter la session multimédia en toute sécurité. |



 

Pour une application console, il est raisonnable de bloquer et d’attendre les événements. En fonction du fichier source et des paramètres d’encodage, l’encodage peut prendre un certain temps. Vous pouvez accéder aux mises à jour de progression comme suit :

1.  Appelez [**IMFMediaSession :: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) pour afficher l’horloge de la présentation.
2.  Interrogez l’horloge de l’interface [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .
3.  Appelez [**IMFPresentationClock :: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) pour accéder à la position actuelle.
4.  La position est donnée en unités de temps. Pour faire en sorte que le pourcentage soit terminé, utilisez la valeur `(100 * position) / duration` .

Voici la déclaration de la `CSession` classe.


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



Le code suivant illustre l’implémentation complète de la `CSession` classe.


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Encodeur AAC**](aac-encoder.md)
</dt> <dt>

[**Encodeur vidéo H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[API de transcodage](transcode-api.md)
</dt> </dl>

 

 
