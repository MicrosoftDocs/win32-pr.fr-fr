---
title: Pour énumérer les formats d’entrée
description: Pour énumérer les formats d’entrée
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- ASF (Advanced Systems Format), énumération des formats d’entrée
- ASF (format avancé des systèmes), énumération des formats d’entrée
- profils, énumération des formats d’entrée
- codecs, énumération des formats d’entrée
- ASF (Advanced Systems Format), énumérations de format d’entrée
- ASF (format des systèmes avancés), énumérations de format d’entrée
- profils, énumérations de format d’entrée
- codecs, énumérations de format d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030935"
---
# <a name="to-enumerate-input-formats"></a>Pour énumérer les formats d’entrée

Chacun des codecs Windows Media accepte un ou plusieurs types de média d’entrée pour la compression. Le kit de développement logiciel (SDK) Windows Media format vous permet d’entrer une plus grande variété de formats que ceux pris en charge par les codecs. Le kit de développement logiciel (SDK) effectue cette opération en effectuant des transformations de prétraitement sur les entrées, le cas échéant, comme le redimensionnement des images vidéo ou le rééchantillonnage de l’audio. Dans tous les cas, vous devez vous assurer que les formats d’entrée pour les fichiers que vous écrivez correspondent aux données que vous envoyez au writer. Chaque codec a un format de média d’entrée par défaut qui est défini dans le writer lors du chargement du profil. Vous pouvez examiner le format d’entrée par défaut en appelant [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).

Les codecs vidéo prennent en charge les formats suivants : IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RVB 555 et RVB 8. Les codecs audio prennent en charge le PCM audio.

Pour énumérer les formats d’entrée pris en charge par un codec, procédez comme suit :

1.  Créez un objet Writer et définissez un profil à utiliser. Pour plus d’informations sur la définition des profils dans le writer, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).
2.  Identifiez le nombre d’entrées pour lequel vous souhaitez vérifier les formats. Pour plus d’informations sur l’identification des numéros d’entrée, consultez [pour identifier les entrées par numéro](to-identify-inputs-by-number.md).
3.  Récupérez le nombre total de formats d’entrée pris en charge par l’entrée souhaitée en appelant [**IWMWriter :: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Parcourez tous les formats d’entrée pris en charge, en effectuant les étapes suivantes pour chacun d’entre eux.
    -   Récupérez l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) pour le format d’entrée en appelant [**IWMWriter :: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le format d’entrée. Appelez [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), en passant la **valeur null** pour le paramètre *PTYPE* afin d’obtenir la taille de la structure. Allouez ensuite de la mémoire pour contenir la structure et rappelez **GetMediaType** pour récupérer la structure. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) hérite de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops). vous pouvez donc effectuer les appels à **GetMediaType** à partir de l’instance de **IWMInputMediaProps** Récupérée à l’étape précédente.
    -   Le format décrit dans la structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contient toutes les informations pertinentes sur le format d’entrée. Le format de base du support est identifié par **WM \_ Media \_ type. SubType**. Pour les flux vidéo, le membre **pbFormat** pointe vers une structure [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) allouée dynamiquement qui contient des détails supplémentaires sur le flux, y compris la taille du rectangle. La taille des frames d’entrée n’est pas obligatoire pour correspondre exactement à une taille prise en charge par le codec. Si elles ne correspondent pas, les composants d’exécution du kit de développement logiciel (SDK), dans de nombreux cas, redimensionnent automatiquement les trames vidéo d’entrée pour qu’elles puissent être acceptées par le codec.

L’exemple de code suivant recherche le format d’entrée du sous-type passé comme paramètre. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




