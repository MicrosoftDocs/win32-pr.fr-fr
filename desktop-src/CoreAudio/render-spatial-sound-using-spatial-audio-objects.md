---
description: Cet article présente des exemples simples qui illustrent comment implémenter un son spatial à l’aide d’objets audio spatiaux statiques, d’objets audio spatiaux dynamiques et d’objets audio spatiaux qui utilisent la fonction de transfert relatif de l’en-tête de Microsoft (HRTF).
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Restituer le son spatial à l’aide d’objets audio spatiaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748548"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Restituer le son spatial à l’aide d’objets audio spatiaux

Cet article présente des exemples simples qui illustrent comment implémenter un son spatial à l’aide d’objets audio spatiaux statiques, d’objets audio spatiaux dynamiques et d’objets audio spatiaux qui utilisent la fonction de transfert relatif de l’en-tête de Microsoft (HRTF). Les étapes d’implémentation pour ces trois techniques sont très similaires et cet article fournit un exemple de code structuré de la même façon pour chaque technique. Pour obtenir des exemples complets d’implémentations de son spatial réel, consultez le [dépôt github des exemples de son spatial Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio). Pour une vue d’ensemble de Windows Sonic, la solution de niveau plate-forme de Microsoft pour la prise en charge des sons spatiaux sur Xbox et Windows, consultez [son spatial](spatial-sound.md).

## <a name="render-audio-using-static-spatial-audio-objects"></a>Rendu audio à l’aide d’objets audio spatiaux statiques

Un objet audio statique est utilisé pour restituer le son à l’un des 18 canaux audio statiques définis dans l’énumération [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) . Chacun de ces canaux représente un orateur réel ou virtualisé à un point fixe dans l’espace qui ne se déplace pas au fil du temps. Les canaux statiques qui sont disponibles sur un appareil particulier dépendent du format de son spatial utilisé. Pour obtenir la liste des formats pris en charge et de leurs nombres de canaux, consultez [son spatial](spatial-sound.md).

Lorsque vous initialisez un flux audio spatial, vous devez spécifier les canaux statiques disponibles que le flux utilisera. Les exemples de définitions de constantes suivants peuvent être utilisés pour spécifier des configurations d’orateur courantes et obtenir le nombre de canaux disponibles pour chacun d’eux.


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



