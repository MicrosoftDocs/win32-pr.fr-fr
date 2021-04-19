---
description: Ce didacticiel montre comment utiliser l’API de transcodage pour encoder un fichier Windows Media Audio (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Didacticiel : encodage d’un fichier WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534444"
---
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="a0d32-103">Didacticiel : encodage d’un fichier WMA</span><span class="sxs-lookup"><span data-stu-id="a0d32-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="a0d32-104">Ce didacticiel montre comment utiliser l' [API de transcodage](transcode-api.md) pour encoder un fichier Windows Media audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="a0d32-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="a0d32-105">Ce didacticiel réutilise la majeure partie du code du didacticiel [codage d’un fichier MP4](tutorial--encoding-an-mp4-file-.md). vous devez donc lire ce didacticiel en premier.</span><span class="sxs-lookup"><span data-stu-id="a0d32-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="a0d32-106">Le seul code qui diffère est la fonction `CreateTranscodeProfile` , qui crée le profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="a0d32-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="a0d32-107">Créer le profil de transcodage</span><span class="sxs-lookup"><span data-stu-id="a0d32-107">Create the Transcode Profile</span></span>

<span data-ttu-id="a0d32-108">Un *Profil* de transcodage décrit les paramètres d’encodage et le conteneur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a0d32-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="a0d32-109">Pour WMA, le conteneur de fichiers est un fichier ASF (Advanced Streaming Format).</span><span class="sxs-lookup"><span data-stu-id="a0d32-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="a0d32-110">Le fichier ASF contient un flux audio, qui est encodé à l’aide de l' [**Encodeur Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="a0d32-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="a0d32-111">Pour générer la topologie de transcodage, créez le profil de transcodage et spécifiez les paramètres du flux audio et du conteneur.</span><span class="sxs-lookup"><span data-stu-id="a0d32-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="a0d32-112">Ensuite, créez la topologie en spécifiant la source d’entrée, l’URL de sortie et le profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="a0d32-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="a0d32-113">Pour créer le profil, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="a0d32-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="a0d32-114">Appelez la fonction [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) pour créer un profil de transcodage vide.</span><span class="sxs-lookup"><span data-stu-id="a0d32-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="a0d32-115">Appelez [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) pour obtenir la liste des types de média audio de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="a0d32-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="a0d32-116">Cette fonction retourne un pointeur [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) qui représente une collection de pointeurs [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="a0d32-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="a0d32-117">Choisissez le type de média audio qui correspond à vos exigences de transcodage et copiez les attributs dans un magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a0d32-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="a0d32-118">Pour ce didacticiel, le premier type de média de la liste est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0d32-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="a0d32-119">Appelez [**IMFCollection :: GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) pour sélectionner un type de média audio dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a0d32-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="a0d32-120">Interrogez le type de média pour obtenir un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) du magasin d’attributs du type de média.</span><span class="sxs-lookup"><span data-stu-id="a0d32-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="a0d32-121">Appelez [**IMFAttributes :: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) pour connaître le nombre d’attributs contenus dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="a0d32-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="a0d32-122">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a0d32-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="a0d32-123">Appelez [**IMFAttributes :: CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) pour copier les attributs du type de média vers le nouveau magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a0d32-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="a0d32-124">Appelez [**IMFTranscodeProfile :: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) pour définir les attributs du flux audio.</span><span class="sxs-lookup"><span data-stu-id="a0d32-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="a0d32-125">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs pour les attributs de niveau conteneur.</span><span class="sxs-lookup"><span data-stu-id="a0d32-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="a0d32-126">Affectez à l’attribut [ \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) la valeur **MFTranscodeContainerType \_ ASF**, qui spécifie un conteneur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="a0d32-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="a0d32-127">Appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) pour définir les attributs au niveau du conteneur sur le profil.</span><span class="sxs-lookup"><span data-stu-id="a0d32-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
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
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a0d32-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0d32-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d32-129">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="a0d32-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 



