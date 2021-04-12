---
description: Cette rubrique explique comment utiliser le lecteur source pour traiter les données multimédias.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Utilisation du lecteur source pour traiter les données multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321449"
---
# <a name="using-the-source-reader-to-process-media-data"></a>Utilisation du lecteur source pour traiter les données multimédias

Cette rubrique explique comment utiliser le [lecteur source](source-reader.md) pour traiter les données multimédias.

Pour utiliser le lecteur source, suivez les étapes de base suivantes :

1.  Créez une instance du lecteur source.
2.  Énumérer les formats de sortie possibles.
3.  Définissez le format de sortie réel pour chaque flux.
4.  Traiter les données de la source.

Le reste de cette rubrique décrit ces étapes en détail.

-   [Création du lecteur source](#creating-the-source-reader)
-   [Énumération des formats de sortie](#enumerating-output-formats)
-   [Définition des formats de sortie](#setting-output-formats)
-   [Traitement des données multimédias](#using-the-source-reader-to-process-media-data)
-   [Drainage du pipeline de données](#draining-the-data-pipeline)
-   [Obtention de la durée du fichier](#getting-the-file-duration)
-   [Cherche](#seeking)
-   [Vitesse de lecture](#playback-rate)
-   [Accélération matérielle](#hardware-acceleration)
-   [Rubriques connexes](#related-topics)

## <a name="creating-the-source-reader"></a>Création du lecteur source

Pour créer une instance du lecteur source, appelez l’une des fonctions suivantes :



| Fonction                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Prend une URL comme entrée. Cette fonction utilise le programme de [résolution source](source-resolver.md) pour créer une source de média à partir de l’URL.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Prend un pointeur vers un flux d’octets. Cette fonction utilise également le programme de résolution source pour créer la source du média.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Prend un pointeur vers une source multimédia qui a déjà été créée. Cette fonction est utile pour les sources multimédias que le programme de résolution source ne peut pas créer, telles que les périphériques de capture ou les sources de média personnalisées.<br/> |



 

En général, pour les fichiers multimédias, utilisez [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl). Pour les appareils, tels que les webcams, utilisez [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). (Pour plus d’informations sur les appareils de capture dans Microsoft Media Foundation, consultez [capture audio/vidéo](audio-video-capture.md).)

Chacune de ces fonctions prend un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) facultatif, qui est utilisé pour définir différentes options sur le lecteur source, comme décrit dans les rubriques de référence pour ces fonctions. Pour connaître le comportement par défaut, affectez la valeur **null** à ce paramètre. Chaque fonction retourne un pointeur [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) comme paramètre de sortie. Vous devez appeler la fonction **CoInitialize (ex)** et [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) avant d’appeler l’une de ces fonctions.

Le code suivant crée le lecteur source à partir d’une URL.


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a>Énumération des formats de sortie

Chaque source multimédia a au moins un flux. Par exemple, un fichier vidéo peut contenir un flux vidéo et un flux audio. Le format de chaque flux est décrit à l’aide d’un type de média, représenté par l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Pour plus d’informations sur les types de médias, consultez [types de médias](media-types.md). Vous devez examiner le type de média pour comprendre le format des données que vous récupérez à partir du lecteur source.

Initialement, chaque flux a un format par défaut, que vous pouvez trouver en appelant la méthode [**IMFSourceReader :: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :

Pour chaque flux, la source du média offre une liste de types de média possibles pour ce flux. Le nombre de types dépend de la source. Si la source représente un fichier multimédia, il n’y a généralement qu’un seul type par flux. Une webcam, en revanche, peut être en mesure de diffuser des vidéos dans différents formats. Dans ce cas, l’application peut sélectionner le format à utiliser dans la liste des types de médias.

Pour obtenir l’un des types de média pour un flux, appelez la méthode [**IMFSourceReader :: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) . Cette méthode prend deux paramètres d’index : l’index du flux et un index dans la liste des types de média pour le flux. Pour énumérer tous les types d’un flux, incrémentez l’index de la liste tout en conservant la constante d’index de flux. Lorsque l’index de liste est hors limites, **GetNativeMediaType** retourne **MF E plus de \_ \_ \_ \_ types**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



Pour énumérer les types de média pour chaque flux, incrémentez l’index de flux. Lorsque l’index de flux sort des limites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) retourne **MF \_ E \_ INVALIDSTREAMNUMBER**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>Définition des formats de sortie

Pour modifier le format de sortie, appelez la méthode [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) . Cette méthode prend l’index de flux et un type de média :

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

Pour le type de média, cela dépend de l’insertion ou non d’un décodeur.

-   Pour récupérer les données directement à partir de la source sans les décoder, utilisez l’un des types retournés par [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).
-   Pour décoder le flux, créez un nouveau type de média qui décrit le format non compressé souhaité.

Dans le cas du décodeur, créez le type de média comme suit :

1.  Appelez [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) pour créer un type de média.
2.  Définissez l’attribut de [**\_ \_ \_ type principal MF MT**](mf-mt-major-type-attribute.md) pour spécifier audio ou Video.
3.  Définissez l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) pour spécifier le sous-type du format de décodage. (Consultez [GUID de sous-type audio](audio-subtype-guids.md) et [GUID de sous-type de vidéo](video-subtype-guids.md).)
4.  Appelez [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).

Le lecteur source chargera automatiquement le décodeur. Pour obtenir des informations complètes sur le format décodé, appelez [**IMFSourceReader :: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) après l’appel à [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)

Le code suivant configure le flux vidéo pour RGB-32 et le flux audio pour le fichier audio PCM.


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a>Traitement des données multimédias

Pour récupérer les données du média à partir de la source, appelez la méthode [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , comme indiqué dans le code suivant.


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



Le premier paramètre est l’index du flux pour lequel vous souhaitez obtenir des données. Vous pouvez également spécifier **\_ \_ un lecteur source MF \_ n’importe quel \_ flux** pour récupérer les données disponibles suivantes à partir de n’importe quel flux. Le deuxième paramètre contient des indicateurs facultatifs ; pour obtenir une liste de ces, consultez [**\_ indicateur de \_ \_ contrôle \_ du lecteur source MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) . Le troisième paramètre reçoit l’index du flux qui produit réellement les données. Vous aurez besoin de ces informations si vous définissez le premier paramètre sur le **\_ lecteur source MF \_ \_ n’importe quel \_ flux**. Le quatrième paramètre reçoit des indicateurs d’État, indiquant les différents événements qui peuvent se produire lors de la lecture des données, telles que les modifications de format dans le flux. Pour obtenir la liste des indicateurs d’État, consultez [**\_ \_ \_ indicateur de lecteur source MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Si la source du média est en mesure de produire des données pour le flux demandé, le dernier paramètre de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) reçoit un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) d’un objet d’exemple de support. Utilisez l’exemple de support pour :

-   Obtient un pointeur vers les données multimédia.
-   Obtient l’heure de présentation et la durée de l’exemple.
-   Obtient des attributs qui décrivent l’entrelacement, la dominance des champs et d’autres aspects de l’exemple.

Le contenu des données multimédias dépend du format du flux. Pour un flux vidéo non compressé, chaque exemple de support contient une seule image vidéo. Pour un flux audio non compressé, chaque exemple de support contient une séquence de trames audio.

La méthode [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) peut retourner **S \_ OK** et ne pas retourner un exemple de support dans le paramètre *pSample* . Par exemple, lorsque vous atteignez la fin du fichier, **ReadSample** définit l' **indicateur \_ \_ \_ ENDOFSTREAM de READERF source MF** dans *dwFlags* et affecte à *pSample* la **valeur null**. Dans ce cas, la méthode **ReadSample** retourne **S \_ OK** , car aucune erreur n’est survenue, même si le paramètre *pSample* est défini sur **null**. Par conséquent, vérifiez toujours la valeur de *pSample* avant de le déréférencer.

Le code suivant montre comment appeler [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) dans une boucle et vérifier les informations retournées par la méthode, jusqu’à ce que la fin du fichier multimédia soit atteinte.


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a>Drainage du pipeline de données

Pendant le traitement des données, un décodeur ou une autre transformation peut mettre en mémoire tampon des exemples d’entrée. Dans le diagramme suivant, l’application appelle [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) et reçoit un exemple avec une durée de présentation égale à *T1*. Le décodeur contient des exemples pour *T2* et *T3*.

![illustration qui montre la mise en mémoire tampon dans un décodeur.](images/sourcereader02.png)

Lors du prochain appel à [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), le lecteur source peut donner à *T4* le décodeur et retourner *T2* à l’application.

Si vous souhaitez décoder tous les exemples actuellement mis en mémoire tampon dans le décodeur, sans passer de nouveaux exemples au décodeur, définissez l’indicateur de **\_ \_ \_ \_ drainage CONTROLF du lecteur source MF** dans le paramètre *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Continuez à effectuer cette opération dans une boucle jusqu’à ce que **ReadSample** retourne un exemple de pointeur **null** . Selon la façon dont le décodeur met en mémoire tampon les exemples, qui peuvent se produire immédiatement ou après plusieurs appels à **ReadSample**.

## <a name="getting-the-file-duration"></a>Obtention de la durée du fichier

Pour obtenir la durée d’un fichier multimédia, appelez la méthode [**IMFSourceReader :: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) et demandez l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) , comme indiqué dans le code suivant.


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



La fonction illustrée ici obtient la durée en unités de 100 nanosecondes. Divisez par 10 millions pour connaître la durée en secondes.

## <a name="seeking"></a>Cherche

Une source multimédia qui obtient des données à partir d’un fichier local peut généralement Rechercher des positions arbitraires dans le fichier. Les périphériques de capture tels que les webcams ne peuvent généralement pas être recherchés, car les données sont actives. Une source qui diffuse des données sur un réseau peut être en mesure de rechercher, selon le protocole de streaming réseau.

Pour déterminer si une source de média peut effectuer une recherche, appelez [**IMFSourceReader :: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) et demandez l’attribut de [ \_ \_ \_ \_ caractéristiques de lecteur de source MF](mf-source-reader-mediasource-characteristics.md) , comme indiqué dans le code suivant :


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



Cette fonction obtient un jeu d’indicateurs de fonctionnalités à partir de la source. Ces indicateurs sont définis dans l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) . Deux indicateurs sont liés à la recherche :



| Indicateur                                                                                                                                      | Description                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ peut \_ Rechercher**<br/>                 | La source peut effectuer une recherche.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ a \_ une \_ recherche lente**<br/> | La recherche peut prendre beaucoup de temps. Par exemple, la source doit peut-être télécharger l’intégralité du fichier avant de pouvoir effectuer une recherche. (Il n’existe aucun critère strict pour qu’une source retourne cet indicateur.)<br/> |



 

Les tests de code suivants pour le **MFMEDIASOURCE \_ peuvent \_ Rechercher** l’indicateur.


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



Pour effectuer une recherche, appelez la méthode [**IMFSourceReader :: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , comme indiqué dans le code suivant.


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Le premier paramètre indique le format d’heure que vous utilisez pour spécifier la position de recherche. Toutes les sources de média dans Media Foundation sont requises pour prendre en charge des unités de 100 nanosecondes, indiquées par la valeur **GUID \_ null**. Le deuxième paramètre est un **PROPVARIANT** qui contient la position de recherche. Pour les unités de temps de 100 nanosecondes, le type de données est **LongLong**.

N’oubliez pas que chaque source de média ne fournit pas de recherche de trame précise. La précision de la recherche dépend de plusieurs facteurs, tels que l’intervalle d’image clé, le fait que le fichier multimédia contient un index et si les données ont une vitesse de transmission constante ou variable. Par conséquent, une fois que vous avez effectué une recherche sur une position dans un fichier, il n’y a aucune garantie que l’horodatage sur l’échantillon suivant correspond exactement à la position demandée. En règle générale, la position réelle n’est pas postérieure à la position demandée. vous pouvez donc ignorer des échantillons jusqu’à ce que vous atteigniez le point souhaité dans le flux.

## <a name="playback-rate"></a>Vitesse de lecture

Bien que vous puissiez définir la vitesse de lecture à l’aide du lecteur source, cela n’est généralement pas très utile pour les raisons suivantes :

-   Le lecteur source ne prend pas en charge la lecture inversée, même si la source du média le fait.
-   L’application contrôle les durées de présentation, de sorte que l’application peut implémenter une lecture rapide ou lente sans définir la vitesse sur la source.
-   Certaines sources multimédias prennent en charge le mode de réglage de l' *épaisseur* , où la source fournit moins d’échantillons, en général uniquement les images clés. Toutefois, si vous souhaitez supprimer des images non-clés, vous pouvez vérifier chaque exemple pour l’attribut [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) .

Pour définir la vitesse de lecture à l’aide du lecteur source, appelez la méthode [**IMFSourceReader :: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) pour récupérer les interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) et [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) à partir de la source du média.

## <a name="hardware-acceleration"></a>Accélération matérielle

Le lecteur source est compatible avec Microsoft DirectX Video Acceleration (DXVA) 2,0 pour le décodage vidéo à accélération matérielle. Pour utiliser DXVA avec le lecteur source, procédez comme suit.

1.  Créez un appareil Microsoft Direct3D.
2.  Appelez la fonction [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) pour créer le gestionnaire de périphériques Direct3D. Cette fonction obtient un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Appelez la méthode [**IDirect3DDeviceManager9 :: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) avec un pointeur vers le périphérique Direct3D.
4.  Créez un magasin d’attributs en appelant la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
5.  Créez le lecteur source. Transmettez le magasin d’attributs dans le paramètre *pAttributes* de la fonction de création.

Lorsque vous fournissez un appareil Direct3D, le lecteur source alloue des exemples vidéo compatibles avec l’API de processeur vidéo DXVA. Vous pouvez utiliser le traitement vidéo DXVA pour effectuer la désentrelacement du matériel ou le mixage vidéo. Pour plus d’informations, consultez la page [traitement vidéo DXVA](dxva-video-processing.md). En outre, si le décodeur prend en charge la 2,0 DXVA, il utilisera le périphérique Direct3D pour effectuer un décodage accéléré par le matériel.

> [!IMPORTANT]
> À compter de Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) peut être utilisé à la place de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). Pour les applications du Windows Store, vous devez utiliser **IMFDXGIDeviceManager**. Pour plus d’informations, consultez les [API vidéo Direct3D 11](direct3d-11-video-apis.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecteur source](source-reader.md)
</dt> </dl>

 

 