La première étape du rendu de l’audio spatial consiste à obtenir le point de terminaison audio vers lequel les données audio seront envoyées. Créez une instance de [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) et appelez [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour obtenir le périphérique de rendu audio par défaut.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Lorsque vous créez un flux audio spatial, vous devez spécifier le format audio utilisé par le flux en fournissant une structure [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) . Si vous jouez des données audio à partir d’un fichier, le format est généralement déterminé par le format de fichier audio. Cet exemple utilise un format mono, 32 bits, 48Hz.


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



L’étape suivante du rendu de l’audio spatial consiste à initialiser un flux audio spatial. Tout d’abord, récupérez une instance de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Appelez [**ISpatialAudioClient :: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) pour vous assurer que le format audio que vous utilisez est pris en charge. Créez un événement que le pipeline audio utilisera pour indiquer à l’application qu’elle est prête pour davantage de données audio.

Remplir une structure [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) qui sera utilisée pour initialiser le flux audio spatial. Dans cet exemple, le champ **StaticObjectTypeMask** est défini sur la **constante \_ stéréo ChannelMask** définie précédemment dans cet article, ce qui signifie que seuls les canaux avant droit et gauche peuvent être utilisés par le flux audio. Étant donné que cet exemple utilise uniquement des objets audio statiques et aucun objet dynamique, le champ **MaxDynamicObjectCount** a la valeur 0. Le champ **Category** est défini sur un membre de l’énumération de [**\_ \_ catégorie de flux audio**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , qui définit la façon dont le système mélange le son de ce flux avec d’autres sources audio.

Appelez [**ISpatialAudioClient :: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) pour activer le flux.


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> Lorsque vous utilisez les interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) sur un titre de kit de développement Xbox One (XDK), vous devez d’abord appeler **EnableSpatialAudio** avant d’appeler [**IMMDeviceEnumerator :: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) ou [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Dans le cas contraire, une \_ erreur E nointerface est retournée à partir de l’appel à Activate. **EnableSpatialAudio** est uniquement disponible pour les titres XDK, et n’a pas besoin d’être appelé pour les applications plateforme Windows universelle s’exécutant sur Xbox One, ni pour les appareils non-Xbox One.

 

Déclarez un pointeur pour un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) qui sera utilisé pour écrire des données audio dans un canal statique. Les applications classiques utilisent un objet pour chaque canal spécifié dans le champ **StaticObjectTypeMask** . Par souci de simplicité, cet exemple utilise uniquement un seul objet audio statique.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Avant d’entrer dans la boucle de rendu audio, appelez [**ISpatialAudioObjectRenderStream :: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) pour indiquer au pipeline de média de commencer à demander des données audio. Cet exemple utilise un compteur pour arrêter le rendu de l’audio après 5 secondes.

À l’intérieur de la boucle de rendu, attendez l’événement de fin de la mémoire tampon, fourni lorsque le flux de données audio spatiales a été initialisé, à signaler. Vous devez définir une limite de délai d’expiration raisonnable, telle que 100 ms, lors de l’attente de l’événement, car toute modification apportée au type de rendu ou au point de terminaison entraînera la non-signalisation de cet événement. Dans ce cas, vous pouvez appeler [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) pour tenter de réinitialiser le flux audio spatial.

Ensuite, appelez [**ISpatialAudioObjectRenderStream :: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) pour informer le système que vous êtes sur le le courant de remplir les mémoires tampons des objets audio avec des données. Cette méthode retourne le nombre d’objets audio dynamiques disponibles, non utilisés dans cet exemple, et le nombre de frames de la mémoire tampon pour les objets audio restitués par ce flux.

Si un objet audio spatial statique n’a pas encore été créé, créez-en un ou plusieurs en appelant [**ISpatialAudioObjectRenderStream :: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), en passant une valeur de l’énumération [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) indiquant le canal statique vers lequel le son de l’objet est restitué.

Ensuite, appelez [**ISpatialAudioObject :: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) pour obtenir un pointeur vers la mémoire tampon audio de l’objet audio spatial. Cette méthode retourne également la taille de la mémoire tampon, en octets. Cet exemple utilise une méthode d’assistance, **WriteToAudioObjectBuffer**, pour remplir la mémoire tampon avec des données audio. Cette méthode est présentée plus loin dans cet article. Après avoir écrit dans la mémoire tampon, l’exemple vérifie si la durée de vie de 5 secondes de l’objet a été atteinte. dans ce cas, [**ISpatialAudioObject :: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) est appelé pour permettre au pipeline audio de savoir qu’aucun son n’est écrit à l’aide de cet objet et que l’objet est défini sur **nullptr** pour libérer ses ressources.

Après avoir écrit des données sur tous vos objets audio, appelez [**ISpatialAudioObjectRenderStream :: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) pour permettre au système de savoir que les données sont prêtes pour le rendu. Vous pouvez uniquement appeler **GetBuffer** entre un appel à **BeginUpdatingAudioObjects** et **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



Lorsque vous avez terminé le rendu de l’audio spatial, arrêtez le flux audio spatial en appelant [**ISpatialAudioObjectRenderStream :: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Si vous n’allez pas réutiliser le flux, libérez ses ressources en appelant [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



La méthode d’assistance **WriteToAudioObjectBuffer** écrit une mémoire tampon complète d’exemples ou le nombre d’échantillons restants spécifiés par notre limite de temps définie par l’application. Cela peut également être déterminé par le nombre d’échantillons restants dans un fichier audio source, par exemple. Une vague sine simple, dont la fréquence est mise à l’échelle par le paramètre d’entrée *Frequency* , est générée et écrite dans la mémoire tampon.


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Restituer l’audio à l’aide d’objets audio spatiales dynamiques

Les objets dynamiques vous permettent de restituer l’audio à partir d’une position arbitraire dans l’espace, par rapport à l’utilisateur. La position et le volume d’un objet audio dynamique peuvent être modifiés au fil du temps. Les jeux utilisent généralement la position d’un objet 3D dans le monde du jeu pour spécifier la position de l’objet audio dynamique qui lui est associé. L’exemple suivant utilise une structure simple, **My3dObject**, pour stocker l’ensemble minimal de données nécessaires pour représenter un objet. Ces données incluent un pointeur vers un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), la position, la vélocité, le volume et la fréquence tonale de l’objet, ainsi qu’une valeur qui stocke le nombre total de frames pour lesquels l’objet doit restituer le son.


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



Les étapes d’implémentation des objets audio dynamiques sont essentiellement les mêmes que les étapes des objets audio statiques décrits ci-dessus. Tout d’abord, procurez-vous un point de terminaison audio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Ensuite, initialisez le flux audio spatial. Récupérez une instance de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Appelez [**ISpatialAudioClient :: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) pour vous assurer que le format audio que vous utilisez est pris en charge. Créez un événement que le pipeline audio utilisera pour indiquer à l’application qu’elle est prête pour davantage de données audio.

Appelez [**ISpatialAudioClient :: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) pour récupérer le nombre d’objets dynamiques pris en charge par le système. Si cet appel retourne 0, les objets audio spatiales dynamiques ne sont pas pris en charge ou activés sur l’appareil actuel. Pour plus d’informations sur l’activation de l’audio spatial et pour plus d’informations sur le nombre d’objets audio dynamiques disponibles pour différents formats audio spatiaux, consultez [son spatial](spatial-sound.md).

Lors du remplissage de la structure [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , définissez le champ **MaxDynamicObjectCount** sur le nombre maximal d’objets dynamiques que votre application utilisera.

Appelez [**ISpatialAudioClient :: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) pour activer le flux.


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



Voici quelques exemples de code spécifique à l’application nécessaires pour prendre en charge cet exemple, qui génère dynamiquement des objets audio positionnés de manière aléatoire et les stocke dans un vecteur.


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



Avant d’entrer dans la boucle de rendu audio, appelez [**ISpatialAudioObjectRenderStream :: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) pour indiquer au pipeline de média de commencer à demander des données audio.

À l’intérieur de la boucle de rendu, attendez l’événement de fin de la mémoire tampon fourni lorsque le flux audio spatial a été initialisé pour être signalé. Vous devez définir une limite de délai d’expiration raisonnable, telle que 100 ms, lors de l’attente de l’événement, car toute modification apportée au type de rendu ou au point de terminaison entraînera la non-signalisation de cet événement. Dans ce cas, vous pouvez appeler [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) pour tenter de réinitialiser le flux audio spatial.

Ensuite, appelez [**ISpatialAudioObjectRenderStream :: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) pour informer le système que vous êtes sur le le courant de remplir les mémoires tampons des objets audio avec des données. Cette méthode retourne le nombre d’objets audio dynamiques disponibles et le nombre de frames de la mémoire tampon pour les objets audio restitués par ce flux.

Chaque fois que le compteur de génération atteint la valeur spécifiée, nous activons un nouvel objet audio dynamique en appelant [**ISpatialAudioObjectRenderStream :: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) en spécifiant [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Si tous les objets audio dynamiques disponibles ont déjà été alloués, cette méthode retourne **SPLAUDCLNT \_ E \_ n’a plus d' \_ \_ objets**. Dans ce cas, vous pouvez choisir de libérer un ou plusieurs objets audio précédemment activés en fonction de la définition de vos priorités propres à votre application. Une fois l’objet audio dynamique créé, il est ajouté à une nouvelle structure **My3dObject** , avec la position aléatoire, la vélocité, le volume et les valeurs de fréquence, qui sont ensuite ajoutées à la liste des objets actifs.

Ensuite, effectuez une itération sur tous les objets actifs, représentés dans cet exemple avec la structure **My3dObject** définie par l’application. Pour chaque objet audio, appelez [**ISpatialAudioObject :: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) pour obtenir un pointeur vers la mémoire tampon audio de l’objet audio spatial. Cette méthode retourne également la taille de la mémoire tampon, en octets. La méthode d’assistance, **WriteToAudioObjectBuffer**, pour remplir la mémoire tampon avec des données audio. Après avoir écrit dans la mémoire tampon, l’exemple met à jour la position de l’objet audio dynamique en appelant [**ISpatialAudioObject :: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). Le volume de l’objet audio peut également être modifié en appelant [**setVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume). Si vous ne mettez pas à jour la position ou le volume de l’objet, il conserve la position et le volume de la dernière fois qu’il a été défini. Si la durée de vie définie par l’application de l’objet a été atteinte, [**ISpatialAudioObject :: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) est appelé pour permettre au pipeline audio de savoir qu’aucun son n’est écrit à l’aide de cet objet et que l’objet est défini sur **nullptr** pour libérer ses ressources.

Après avoir écrit des données sur tous vos objets audio, appelez [**ISpatialAudioObjectRenderStream :: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) pour permettre au système de savoir que les données sont prêtes pour le rendu. Vous pouvez uniquement appeler **GetBuffer** entre un appel à **BeginUpdatingAudioObjects** et **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



Lorsque vous avez terminé le rendu de l’audio spatial, arrêtez le flux audio spatial en appelant [**ISpatialAudioObjectRenderStream :: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Si vous n’allez pas réutiliser le flux, libérez ses ressources en appelant [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Rendu audio à l’aide d’objets audio spatiales dynamiques pour HRTF

Un autre ensemble d’API, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) et [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), active l’audio spatial qui utilise la fonction de transfert de tête (HRTF) de Microsoft pour atténuer les sons afin de simuler la position de l’émetteur dans l’espace, par rapport à l’utilisateur, qui peut être modifiée dans le temps. En plus de la position, les objets audio HRTF vous permettent de spécifier une orientation dans l’espace, une direction dans laquelle le son est émis, tel qu’une forme conique ou cardioïde, et un modèle de dégradation lorsque l’objet se déplace plus près de l’écouteur virtuel. Notez que ces interfaces HRTF ne sont disponibles que lorsque l’utilisateur a sélectionné Windows Sonic pour casque comme moteur audio spatial pour l’appareil. Pour plus d’informations sur la configuration d’un appareil pour utiliser Windows Sonic pour casque, consultez [son spatial](spatial-sound.md).

Les API [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) et [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) permettent à une application d’utiliser explicitement le chemin d’accès de rendu Windows Sonic pour casque directement. Ces API ne prennent pas en charge les formats de son spatial, tels que Dolby Atmos pour Home Theater ou Dolby Atmos pour casque, ni le basculement de format de sortie contrôlé par le consommateur via le panneau de configuration **audio** , ni la lecture sur les haut-parleurs. Ces interfaces sont destinées à être utilisées dans les applications Windows Mixed realer qui souhaitent utiliser Windows Sonic pour les fonctionnalités spécifiques aux casques (telles que les présélections environnementales et les Rolloff basées sur les distances spécifiés par programmation, en dehors des pipelines de création de contenu classiques). La plupart des jeux et des scénarios de réalité virtuelle préfèrent utiliser [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) à la place. Les étapes d’implémentation pour les deux ensembles d’API étant presque identiques, il est possible d’implémenter les deux technologies et de basculer au moment de l’exécution en fonction de la fonctionnalité disponible sur l’appareil actuel.

En général, les applications de réalité mixte utilisent la position d’un objet 3D dans le monde virtuel pour spécifier la position de l’objet audio dynamique qui lui est associé. L’exemple suivant utilise une structure simple, **My3dObjectForHrtf**, pour stocker l’ensemble minimal de données nécessaires pour représenter un objet. Ces données incluent un pointeur vers un [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), la position, l’orientation, la vélocité et la fréquence tonale de l’objet, ainsi qu’une valeur qui stocke le nombre total de frames pour lesquels l’objet doit restituer le son.


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



Les étapes d’implémentation pour les objets HRTF audio dynamiques sont en grande partie les mêmes que les étapes pour les objets audio dynamiques décrits dans la section précédente. Tout d’abord, procurez-vous un point de terminaison audio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Ensuite, initialisez le flux audio spatial. Récupérez une instance de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Appelez [**ISpatialAudioClient :: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) pour vous assurer que le format audio que vous utilisez est pris en charge. Créez un événement que le pipeline audio utilisera pour indiquer à l’application qu’elle est prête pour davantage de données audio.

Appelez [**ISpatialAudioClient :: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) pour récupérer le nombre d’objets dynamiques pris en charge par le système. Si cet appel retourne 0, les objets audio spatiales dynamiques ne sont pas pris en charge ou activés sur l’appareil actuel. Pour plus d’informations sur l’activation de l’audio spatial et pour plus d’informations sur le nombre d’objets audio dynamiques disponibles pour différents formats audio spatiaux, consultez [son spatial](spatial-sound.md).

Lors du remplissage de la structure [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) , définissez le champ **MaxDynamicObjectCount** sur le nombre maximal d’objets dynamiques que votre application utilisera. Les paramètres d’activation pour HRTF prennent en charge quelques paramètres supplémentaires, tels que [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)et [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), qui spécifient les valeurs par défaut de ces paramètres pour les nouveaux objets créés à partir du flux. Ces paramètres sont facultatifs. Définissez les champs sur **nullptr** pour ne fournir aucune valeur par défaut.

Appelez [**ISpatialAudioClient :: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) pour activer le flux.


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



Voici quelques exemples de code spécifique à l’application nécessaires pour prendre en charge cet exemple, qui génère dynamiquement des objets audio positionnés de manière aléatoire et les stocke dans un vecteur.


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



Avant d’entrer dans la boucle de rendu audio, appelez [**ISpatialAudioObjectRenderStreamForHrtf :: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) pour indiquer au pipeline de média de commencer à demander des données audio.

À l’intérieur de la boucle de rendu, attendez l’événement de fin de la mémoire tampon fourni lorsque le flux audio spatial a été initialisé pour être signalé. Vous devez définir une limite de délai d’expiration raisonnable, telle que 100 ms, lors de l’attente de l’événement, car toute modification apportée au type de rendu ou au point de terminaison entraînera la non-signalisation de cet événement. Dans ce cas, vous pouvez appeler [**ISpatialAudioRenderStreamForHrtf :: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) pour tenter de réinitialiser le flux audio spatial.

Ensuite, appelez [**ISpatialAudioRenderStreamForHrtf :: BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) pour informer le système que vous êtes sur le le courant de remplir les mémoires tampons des objets audio avec des données. Cette méthode retourne le nombre d’objets audio dynamiques disponibles, non utilisés dans cet exemple, et le nombre de frames de la mémoire tampon pour les objets audio restitués par ce flux.

Chaque fois que le compteur de génération atteint la valeur spécifiée, nous activons un nouvel objet audio dynamique en appelant [**ISpatialAudioRenderStreamForHrtf :: ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) en spécifiant [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Si tous les objets audio dynamiques disponibles ont déjà été alloués, cette méthode retourne **SPLAUDCLNT \_ E \_ n’a plus d' \_ \_ objets**. Dans ce cas, vous pouvez choisir de libérer un ou plusieurs objets audio précédemment activés en fonction de la définition de vos priorités propres à votre application. Une fois l’objet audio dynamique créé, il est ajouté à une nouvelle structure **My3dObjectForHrtf** , avec la position aléatoire, la rotation, la vélocité, le volume et les valeurs de fréquence, qui sont ensuite ajoutées à la liste des objets actifs.

Ensuite, effectuez une itération sur tous les objets actifs, représentés dans cet exemple avec la structure **My3dObjectForHrtf** définie par l’application. Pour chaque objet audio, appelez [**ISpatialAudioObjectForHrtf :: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) pour obtenir un pointeur vers la mémoire tampon audio de l’objet audio spatial. Cette méthode retourne également la taille de la mémoire tampon, en octets. La méthode d’assistance, **WriteToAudioObjectBuffer**, décrite précédemment dans cet article, permet de remplir la mémoire tampon avec des données audio. Après avoir écrit dans la mémoire tampon, l’exemple met à jour la position et l’orientation de l’objet audio HRTF en appelant [**ISpatialAudioObjectForHrtf :: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) et [**ISpatialAudioObjectForHrtf :: SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation). Dans cet exemple, une méthode d’assistance, **CalculateEmitterConeOrientationMatrix**, est utilisée pour calculer la matrice d’orientation en fonction de la direction vers laquelle l’objet 3D pointe. L’implémentation de cette méthode est illustrée ci-dessous. Le volume de l’objet audio peut également être modifié en appelant [**ISpatialAudioObjectForHrtf :: SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain). Si vous ne mettez pas à jour la position, l’orientation ou le volume de l’objet, il conserve la position, l’orientation et le volume de la dernière fois qu’il a été défini. Si la durée de vie définie par l’application de l’objet a été atteinte, [**ISpatialAudioObjectForHrtf :: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) est appelé pour permettre au pipeline audio de savoir qu’aucun son n’est écrit à l’aide de cet objet et que l’objet est défini sur **nullptr** pour libérer ses ressources.

Après avoir écrit des données sur tous vos objets audio, appelez [**ISpatialAudioRenderStreamForHrtf :: EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) pour permettre au système de savoir que les données sont prêtes pour le rendu. Vous pouvez uniquement appeler **GetBuffer** entre un appel à **BeginUpdatingAudioObjects** et **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



Lorsque vous avez terminé le rendu de l’audio spatial, arrêtez le flux audio spatial en appelant [**ISpatialAudioRenderStreamForHrtf :: Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)). Si vous n’allez pas réutiliser le flux, libérez ses ressources en appelant [**ISpatialAudioRenderStreamForHrtf :: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



L’exemple de code suivant montre l’implémentation de la méthode d’assistance **CalculateEmitterConeOrientationMatrix** qui a été utilisée dans l’exemple ci-dessus pour calculer la matrice d’orientation en fonction de la direction vers laquelle l’objet 3D pointe.


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Son spatial](spatial-sound.md)
</dt> <dt>

[**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
