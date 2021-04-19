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
# <a name="tutorial-encoding-a-wma-file"></a>Didacticiel : encodage d’un fichier WMA

Ce didacticiel montre comment utiliser l' [API de transcodage](transcode-api.md) pour encoder un fichier Windows Media audio (WMA).

Ce didacticiel réutilise la majeure partie du code du didacticiel [codage d’un fichier MP4](tutorial--encoding-an-mp4-file-.md). vous devez donc lire ce didacticiel en premier. Le seul code qui diffère est la fonction `CreateTranscodeProfile` , qui crée le profil de transcodage.

## <a name="create-the-transcode-profile"></a>Créer le profil de transcodage

Un *Profil* de transcodage décrit les paramètres d’encodage et le conteneur de fichiers. Pour WMA, le conteneur de fichiers est un fichier ASF (Advanced Streaming Format). Le fichier ASF contient un flux audio, qui est encodé à l’aide de l' [**Encodeur Windows Media Audio**](windowsmediaaudioencoder.md).

Pour générer la topologie de transcodage, créez le profil de transcodage et spécifiez les paramètres du flux audio et du conteneur. Ensuite, créez la topologie en spécifiant la source d’entrée, l’URL de sortie et le profil de transcodage.

Pour créer le profil, procédez comme suit.

1.  Appelez la fonction [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) pour créer un profil de transcodage vide.
2.  Appelez [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) pour obtenir la liste des types de média audio de l’encodeur. Cette fonction retourne un pointeur [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) qui représente une collection de pointeurs [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .
3.  Choisissez le type de média audio qui correspond à vos exigences de transcodage et copiez les attributs dans un magasin d’attributs. Pour ce didacticiel, le premier type de média de la liste est utilisé.
    -   Appelez [**IMFCollection :: GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) pour sélectionner un type de média audio dans la liste.
    -   Interrogez le type de média pour obtenir un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) du magasin d’attributs du type de média.
    -   Appelez [**IMFAttributes :: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) pour connaître le nombre d’attributs contenus dans le type de média.
    -   Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.
    -   Appelez [**IMFAttributes :: CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) pour copier les attributs du type de média vers le nouveau magasin d’attributs.
4.  Appelez [**IMFTranscodeProfile :: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) pour définir les attributs du flux audio.
5.  Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs pour les attributs de niveau conteneur.
6.  Affectez à l’attribut [ \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) la valeur **MFTranscodeContainerType \_ ASF**, qui spécifie un conteneur de fichiers ASF.
7.  Appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) pour définir les attributs au niveau du conteneur sur le profil.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de transcodage](transcode-api.md)
</dt> </dl>

 

 



