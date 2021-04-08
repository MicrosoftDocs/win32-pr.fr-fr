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
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="c985b-103">Restituer le son spatial à l’aide d’objets audio spatiaux</span><span class="sxs-lookup"><span data-stu-id="c985b-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="c985b-104">Cet article présente des exemples simples qui illustrent comment implémenter un son spatial à l’aide d’objets audio spatiaux statiques, d’objets audio spatiaux dynamiques et d’objets audio spatiaux qui utilisent la fonction de transfert relatif de l’en-tête de Microsoft (HRTF).</span><span class="sxs-lookup"><span data-stu-id="c985b-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="c985b-105">Les étapes d’implémentation pour ces trois techniques sont très similaires et cet article fournit un exemple de code structuré de la même façon pour chaque technique.</span><span class="sxs-lookup"><span data-stu-id="c985b-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="c985b-106">Pour obtenir des exemples complets d’implémentations de son spatial réel, consultez le [dépôt github des exemples de son spatial Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span><span class="sxs-lookup"><span data-stu-id="c985b-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="c985b-107">Pour une vue d’ensemble de Windows Sonic, la solution de niveau plate-forme de Microsoft pour la prise en charge des sons spatiaux sur Xbox et Windows, consultez [son spatial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c985b-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="c985b-108">Rendu audio à l’aide d’objets audio spatiaux statiques</span><span class="sxs-lookup"><span data-stu-id="c985b-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="c985b-109">Un objet audio statique est utilisé pour restituer le son à l’un des 18 canaux audio statiques définis dans l’énumération [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) .</span><span class="sxs-lookup"><span data-stu-id="c985b-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="c985b-110">Chacun de ces canaux représente un orateur réel ou virtualisé à un point fixe dans l’espace qui ne se déplace pas au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="c985b-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="c985b-111">Les canaux statiques qui sont disponibles sur un appareil particulier dépendent du format de son spatial utilisé.</span><span class="sxs-lookup"><span data-stu-id="c985b-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="c985b-112">Pour obtenir la liste des formats pris en charge et de leurs nombres de canaux, consultez [son spatial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c985b-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c985b-113">Lorsque vous initialisez un flux audio spatial, vous devez spécifier les canaux statiques disponibles que le flux utilisera.</span><span class="sxs-lookup"><span data-stu-id="c985b-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="c985b-114">Les exemples de définitions de constantes suivants peuvent être utilisés pour spécifier des configurations d’orateur courantes et obtenir le nombre de canaux disponibles pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="c985b-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


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



<span data-ttu-id="c985b-115">La première étape du rendu de l’audio spatial consiste à obtenir le point de terminaison audio vers lequel les données audio seront envoyées.</span><span class="sxs-lookup"><span data-stu-id="c985b-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="c985b-116">Créez une instance de [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) et appelez [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour obtenir le périphérique de rendu audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="c985b-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="c985b-117">Lorsque vous créez un flux audio spatial, vous devez spécifier le format audio utilisé par le flux en fournissant une structure [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c985b-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="c985b-118">Si vous jouez des données audio à partir d’un fichier, le format est généralement déterminé par le format de fichier audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="c985b-119">Cet exemple utilise un format mono, 32 bits, 48Hz.</span><span class="sxs-lookup"><span data-stu-id="c985b-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


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



<span data-ttu-id="c985b-120">L’étape suivante du rendu de l’audio spatial consiste à initialiser un flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="c985b-121">Tout d’abord, récupérez une instance de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="c985b-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="c985b-122">Appelez [**ISpatialAudioClient :: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) pour vous assurer que le format audio que vous utilisez est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c985b-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="c985b-123">Créez un événement que le pipeline audio utilisera pour indiquer à l’application qu’elle est prête pour davantage de données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="c985b-124">Remplir une structure [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) qui sera utilisée pour initialiser le flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="c985b-125">Dans cet exemple, le champ **StaticObjectTypeMask** est défini sur la **constante \_ stéréo ChannelMask** définie précédemment dans cet article, ce qui signifie que seuls les canaux avant droit et gauche peuvent être utilisés par le flux audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="c985b-126">Étant donné que cet exemple utilise uniquement des objets audio statiques et aucun objet dynamique, le champ **MaxDynamicObjectCount** a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="c985b-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="c985b-127">Le champ **Category** est défini sur un membre de l’énumération de [**\_ \_ catégorie de flux audio**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , qui définit la façon dont le système mélange le son de ce flux avec d’autres sources audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="c985b-128">Appelez [**ISpatialAudioClient :: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) pour activer le flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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
> <span data-ttu-id="c985b-129">Lorsque vous utilisez les interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) sur un titre de kit de développement Xbox One (XDK), vous devez d’abord appeler **EnableSpatialAudio** avant d’appeler [**IMMDeviceEnumerator :: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) ou [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="c985b-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="c985b-130">Dans le cas contraire, une \_ erreur E nointerface est retournée à partir de l’appel à Activate.</span><span class="sxs-lookup"><span data-stu-id="c985b-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="c985b-131">**EnableSpatialAudio** est uniquement disponible pour les titres XDK, et n’a pas besoin d’être appelé pour les applications plateforme Windows universelle s’exécutant sur Xbox One, ni pour les appareils non-Xbox One.</span><span class="sxs-lookup"><span data-stu-id="c985b-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="c985b-132">Déclarez un pointeur pour un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) qui sera utilisé pour écrire des données audio dans un canal statique.</span><span class="sxs-lookup"><span data-stu-id="c985b-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="c985b-133">Les applications classiques utilisent un objet pour chaque canal spécifié dans le champ **StaticObjectTypeMask** .</span><span class="sxs-lookup"><span data-stu-id="c985b-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="c985b-134">Par souci de simplicité, cet exemple utilise uniquement un seul objet audio statique.</span><span class="sxs-lookup"><span data-stu-id="c985b-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="c985b-135">Avant d’entrer dans la boucle de rendu audio, appelez [**ISpatialAudioObjectRenderStream :: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) pour indiquer au pipeline de média de commencer à demander des données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="c985b-136">Cet exemple utilise un compteur pour arrêter le rendu de l’audio après 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="c985b-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="c985b-137">À l’intérieur de la boucle de rendu, attendez l’événement de fin de la mémoire tampon, fourni lorsque le flux de données audio spatiales a été initialisé, à signaler.</span><span class="sxs-lookup"><span data-stu-id="c985b-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="c985b-138">Vous devez définir une limite de délai d’expiration raisonnable, telle que 100 ms, lors de l’attente de l’événement, car toute modification apportée au type de rendu ou au point de terminaison entraînera la non-signalisation de cet événement.</span><span class="sxs-lookup"><span data-stu-id="c985b-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="c985b-139">Dans ce cas, vous pouvez appeler [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) pour tenter de réinitialiser le flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="c985b-140">Ensuite, appelez [**ISpatialAudioObjectRenderStream :: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) pour informer le système que vous êtes sur le le courant de remplir les mémoires tampons des objets audio avec des données.</span><span class="sxs-lookup"><span data-stu-id="c985b-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="c985b-141">Cette méthode retourne le nombre d’objets audio dynamiques disponibles, non utilisés dans cet exemple, et le nombre de frames de la mémoire tampon pour les objets audio restitués par ce flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="c985b-142">Si un objet audio spatial statique n’a pas encore été créé, créez-en un ou plusieurs en appelant [**ISpatialAudioObjectRenderStream :: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), en passant une valeur de l’énumération [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) indiquant le canal statique vers lequel le son de l’objet est restitué.</span><span class="sxs-lookup"><span data-stu-id="c985b-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="c985b-143">Ensuite, appelez [**ISpatialAudioObject :: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) pour obtenir un pointeur vers la mémoire tampon audio de l’objet audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="c985b-144">Cette méthode retourne également la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="c985b-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="c985b-145">Cet exemple utilise une méthode d’assistance, **WriteToAudioObjectBuffer**, pour remplir la mémoire tampon avec des données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="c985b-146">Cette méthode est présentée plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c985b-146">This method is shown later in this article.</span></span> <span data-ttu-id="c985b-147">Après avoir écrit dans la mémoire tampon, l’exemple vérifie si la durée de vie de 5 secondes de l’objet a été atteinte. dans ce cas, [**ISpatialAudioObject :: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) est appelé pour permettre au pipeline audio de savoir qu’aucun son n’est écrit à l’aide de cet objet et que l’objet est défini sur **nullptr** pour libérer ses ressources.</span><span class="sxs-lookup"><span data-stu-id="c985b-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="c985b-148">Après avoir écrit des données sur tous vos objets audio, appelez [**ISpatialAudioObjectRenderStream :: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) pour permettre au système de savoir que les données sont prêtes pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="c985b-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="c985b-149">Vous pouvez uniquement appeler **GetBuffer** entre un appel à **BeginUpdatingAudioObjects** et **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="c985b-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="c985b-150">Lorsque vous avez terminé le rendu de l’audio spatial, arrêtez le flux audio spatial en appelant [**ISpatialAudioObjectRenderStream :: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="c985b-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="c985b-151">Si vous n’allez pas réutiliser le flux, libérez ses ressources en appelant [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="c985b-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="c985b-152">La méthode d’assistance **WriteToAudioObjectBuffer** écrit une mémoire tampon complète d’exemples ou le nombre d’échantillons restants spécifiés par notre limite de temps définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="c985b-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="c985b-153">Cela peut également être déterminé par le nombre d’échantillons restants dans un fichier audio source, par exemple.</span><span class="sxs-lookup"><span data-stu-id="c985b-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="c985b-154">Une vague sine simple, dont la fréquence est mise à l’échelle par le paramètre d’entrée *Frequency* , est générée et écrite dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c985b-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="c985b-155">Restituer l’audio à l’aide d’objets audio spatiales dynamiques</span><span class="sxs-lookup"><span data-stu-id="c985b-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="c985b-156">Les objets dynamiques vous permettent de restituer l’audio à partir d’une position arbitraire dans l’espace, par rapport à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c985b-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="c985b-157">La position et le volume d’un objet audio dynamique peuvent être modifiés au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="c985b-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="c985b-158">Les jeux utilisent généralement la position d’un objet 3D dans le monde du jeu pour spécifier la position de l’objet audio dynamique qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="c985b-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="c985b-159">L’exemple suivant utilise une structure simple, **My3dObject**, pour stocker l’ensemble minimal de données nécessaires pour représenter un objet.</span><span class="sxs-lookup"><span data-stu-id="c985b-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="c985b-160">Ces données incluent un pointeur vers un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), la position, la vélocité, le volume et la fréquence tonale de l’objet, ainsi qu’une valeur qui stocke le nombre total de frames pour lesquels l’objet doit restituer le son.</span><span class="sxs-lookup"><span data-stu-id="c985b-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


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



<span data-ttu-id="c985b-161">Les étapes d’implémentation des objets audio dynamiques sont essentiellement les mêmes que les étapes des objets audio statiques décrits ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c985b-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="c985b-162">Tout d’abord, procurez-vous un point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="c985b-163">Ensuite, initialisez le flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="c985b-164">Récupérez une instance de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="c985b-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="c985b-165">Appelez [**ISpatialAudioClient :: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) pour vous assurer que le format audio que vous utilisez est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c985b-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="c985b-166">Créez un événement que le pipeline audio utilisera pour indiquer à l’application qu’elle est prête pour davantage de données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="c985b-167">Appelez [**ISpatialAudioClient :: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) pour récupérer le nombre d’objets dynamiques pris en charge par le système.</span><span class="sxs-lookup"><span data-stu-id="c985b-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="c985b-168">Si cet appel retourne 0, les objets audio spatiales dynamiques ne sont pas pris en charge ou activés sur l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="c985b-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="c985b-169">Pour plus d’informations sur l’activation de l’audio spatial et pour plus d’informations sur le nombre d’objets audio dynamiques disponibles pour différents formats audio spatiaux, consultez [son spatial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c985b-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c985b-170">Lors du remplissage de la structure [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , définissez le champ **MaxDynamicObjectCount** sur le nombre maximal d’objets dynamiques que votre application utilisera.</span><span class="sxs-lookup"><span data-stu-id="c985b-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="c985b-171">Appelez [**ISpatialAudioClient :: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) pour activer le flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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



<span data-ttu-id="c985b-172">Voici quelques exemples de code spécifique à l’application nécessaires pour prendre en charge cet exemple, qui génère dynamiquement des objets audio positionnés de manière aléatoire et les stocke dans un vecteur.</span><span class="sxs-lookup"><span data-stu-id="c985b-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


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



<span data-ttu-id="c985b-173">Avant d’entrer dans la boucle de rendu audio, appelez [**ISpatialAudioObjectRenderStream :: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) pour indiquer au pipeline de média de commencer à demander des données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="c985b-174">À l’intérieur de la boucle de rendu, attendez l’événement de fin de la mémoire tampon fourni lorsque le flux audio spatial a été initialisé pour être signalé.</span><span class="sxs-lookup"><span data-stu-id="c985b-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="c985b-175">Vous devez définir une limite de délai d’expiration raisonnable, telle que 100 ms, lors de l’attente de l’événement, car toute modification apportée au type de rendu ou au point de terminaison entraînera la non-signalisation de cet événement.</span><span class="sxs-lookup"><span data-stu-id="c985b-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="c985b-176">Dans ce cas, vous pouvez appeler [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) pour tenter de réinitialiser le flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="c985b-177">Ensuite, appelez [**ISpatialAudioObjectRenderStream :: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) pour informer le système que vous êtes sur le le courant de remplir les mémoires tampons des objets audio avec des données.</span><span class="sxs-lookup"><span data-stu-id="c985b-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="c985b-178">Cette méthode retourne le nombre d’objets audio dynamiques disponibles et le nombre de frames de la mémoire tampon pour les objets audio restitués par ce flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="c985b-179">Chaque fois que le compteur de génération atteint la valeur spécifiée, nous activons un nouvel objet audio dynamique en appelant [**ISpatialAudioObjectRenderStream :: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) en spécifiant [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="c985b-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="c985b-180">Si tous les objets audio dynamiques disponibles ont déjà été alloués, cette méthode retourne **SPLAUDCLNT \_ E \_ n’a plus d' \_ \_ objets**.</span><span class="sxs-lookup"><span data-stu-id="c985b-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="c985b-181">Dans ce cas, vous pouvez choisir de libérer un ou plusieurs objets audio précédemment activés en fonction de la définition de vos priorités propres à votre application.</span><span class="sxs-lookup"><span data-stu-id="c985b-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="c985b-182">Une fois l’objet audio dynamique créé, il est ajouté à une nouvelle structure **My3dObject** , avec la position aléatoire, la vélocité, le volume et les valeurs de fréquence, qui sont ensuite ajoutées à la liste des objets actifs.</span><span class="sxs-lookup"><span data-stu-id="c985b-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="c985b-183">Ensuite, effectuez une itération sur tous les objets actifs, représentés dans cet exemple avec la structure **My3dObject** définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="c985b-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="c985b-184">Pour chaque objet audio, appelez [**ISpatialAudioObject :: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) pour obtenir un pointeur vers la mémoire tampon audio de l’objet audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="c985b-185">Cette méthode retourne également la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="c985b-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="c985b-186">La méthode d’assistance, **WriteToAudioObjectBuffer**, pour remplir la mémoire tampon avec des données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="c985b-187">Après avoir écrit dans la mémoire tampon, l’exemple met à jour la position de l’objet audio dynamique en appelant [**ISpatialAudioObject :: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span><span class="sxs-lookup"><span data-stu-id="c985b-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="c985b-188">Le volume de l’objet audio peut également être modifié en appelant [**setVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span><span class="sxs-lookup"><span data-stu-id="c985b-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="c985b-189">Si vous ne mettez pas à jour la position ou le volume de l’objet, il conserve la position et le volume de la dernière fois qu’il a été défini.</span><span class="sxs-lookup"><span data-stu-id="c985b-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="c985b-190">Si la durée de vie définie par l’application de l’objet a été atteinte, [**ISpatialAudioObject :: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) est appelé pour permettre au pipeline audio de savoir qu’aucun son n’est écrit à l’aide de cet objet et que l’objet est défini sur **nullptr** pour libérer ses ressources.</span><span class="sxs-lookup"><span data-stu-id="c985b-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="c985b-191">Après avoir écrit des données sur tous vos objets audio, appelez [**ISpatialAudioObjectRenderStream :: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) pour permettre au système de savoir que les données sont prêtes pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="c985b-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="c985b-192">Vous pouvez uniquement appeler **GetBuffer** entre un appel à **BeginUpdatingAudioObjects** et **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="c985b-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="c985b-193">Lorsque vous avez terminé le rendu de l’audio spatial, arrêtez le flux audio spatial en appelant [**ISpatialAudioObjectRenderStream :: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="c985b-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="c985b-194">Si vous n’allez pas réutiliser le flux, libérez ses ressources en appelant [**ISpatialAudioObjectRenderStream :: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="c985b-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="c985b-195">Rendu audio à l’aide d’objets audio spatiales dynamiques pour HRTF</span><span class="sxs-lookup"><span data-stu-id="c985b-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="c985b-196">Un autre ensemble d’API, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) et [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), active l’audio spatial qui utilise la fonction de transfert de tête (HRTF) de Microsoft pour atténuer les sons afin de simuler la position de l’émetteur dans l’espace, par rapport à l’utilisateur, qui peut être modifiée dans le temps.</span><span class="sxs-lookup"><span data-stu-id="c985b-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="c985b-197">En plus de la position, les objets audio HRTF vous permettent de spécifier une orientation dans l’espace, une direction dans laquelle le son est émis, tel qu’une forme conique ou cardioïde, et un modèle de dégradation lorsque l’objet se déplace plus près de l’écouteur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c985b-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="c985b-198">Notez que ces interfaces HRTF ne sont disponibles que lorsque l’utilisateur a sélectionné Windows Sonic pour casque comme moteur audio spatial pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c985b-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="c985b-199">Pour plus d’informations sur la configuration d’un appareil pour utiliser Windows Sonic pour casque, consultez [son spatial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c985b-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c985b-200">Les API [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) et [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) permettent à une application d’utiliser explicitement le chemin d’accès de rendu Windows Sonic pour casque directement.</span><span class="sxs-lookup"><span data-stu-id="c985b-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="c985b-201">Ces API ne prennent pas en charge les formats de son spatial, tels que Dolby Atmos pour Home Theater ou Dolby Atmos pour casque, ni le basculement de format de sortie contrôlé par le consommateur via le panneau de configuration **audio** , ni la lecture sur les haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="c985b-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="c985b-202">Ces interfaces sont destinées à être utilisées dans les applications Windows Mixed realer qui souhaitent utiliser Windows Sonic pour les fonctionnalités spécifiques aux casques (telles que les présélections environnementales et les Rolloff basées sur les distances spécifiés par programmation, en dehors des pipelines de création de contenu classiques).</span><span class="sxs-lookup"><span data-stu-id="c985b-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="c985b-203">La plupart des jeux et des scénarios de réalité virtuelle préfèrent utiliser [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) à la place.</span><span class="sxs-lookup"><span data-stu-id="c985b-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="c985b-204">Les étapes d’implémentation pour les deux ensembles d’API étant presque identiques, il est possible d’implémenter les deux technologies et de basculer au moment de l’exécution en fonction de la fonctionnalité disponible sur l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="c985b-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="c985b-205">En général, les applications de réalité mixte utilisent la position d’un objet 3D dans le monde virtuel pour spécifier la position de l’objet audio dynamique qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="c985b-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="c985b-206">L’exemple suivant utilise une structure simple, **My3dObjectForHrtf**, pour stocker l’ensemble minimal de données nécessaires pour représenter un objet.</span><span class="sxs-lookup"><span data-stu-id="c985b-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="c985b-207">Ces données incluent un pointeur vers un [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), la position, l’orientation, la vélocité et la fréquence tonale de l’objet, ainsi qu’une valeur qui stocke le nombre total de frames pour lesquels l’objet doit restituer le son.</span><span class="sxs-lookup"><span data-stu-id="c985b-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


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



<span data-ttu-id="c985b-208">Les étapes d’implémentation pour les objets HRTF audio dynamiques sont en grande partie les mêmes que les étapes pour les objets audio dynamiques décrits dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="c985b-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="c985b-209">Tout d’abord, procurez-vous un point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="c985b-210">Ensuite, initialisez le flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="c985b-211">Récupérez une instance de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="c985b-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="c985b-212">Appelez [**ISpatialAudioClient :: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) pour vous assurer que le format audio que vous utilisez est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c985b-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="c985b-213">Créez un événement que le pipeline audio utilisera pour indiquer à l’application qu’elle est prête pour davantage de données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="c985b-214">Appelez [**ISpatialAudioClient :: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) pour récupérer le nombre d’objets dynamiques pris en charge par le système.</span><span class="sxs-lookup"><span data-stu-id="c985b-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="c985b-215">Si cet appel retourne 0, les objets audio spatiales dynamiques ne sont pas pris en charge ou activés sur l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="c985b-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="c985b-216">Pour plus d’informations sur l’activation de l’audio spatial et pour plus d’informations sur le nombre d’objets audio dynamiques disponibles pour différents formats audio spatiaux, consultez [son spatial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c985b-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c985b-217">Lors du remplissage de la structure [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) , définissez le champ **MaxDynamicObjectCount** sur le nombre maximal d’objets dynamiques que votre application utilisera.</span><span class="sxs-lookup"><span data-stu-id="c985b-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="c985b-218">Les paramètres d’activation pour HRTF prennent en charge quelques paramètres supplémentaires, tels que [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)et [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), qui spécifient les valeurs par défaut de ces paramètres pour les nouveaux objets créés à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="c985b-219">Ces paramètres sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="c985b-219">These parameters are optional.</span></span> <span data-ttu-id="c985b-220">Définissez les champs sur **nullptr** pour ne fournir aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c985b-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="c985b-221">Appelez [**ISpatialAudioClient :: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) pour activer le flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


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



<span data-ttu-id="c985b-222">Voici quelques exemples de code spécifique à l’application nécessaires pour prendre en charge cet exemple, qui génère dynamiquement des objets audio positionnés de manière aléatoire et les stocke dans un vecteur.</span><span class="sxs-lookup"><span data-stu-id="c985b-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


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



<span data-ttu-id="c985b-223">Avant d’entrer dans la boucle de rendu audio, appelez [**ISpatialAudioObjectRenderStreamForHrtf :: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) pour indiquer au pipeline de média de commencer à demander des données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="c985b-224">À l’intérieur de la boucle de rendu, attendez l’événement de fin de la mémoire tampon fourni lorsque le flux audio spatial a été initialisé pour être signalé.</span><span class="sxs-lookup"><span data-stu-id="c985b-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="c985b-225">Vous devez définir une limite de délai d’expiration raisonnable, telle que 100 ms, lors de l’attente de l’événement, car toute modification apportée au type de rendu ou au point de terminaison entraînera la non-signalisation de cet événement.</span><span class="sxs-lookup"><span data-stu-id="c985b-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="c985b-226">Dans ce cas, vous pouvez appeler [**ISpatialAudioRenderStreamForHrtf :: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) pour tenter de réinitialiser le flux audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="c985b-227">Ensuite, appelez [**ISpatialAudioRenderStreamForHrtf :: BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) pour informer le système que vous êtes sur le le courant de remplir les mémoires tampons des objets audio avec des données.</span><span class="sxs-lookup"><span data-stu-id="c985b-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="c985b-228">Cette méthode retourne le nombre d’objets audio dynamiques disponibles, non utilisés dans cet exemple, et le nombre de frames de la mémoire tampon pour les objets audio restitués par ce flux.</span><span class="sxs-lookup"><span data-stu-id="c985b-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="c985b-229">Chaque fois que le compteur de génération atteint la valeur spécifiée, nous activons un nouvel objet audio dynamique en appelant [**ISpatialAudioRenderStreamForHrtf :: ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) en spécifiant [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="c985b-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="c985b-230">Si tous les objets audio dynamiques disponibles ont déjà été alloués, cette méthode retourne **SPLAUDCLNT \_ E \_ n’a plus d' \_ \_ objets**.</span><span class="sxs-lookup"><span data-stu-id="c985b-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="c985b-231">Dans ce cas, vous pouvez choisir de libérer un ou plusieurs objets audio précédemment activés en fonction de la définition de vos priorités propres à votre application.</span><span class="sxs-lookup"><span data-stu-id="c985b-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="c985b-232">Une fois l’objet audio dynamique créé, il est ajouté à une nouvelle structure **My3dObjectForHrtf** , avec la position aléatoire, la rotation, la vélocité, le volume et les valeurs de fréquence, qui sont ensuite ajoutées à la liste des objets actifs.</span><span class="sxs-lookup"><span data-stu-id="c985b-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="c985b-233">Ensuite, effectuez une itération sur tous les objets actifs, représentés dans cet exemple avec la structure **My3dObjectForHrtf** définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="c985b-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="c985b-234">Pour chaque objet audio, appelez [**ISpatialAudioObjectForHrtf :: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) pour obtenir un pointeur vers la mémoire tampon audio de l’objet audio spatial.</span><span class="sxs-lookup"><span data-stu-id="c985b-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="c985b-235">Cette méthode retourne également la taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="c985b-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="c985b-236">La méthode d’assistance, **WriteToAudioObjectBuffer**, décrite précédemment dans cet article, permet de remplir la mémoire tampon avec des données audio.</span><span class="sxs-lookup"><span data-stu-id="c985b-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="c985b-237">Après avoir écrit dans la mémoire tampon, l’exemple met à jour la position et l’orientation de l’objet audio HRTF en appelant [**ISpatialAudioObjectForHrtf :: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) et [**ISpatialAudioObjectForHrtf :: SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span><span class="sxs-lookup"><span data-stu-id="c985b-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="c985b-238">Dans cet exemple, une méthode d’assistance, **CalculateEmitterConeOrientationMatrix**, est utilisée pour calculer la matrice d’orientation en fonction de la direction vers laquelle l’objet 3D pointe.</span><span class="sxs-lookup"><span data-stu-id="c985b-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="c985b-239">L’implémentation de cette méthode est illustrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c985b-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="c985b-240">Le volume de l’objet audio peut également être modifié en appelant [**ISpatialAudioObjectForHrtf :: SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span><span class="sxs-lookup"><span data-stu-id="c985b-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="c985b-241">Si vous ne mettez pas à jour la position, l’orientation ou le volume de l’objet, il conserve la position, l’orientation et le volume de la dernière fois qu’il a été défini.</span><span class="sxs-lookup"><span data-stu-id="c985b-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="c985b-242">Si la durée de vie définie par l’application de l’objet a été atteinte, [**ISpatialAudioObjectForHrtf :: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) est appelé pour permettre au pipeline audio de savoir qu’aucun son n’est écrit à l’aide de cet objet et que l’objet est défini sur **nullptr** pour libérer ses ressources.</span><span class="sxs-lookup"><span data-stu-id="c985b-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="c985b-243">Après avoir écrit des données sur tous vos objets audio, appelez [**ISpatialAudioRenderStreamForHrtf :: EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) pour permettre au système de savoir que les données sont prêtes pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="c985b-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="c985b-244">Vous pouvez uniquement appeler **GetBuffer** entre un appel à **BeginUpdatingAudioObjects** et **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="c985b-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


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



<span data-ttu-id="c985b-245">Lorsque vous avez terminé le rendu de l’audio spatial, arrêtez le flux audio spatial en appelant [**ISpatialAudioRenderStreamForHrtf :: Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c985b-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="c985b-246">Si vous n’allez pas réutiliser le flux, libérez ses ressources en appelant [**ISpatialAudioRenderStreamForHrtf :: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c985b-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="c985b-247">L’exemple de code suivant montre l’implémentation de la méthode d’assistance **CalculateEmitterConeOrientationMatrix** qui a été utilisée dans l’exemple ci-dessus pour calculer la matrice d’orientation en fonction de la direction vers laquelle l’objet 3D pointe.</span><span class="sxs-lookup"><span data-stu-id="c985b-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c985b-248">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c985b-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c985b-249">Son spatial</span><span class="sxs-lookup"><span data-stu-id="c985b-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="c985b-250">**ISpatialAudioClient**</span><span class="sxs-lookup"><span data-stu-id="c985b-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="c985b-251">**ISpatialAudioObject**</span><span class="sxs-lookup"><span data-stu-id="c985b-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
