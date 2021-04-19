---
description: Définition des types de médias sur un DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Définition des types de médias sur un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523109"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="96750-103">Définition des types de médias sur un DMO</span><span class="sxs-lookup"><span data-stu-id="96750-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="96750-104">Avant qu’un DMO puisse traiter des données, le client doit définir le type de média pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="96750-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="96750-105">(Il existe une exception mineure pour cette règle ; consultez [flux facultatifs](optional-streams.md).) Pour rechercher le nombre de flux, appelez la méthode [**IMediaObject :: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :</span><span class="sxs-lookup"><span data-stu-id="96750-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="96750-106">Cette méthode retourne deux valeurs, le nombre d’entrées et le nombre de sorties.</span><span class="sxs-lookup"><span data-stu-id="96750-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="96750-107">Ces valeurs sont fixes pour la durée de vie de la DMO.</span><span class="sxs-lookup"><span data-stu-id="96750-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="96750-108">**Types préférés**</span><span class="sxs-lookup"><span data-stu-id="96750-108">**Preferred Types**</span></span>

<span data-ttu-id="96750-109">Pour chaque flux, DMO attribue une liste de types de média possibles, par ordre de préférence.</span><span class="sxs-lookup"><span data-stu-id="96750-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="96750-110">Par exemple, les types préférés peuvent être 32-RGB, RVB 24 bits et RVB 16 bits, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="96750-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="96750-111">Lorsque le client définit les types de médias, il peut utiliser ces listes comme un indicateur.</span><span class="sxs-lookup"><span data-stu-id="96750-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="96750-112">Pour récupérer un type préféré pour un flux, appelez la méthode [**IMediaObject :: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) ou [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="96750-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="96750-113">Spécifiez le numéro du flux et une valeur d’index pour le type (à partir de zéro).</span><span class="sxs-lookup"><span data-stu-id="96750-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="96750-114">Par exemple, le code suivant récupère le premier type préféré dans le premier flux d’entrée :</span><span class="sxs-lookup"><span data-stu-id="96750-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="96750-115">Pour énumérer tous les types de médias préférés sur un flux donné, utilisez une boucle qui incrémente l’index de type jusqu’à ce que la méthode retourne DMO \_ E \_ plus d' \_ \_ éléments, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="96750-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="96750-116">Vous devez noter les points suivants sur les types préférés :</span><span class="sxs-lookup"><span data-stu-id="96750-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="96750-117">DMO peut retourner un type qui n’a aucun bloc de format.</span><span class="sxs-lookup"><span data-stu-id="96750-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="96750-118">Par exemple, un DMO peut spécifier un type de vidéo, tel que RVB 24 bits, sans fournir la largeur et la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="96750-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="96750-119">Toutefois, lorsque vous définissez le type, vous devez fournir un bloc de format complet.</span><span class="sxs-lookup"><span data-stu-id="96750-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="96750-120">(Certains types de média, comme MIDI, ne requièrent jamais de bloc de format, auquel cas cette remarque ne s’applique pas.)</span><span class="sxs-lookup"><span data-stu-id="96750-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="96750-121">DMO n’est pas requis pour prendre en charge toutes les combinaisons de types préférés qu’il retourne.</span><span class="sxs-lookup"><span data-stu-id="96750-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="96750-122">Par exemple, si un DMO a deux flux et que chaque flux a quatre types préférés, il existe 16 combinaisons possibles, mais elles ne sont pas toutes garanties comme étant valides.</span><span class="sxs-lookup"><span data-stu-id="96750-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="96750-123">Lorsque le client définit le type de média pour un flux, DMO peut mettre à jour les types préférés pour d’autres flux afin de refléter le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="96750-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="96750-124">Toutefois, cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="96750-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="96750-125">Pour certains flux, DMO peut ne pas proposer de types préférés.</span><span class="sxs-lookup"><span data-stu-id="96750-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="96750-126">En règle générale, un DMO doit offrir au moins certains types préférés sur certains flux.</span><span class="sxs-lookup"><span data-stu-id="96750-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="96750-127">DMO n’est pas obligé d’offrir une liste complète des types de médias qu’il peut accepter.</span><span class="sxs-lookup"><span data-stu-id="96750-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="96750-128">Il peut y avoir des types « non publiés » pris en charge par DMO, mais qui ne sont pas proposés comme types préférés.</span><span class="sxs-lookup"><span data-stu-id="96750-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="96750-129">En bref, le client doit traiter les types préférés comme des indications uniquement.</span><span class="sxs-lookup"><span data-stu-id="96750-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="96750-130">La seule façon de savoir quels types sont pris en charge consiste à les tester, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="96750-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="96750-131">**Définition du type de média sur un flux**</span><span class="sxs-lookup"><span data-stu-id="96750-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="96750-132">Utilisez les méthodes [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) et [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) pour définir le type de chaque flux.</span><span class="sxs-lookup"><span data-stu-id="96750-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="96750-133">Vous devez fournir une structure de **\_ \_ type de média DMO** qui contient une description complète du type de média.</span><span class="sxs-lookup"><span data-stu-id="96750-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="96750-134">L’exemple suivant définit le type de média sur le flux d’entrée 0, à l’aide de l’audio PCM stéréo 44,1 kHz 16 bits :</span><span class="sxs-lookup"><span data-stu-id="96750-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="96750-135">Pour tester un type de média sans le définir, appelez **SetInputType** ou **SetOutputType** avec l' \_ indicateur DMO Set \_ TYPEF \_ test \_ only.</span><span class="sxs-lookup"><span data-stu-id="96750-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="96750-136">La méthode retourne S \_ OK si le type est acceptable, ou a la \_ valeur false dans le cas contraire :</span><span class="sxs-lookup"><span data-stu-id="96750-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="96750-137">Étant donné que les paramètres d’un flux peuvent affecter un autre flux, vous devrez peut-être effacer le type de média d’un flux.</span><span class="sxs-lookup"><span data-stu-id="96750-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="96750-138">Pour ce faire, appelez **SetInputType** ou **SetOutputType** avec l' \_ indicateur Set \_ TYPEF \_ Clear de DMO.</span><span class="sxs-lookup"><span data-stu-id="96750-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="96750-139">Pour un décodeur DMO, le client définit en premier le type d’entrée, puis choisit un type de sortie.</span><span class="sxs-lookup"><span data-stu-id="96750-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="96750-140">Pour un encodeur DMO, le client définit d’abord le type de sortie, puis le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="96750-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96750-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96750-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96750-142">Hébergement direct d’un DMO</span><span class="sxs-lookup"><span data-stu-id="96750-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



