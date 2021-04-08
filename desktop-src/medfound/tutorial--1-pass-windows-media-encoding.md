---
description: L’encodage fait référence au processus de conversion de médias numériques d’un format dans un autre. Par exemple, la conversion de son MP3 au format Windows Media Audio comme défini par la spécification ASF (Advanced Systems Format).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Didacticiel : 1-passer l’encodage Windows Media'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761461"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>Didacticiel : 1-passer l’encodage Windows Media

L’encodage fait référence au processus de conversion de médias numériques d’un format dans un autre. Par exemple, la conversion de son MP3 au format Windows Media Audio comme défini par la spécification ASF (Advanced Systems Format).

**Remarque**  La spécification ASF définit un type de conteneur pour le fichier de sortie (. WMA ou. wmv) qui peut contenir des données multimédias dans n’importe quel format, compressé ou non compressé. Par exemple, un conteneur ASF comme un fichier. WMA peut contenir des données multimédias au format MP3. Le processus d’encodage convertit le format réel des données contenues dans le fichier.

Ce didacticiel montre l’encodage d’une source d’entrée de contenu clair (non protégée par DRM) dans le contenu Windows Media et l’écriture de données dans un nouveau fichier ASF (. WM \* ) à l’aide de composants ASF de couche de pipeline. Ces composants seront utilisés pour générer une topologie d’encodage partielle, qui sera contrôlée par une instance de la session multimédia.

Dans ce didacticiel, vous allez créer une application console qui prend les noms de fichiers d’entrée et de sortie, et le mode d’encodage comme arguments. Le fichier d’entrée peut être dans un format compressé ou non compressé. Les modes d’encodage valides sont « CBR » (vitesse binaire constante) ou « VBR » (vitesse de transmission variable). L’application crée une source de média pour représenter la source spécifiée par le nom de fichier d’entrée, et le récepteur de fichiers ASF pour archiver le contenu encodé du fichier source dans un fichier ASF. Pour simplifier l’implémentation du scénario, le fichier de sortie n’aura qu’un seul flux audio et un seul flux vidéo. L’application insère le codec Windows Media Audio 9,1 Professional pour la conversion de format de flux audio et le codec Windows Media Video 9 pour le flux vidéo.

Pour un encodage à taux binaire constant, avant le début de la session d’encodage, l’encodeur doit connaître la vitesse de transmission cible qu’il doit atteindre. Dans ce didacticiel, pour le mode « CBR », l’application utilise la vitesse de transmission disponible avec le premier type de média de sortie récupéré à partir de l’encodeur pendant la négociation de type de média comme vitesse de transmission cible. Pour l’encodage à taux binaire variable, ce didacticiel montre l’encodage avec une vitesse de transmission variable en définissant un niveau de qualité. Les flux audio sont encodés au niveau de qualité 98 et les flux vidéo au niveau de qualité 95.

La procédure suivante résume les étapes d’encodage du contenu Windows Media dans un conteneur ASF à l’aide d’un mode d’encodage à passage.

1.  Créer une source de média pour le spécifié à l’aide du programme de résolution source.
2.  Énumérer les flux dans la source du média.
3.  Créez le récepteur de média ASF et ajoutez des récepteurs de flux en fonction des flux de la source du média qui doivent être encodés.
4.  Configurez le récepteur multimédia avec les propriétés d’encodage requises.
5.  Créez les encodeurs Windows Media pour les flux dans le fichier de sortie.
6.  Configurez les encodeurs avec les propriétés définies sur le récepteur multimédia.
7.  Générez une topologie d’encodage partielle.
8.  Instanciez la session multimédia et définissez la topologie sur la session multimédia.
9.  Démarrez la session d’encodage en contrôlant la session multimédia et en obtenant tous les événements pertinents à partir de la session multimédia.
10. Pour l’encodage VBR, récupérez les valeurs de propriété d’encodage de l’encodeur et définissez-les sur le récepteur multimédia.
11. Fermez et arrêtez la session d’encodage.

Ce didacticiel contient les sections suivantes :

-   [Conditions préalables](#prerequisites)
-   [Configurer le projet](#set-up-the-project)
-   [Créer la source du média](#create-the-media-source)
-   [Créer le récepteur de fichiers ASF](#create-the-asf-file-sink)
    -   [Créer l’objet de profil ASF](#create-the-asf-profile-object)
    -   [Créer un type de média audio compressé](#create-a-compressed-audio-media-type)
    -   [Créer un type de média vidéo compressé](#create-a-compressed-video-media-type)
    -   [Créer l’objet ASF ContentInfo](#create-the-asf-contentinfo-object)
    -   [Créer le récepteur de fichiers ASF](#create-the-asf-file-sink)
-   [Créer la topologie d’encodage partiel](#build-the-partial-encoding-topology)
    -   [Créer le nœud de topologie source pour la source du média](#create-the-source-topology-node-for-the-media-source)
    -   [Instancier les encodeurs requis et créer les nœuds de transformation](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [Créer les nœuds de topologie de sortie pour le récepteur de fichiers](#create-the-output-topology-nodes-for-the-file-sink)
    -   [Connecter les nœuds source, de transformation et récepteur](#connect-the-source-transform-and-sink-nodes)
-   [Gestion de la session d’encodage](#handling-the-encoding-session)
-   [Mettre à jour les propriétés d’encodage dans le récepteur de fichiers](#update-encoding-properties-in-the-file-sink)
-   [Implémenter main](#implement-main)
-   [Tester le fichier de sortie](#test-the-output-file)
-   [Codes d’erreur courants et conseils de débogage](#common-error-codes-and-debugging-tips)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Ce didacticiel part des principes suivants :

-   Vous êtes familiarisé avec la [structure de fichiers ASF](asf-file-structure.md), les [composants ASF de couche de pipeline](pipeline-layer-asf-components.md) fournis par Media Foundation pour travailler avec des objets ASF. Ces composants incluent les objets suivants :
    -   [Sources multimédias](media-sources.md)

        **Remarque**  Si vous effectuez une conversion (en convertissant un fichier de taux binaire plus élevé en un fichier de vitesse de transmission inférieur sans modifier les formats), vous utiliserez la [source du média ASF](asf-media-source.md).

    -   [Encodeurs Windows Media](windows-media-encoders.md)
    -   [Récepteurs de média ASF](asf-media-sinks.md)
    -   [Objet ASF ContentInfo](asf-contentinfo-object.md)
    -   [Profil ASF](asf-profile.md)

-   Vous êtes familiarisé avec les encodeurs Windows Media et les différents types d’encodage, notamment le [codage à vitesse de transmission constant](constant-bit-rate-encoding.md) et l' [encodage à vitesse de transmission variable basé sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md).
-   Vous êtes familiarisé avec les opérations de l’encodeur MFT. En particulier, la création d’une instance de l’encodeur et la définition des types d’entrée et de sortie sur l’encodeur.
-   Vous êtes familiarisé avec les objets de topologie et comment créer une topologie d’encodage. Pour plus d’informations sur les topologies et les nœuds de topologie, consultez [création de topologies](creating-topologies.md).
-   Vous êtes familiarisé avec le modèle d’événement de la [session de média](media-session.md)et les opérations de contrôle de Workflow. Pour plus d’informations, consultez [événements de session multimédia](media-session-events.md).

## <a name="set-up-the-project"></a>Configurer le projet

1.  Incluez les en-têtes suivants dans votre fichier source :

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  Lien vers les fichiers de bibliothèque suivants :

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  Déclarez la fonction [SafeRelease](saferelease.md) .

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  Déclarez l' \_ énumération du mode d’encodage pour définir les types d’encodage CBR et VBR.

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  Définissez une constante pour la fenêtre de mémoire tampon d’un flux vidéo.

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>Créer la source du média

Créez une source de média pour la source d’entrée. Media Foundation fournit des sources multimédias intégrées pour différents formats de média : MP3, MP4/3GP, AVI/WAVE. Pour plus d’informations sur les formats pris en charge par Media Foundation, consultez [formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md).

Pour créer la source du média, utilisez le programme de [résolution source](source-resolver.md). Cet objet analyse l’URL qui a été spécifiée pour le fichier source et crée la source de média appropriée.

Effectuez les appels suivants :

-   [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    Pour plus d’informations sur ces appels, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).

    Si votre fichier d’entrée est au format ASF et que vous souhaitez le convertir en un fichier de vitesse de transmission différent sans modifier les formats, le solveur source crée une instance de la [source du média ASF](asf-media-source.md).

L’exemple de code suivant montre une fonction CreateMediaSource qui crée une source de média pour le fichier spécifié.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>Créer le récepteur de fichiers ASF

Créez une instance du récepteur de fichiers ASF qui archivera les données multimédias encodées dans un fichier ASF à la fin de la session d’encodage.

Dans ce didacticiel, vous allez créer un objet d’activation pour le récepteur de fichiers ASF. Le récepteur de fichiers a besoin des informations suivantes pour créer les récepteurs de flux requis.

-   Flux à encoder et à écrire dans le fichier final.
-   Les propriétés d’encodage utilisées pour encoder le contenu multimédia, telles que, le type d’encodage, le nombre de passes d’encodage et les propriétés associées.
-   Propriétés de fichier globales qui indiquent au récepteur multimédia s’il doit ajuster automatiquement les paramètres de compartiment perdu (vitesse de transmission et taille de mémoire tampon).

Les informations de flux de données sont configurées dans l’objet de profil ASF et les propriétés d’encodage et globales sont définies dans une banque de propriétés gérée par l’objet ASF ContentInfo.

Pour obtenir une vue d’ensemble du récepteur de fichiers ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).

### <a name="create-the-asf-profile-object"></a>Créer l’objet de profil ASF

Pour que le récepteur de fichiers ASF écrive les données multimédias encodées dans un fichier ASF, le récepteur doit connaître le nombre de flux et le type de flux pour lesquels créer des récepteurs de flux. Dans ce didacticiel, vous allez extraire ces informations de la source du média et créer les flux de sortie correspondants. Limitez vos flux de sortie à un flux audio et à un flux vidéo. Pour chaque flux sélectionné dans la source, créez un flux cible et ajoutez-le au profil.

Pour implémenter cette étape, vous avez besoin des objets suivants.

-   [Profil ASF](asf-profile.md)
-   Descripteur de présentation pour la source du média
-   Descripteurs de flux pour les flux sélectionnés dans la source du média.
-   Types de médias pour les flux sélectionnés.

Les étapes suivantes décrivent le processus de création du profil ASF et des flux cibles.

**Pour créer le profil ASF**

1.  Appelez [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) pour créer un objet de profil vide.
2.  Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) pour créer le descripteur de présentation pour la source de média créée à l’étape décrite dans la section « créer la source du média » de ce didacticiel.
3.  Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) pour connaître le nombre de flux dans la source du média.
4.  Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour chaque flux dans la source du média, puis récupérez le descripteur de flux du flux.
5.  Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) suivi de [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) et récupérez le premier type de média pour le flux.

    **Remarque**   Pour éviter les appels complexes, supposez qu’il n’existe qu’un seul type de média par flux et sélectionnez le premier type de média du flux. Pour les flux complexes, vous devez énumérer chaque type de média à partir du gestionnaire de type de média et choisir le type de média que vous souhaitez Encoder.

6.  Appelez I [**IMFMediaType :: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) pour obtenir le type principal du flux afin de déterminer si le flux contient des données audio ou vidéo.
7.  En fonction du type principal du flux, créez des types de médias cibles. Ces types de médias contiendront les informations de format que l’encodeur utilisera pendant la session d’encodage. Les sections suivantes de ce didacticiel décrivent le processus de création des types de média cible.
    -   Créer un type de média audio compressé
    -   Créer un type de média vidéo compressé
8.  Créez un flux basé sur le type de média cible, configurez le flux en fonction des exigences de l’application et ajoutez le flux au profil. Pour plus d’informations, consultez [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md).

    1.  Appelez [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) et transmettez le type de média cible pour créer le flux de sortie. La méthode récupère l’interface IMFASFStreamConfig de l’objet de flux.
    2.  Configurez le flux.
        -   Appelez [**IMFASFStreamConfig :: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) pour assigner un nombre au flux. Ce paramètre est obligatoire.
        -   Éventuellement, configurez les paramètres de compartiment avec fuite, l’extension de charge utile et l’exclusion mutuelle sur chaque flux en appelant les méthodes [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) et les attributs de configuration de flux pertinents.
    3.  Ajoutez les propriétés d’encodage de niveau de flux à l’aide de l’objet ASF ContentInfo. Pour plus d’informations sur cette étape, consultez la section « créer l’objet ASF ContentInfo » dans ce didacticiel.
    4.  Appelez [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) pour ajouter le flux au profil.

    L’exemple de code suivant crée un flux audio de sortie.

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    L’exemple de code suivant crée un flux vidéo de sortie.

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

L’exemple de code suivant crée des flux de sortie en fonction des flux dans la source.


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>Créer un type de média audio compressé

Si vous souhaitez inclure un flux audio dans le fichier de sortie, créez un type audio en spécifiant les caractéristiques du type encodé en définissant les attributs requis. Pour vous assurer que le type audio est compatible avec l’encodeur audio Windows Media, instanciez la MFT de l’encodeur, définissez les propriétés d’encodage et récupérez un type de média en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Obtenez le type de sortie requis en parcourant tous les types disponibles, en obtenant les attributs de chaque type de média et en sélectionnant le type le plus proche de vos spécifications. Dans ce didacticiel, récupérez le premier type disponible dans la liste des types de médias de sortie pris en charge par l’encodeur.

**Remarque**  Pour Windows 7, Media Foundation fournit une nouvelle fonction, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , qui récupère la liste des types audio compatibles. Cette fonction obtient uniquement les types de médias pour l’encodage CBR.

Un type audio complet doit avoir les attributs suivants définis :

-   [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)
-   [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)
-   [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)
-   [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)
-   [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)

L’exemple de code suivant crée un type audio compressé en obtenant un type compatible à partir de l’encodeur Windows Media Audio. L’implémentation de SetEncodingProperties est présentée dans la section « créer l’objet ASF ContentInfo » de ce didacticiel.


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>Créer un type de média vidéo compressé

Si vous souhaitez inclure un flux vidéo dans le fichier de sortie, créez un type de vidéo encodé de façon complète. Le type de support complet doit inclure la vitesse de transmission souhaitée et les données privées du codec.

Il existe deux façons de créer un type de média vidéo complet.

-   Créez un type de média vide et copiez les attributs de type de média à partir du type de vidéo source et remplacez l’attribut de sous- [**\_ \_ type MF MT**](mf-mt-subtype-attribute.md) par la constante GUID MFVideoFormat \_ WMV3.

    Un type de vidéo complet doit avoir les attributs suivants définis :

    -   \_type de \_ majeurese MF MT \_
    -   \_sous- \_ type MF MT
    -   \_fréquence d' \_ images MF MF \_
    -   \_taille de \_ trame MF MF \_
    -   \_ \_ mode entrelacé MF-MT \_
    -   \_ \_ \_ rapport hauteur/largeur des pixels \_ MF
    -   \_vitesse de \_ \_ transmission moy. MF
    -   \_ \_ données utilisateur MF \_ MT

    L’exemple de code suivant crée un type de vidéo compressé à partir du type de vidéo de la source.

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   Procurez-vous un type de média compatible à partir de l’encodeur vidéo Windows Media en définissant les propriétés d’encodage, puis en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Cette méthode retourne le type partiel. Veillez à convertir le type partiel en un type complet en ajoutant les informations suivantes :

    -   Définissez la vitesse de transmission vidéo dans l’attribut vitesse de [**\_ \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) .
    -   Ajoutez des données privées de codec en définissant l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) . Pour obtenir des instructions détaillées, consultez « données de codec privées » dans [configuration d’un encodeur WMV](configuring-a-wmv-encoder.md).

    Comme [**IWMCodecPrivateData :: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) vérifie la vitesse de transmission avant de retourner les données privées du codec, veillez à définir la vitesse de transmission avant d’obtenir les données privées du codec.

    L’exemple de code suivant crée un type de vidéo compressé en obtenant un type compatible à partir de l’encodeur Windows Media Video. Il crée également un type de vidéo non compressé et le définit comme entrée de l’encodeur. Elle est implémentée dans la fonction d’assistance CreateUncompressedVideoType. GetOutputTypeFromWMVEncoder convertit le type partiel retourné en un type complet en ajoutant des données privées de codec. L’implémentation de SetEncodingProperties est présentée dans la section « créer l’objet ASF ContentInfo » de ce didacticiel.

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    L’exemple de code suivant crée un type de vidéo non compressé.

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    L’exemple de code suivant ajoute des données privées de codec au type de média vidéo spécifié.

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>Créer l’objet ASF ContentInfo

L’objet ASF ContentInfo est un composant de niveau WMContainer conçu principalement pour stocker les informations relatives aux objets d’en-tête ASF. Le récepteur de fichiers ASF implémente l’objet ContentInfo afin de stocker les informations (dans une banque de propriétés) qui seront utilisées pour écrire l’objet d’en-tête ASF du fichier encodé. Pour ce faire, vous devez créer et configurer l’ensemble d’informations suivant sur l’objet ContentInfo avant de démarrer la session d’encodage.

1.  Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo vide.

    L’exemple de code suivant crée un objet ContentInfo vide.

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  Appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) pour récupérer la Banque de propriétés au niveau du flux du récepteur de fichiers. Dans cet appel, vous devez transmettre le numéro de flux que vous avez affecté au flux lors de la création du profil ASF.
3.  Définissez les [propriétés d’encodage](configuring-the-encoder.md) au niveau du flux dans la Banque de propriétés de flux du récepteur de fichiers. Pour plus d’informations, consultez « Propriétés d’encodage de flux » dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).

    L’exemple de code suivant définit les propriétés de niveau de flux dans la Banque de propriétés du récepteur de fichiers.

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    L’exemple de code suivant montre l’implémentation de SetEncodingProperties. Cette fonction définit les propriétés d’encodage de niveau flux pour CBR et VBR.

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  Appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) pour récupérer la Banque de propriétés globale du récepteur de fichiers. Dans cet appel, vous devez passer 0 dans le premier paramètre. Pour plus d’informations, consultez « Propriétés globales du récepteur de fichiers » dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).
5.  Définissez la valeur de la variable [**MFPKEY ASFMEDIASINK de la \_ vitesse de \_ \_ transmission**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) par variante pour \_ que les valeurs de compartiment avec fuite dans le multiplexeur ASF soient correctement ajustées. Pour plus d’informations sur cette propriété, consultez « initialisation du multiplexeur et paramètres des compartiments de fuites » dans [création de l’objet multiplexeur](creating-the-multiplexer-object.md).

    L’exemple de code suivant définit les propriétés de niveau de flux dans la Banque de propriétés du récepteur de fichiers.

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > D’autres propriétés peuvent être définies au niveau global pour le récepteur de fichiers. Pour plus d’informations, consultez « Configuration de l’objet ContentInfo avec les paramètres de l’encodeur » dans [définition des propriétés dans l’objet ContentInfo](setting-properties-in-the-contentinfo-object.md).

     

Vous allez utiliser le fichier ASF ContentInfo configuré pour créer un objet d’activation pour le récepteur de fichiers ASF (décrit dans la section suivante).

Si vous créez un récepteur de fichiers out-of-process ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), c’est-à-dire en utilisant un objet d’activation, vous pouvez utiliser l’objet ContentInfo configuré pour instancier le récepteur multimédia ASF (décrit dans la section suivante). Si vous créez un récepteur de fichiers in-process ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), au lieu de créer l’objet ContentInfo vide comme décrit à l’étape 1, vous pouvez obtenir une référence à l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) en appelant **IMFMediaSink :: QueryInterface** sur le récepteur de fichiers. Vous devez ensuite configurer l’objet ContentInfo comme décrit dans cette section.

### <a name="create-the-asf-file-sink"></a>Créer le récepteur de fichiers ASF

Dans cette étape du didacticiel, vous allez utiliser le fichier ASF ContentInfo, que vous avez créé à l’étape précédente, pour créer un objet d’activation pour le récepteur de fichiers ASF en appelant la fonction [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) . Pour plus d’informations, consultez [création du récepteur de fichiers ASF](creating-the-asf-file-sink.md).

L’exemple de code suivant crée l’objet d’activation pour le récepteur de fichiers.


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>Créer la topologie d’encodage partiel

Ensuite, vous allez créer une topologie d’encodage partielle en créant des nœuds de topologie pour la source du média, les encodeurs Windows Media requis et le récepteur de fichiers ASF. Après avoir ajouté les nœuds de topologie, vous allez connecter les nœuds source, transformation et récepteur. Avant d’ajouter des nœuds de topologie, vous devez créer un objet de topologie vide en appelant [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).

### <a name="create-the-source-topology-node-for-the-media-source"></a>Créer le nœud de topologie source pour la source du média

Dans cette étape, vous allez créer le nœud de topologie source pour la source du média.

Pour créer ce nœud, vous avez besoin des références suivantes :

-   Pointeur vers la source du média que vous avez créée à l’étape décrite dans la section « créer la source du média » de ce didacticiel.
-   Pointeur vers le descripteur de présentation pour la source du média. Vous pouvez obtenir une référence à l’interface IMFPresentationDescriptor de la source du média en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Pointeur vers le descripteur de flux pour chaque flux dans la source du média pour laquelle vous avez créé un flux cible à l’étape décrite dans la section « créer l’objet profil ASF » de ce didacticiel.

Pour plus d’informations sur la création de nœuds sources et d’exemples de code, consultez [création de nœuds sources](creating-source-nodes.md).

L’exemple de code suivant crée une topologie partielle en ajoutant le nœud source et les nœuds de transformation requis. Ce code appelle les fonctions d’assistance AddSourceNode et AddTransformOutputNodes. Ces fonctions sont incluses plus loin dans ce didacticiel.


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



L’exemple de code suivant crée et ajoute le nœud de topologie source à la topologie d’encodage. Elle prend des pointeurs vers un objet de topologie précédemment, la source du média pour énumérer les flux sources, le descripteur de présentation de la source du média et le descripteur de flux de la source du média. L’appelant reçoit un pointeur vers le nœud de topologie source.


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>Instancier les encodeurs requis et créer les nœuds de transformation

Le pipeline Media Foundation n’insère pas automatiquement les encodeurs Windows Media requis pour les flux qu’il doit Encoder. L’application doit ajouter les encodeurs manuellement. Pour ce faire, énumérez les flux dans le profil ASF que vous avez créé à l’étape décrite dans la section « créer l’objet profil ASF » de ce didacticiel. Pour chaque flux dans la source et le flux correspondant dans le profil, instanciez les encodeurs requis. Pour cette étape, vous avez besoin d’un pointeur vers l’objet d’activation pour le récepteur de fichiers que vous avez créé à l’étape décrite dans la section « créer le récepteur de fichiers ASF » de ce didacticiel.

Pour obtenir une vue d’ensemble de la création d’encodeurs par le biais d’objets d’activation, consultez [utilisation des objets d’activation d’un](using-an-encoder-s-activation-objects.md)encodeur.

La procédure suivante décrit les étapes requises pour instancier les encodeurs requis.

1.  Pour obtenir une référence à l’objet ContentInfo du récepteur, appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sur le récepteur de fichiers Activate, puis interrogez [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) à partir du récepteur de fichiers en appelant **QueryInterface**.
2.  Récupérez le profil ASF associé à l’objet ContentInfo en appelant [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).
3.  Énumérer les flux dans le profil. Pour cela, vous avez besoin du nombre de flux et d’une référence à l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) de chaque flux.

    Appelez les méthodes suivantes :

    -   [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  Pour chaque flux, récupérez le type principal et les propriétés d’encodage du flux à partir de l’objet ContentInfo.

    Appelez les méthodes suivantes :

    -   [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        Pour cet appel, vous avez besoin du numéro de flux récupéré par l’appel de [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .

5.  Selon le type de flux, audio ou vidéo, instanciez l’objet d’activation pour l’encodeur en appelant [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).

    Pour appeler ces fonctions, vous avez besoin des références suivantes :

    -   Pointeur vers le type de média du flux récupéré par [**IMFASFStreamConfig :: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) à l’étape précédente.
    -   Pointeur vers le magasin de propriétés d’encodage du flux récupéré par [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). En passant un pointeur vers la Banque de propriétés, les propriétés de flux définies dans le récepteur de fichiers sont copiées sur la table MFT de l’encodeur.

6.  Mettez à jour le paramètre de compartiment avec fuite pour le flux audio.

    [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) définit le type de sortie sur la MFT de l’encodeur sous-jacent pour le codec audio Windows Media. Une fois que le type de média de sortie est défini, l’encodeur obtient la vitesse de transmission moyenne à partir du type de média de sortie, calcule la vitesse de transmission de la fenêtre de mémoire tampon et définit les valeurs de compartiment avec fuite qui seront utilisées pendant la session d’encodage. Vous pouvez mettre à jour ces valeurs dans le récepteur de fichiers en interrogeant l’encodeur ou en définissant des valeurs personnalisées. Pour mettre à jour les valeurs, vous avez besoin de l’ensemble d’informations suivant :

    -   Vitesse de transmission moyenne : obtient la vitesse de transmission moyenne de l’attribut nombre moyen d' [**\_ \_ \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) de l’ensemble des octets audio MF
    -   Fenêtre de mémoire tampon : vous pouvez la récupérer en appelant [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).
    -   Taille de la mémoire tampon initiale : définie sur 0.

    Créez un tableau de valeurs DWORD et définissez la valeur dans la [**propriété \_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigée \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) du récepteur de flux audio. Si vous ne fournissez pas les valeurs mises à jour, la session multimédia les définit de manière appropriée.

    Pour plus d’informations, consultez [le modèle de mémoire tampon de compartiment](the-leaky-bucket-buffer-model.md)perdu.

Les objets d’activation créés à l’étape 5 doivent être ajoutés à la topologie comme des nœuds de topologie de transformation. Pour plus d’informations et pour obtenir un exemple de code, consultez « Création d’un nœud de transformation à partir d’un objet d’activation » dans [création de nœuds de transformation](creating-transform-nodes.md).

L’exemple de code suivant crée et ajoute l’activation de l’encodeur requis. Elle prend des pointeurs vers un objet de topologie précédemment créé, l’objet d’activation du récepteur de fichiers et le type de média du flux source. Il appelle également AddOutputNode (Voir l’exemple de code suivant) qui crée et ajoute le nœud récepteur à la topologie d’encodage. L’appelant reçoit un pointeur vers le nœud de topologie source.


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>Créer les nœuds de topologie de sortie pour le récepteur de fichiers

Au cours de cette étape, vous allez créer le nœud de topologie de sortie pour le récepteur de fichiers ASF.

Pour créer ce nœud, vous avez besoin des références suivantes :

-   Pointeur vers l’objet d’activation que vous avez créé à l’étape décrite dans la section « créer le récepteur de fichiers ASF » de ce didacticiel.
-   Les numéros de flux pour identifier les récepteurs de flux ajoutés au récepteur de fichiers. Les numéros de flux correspondent à l’identification du flux qui a été définie lors de la création du flux.

Pour plus d’informations sur la création de nœuds de sortie et d’exemple de code, consultez « Création d’un nœud de sortie à partir d’un objet d’activation » dans [création de nœuds de sortie](creating-output-nodes.md).

Si vous n’utilisez pas l’objet d’activation pour le récepteur de fichiers, vous devez énumérer les récepteurs de flux dans le récepteur de fichiers ASF et définir chaque récepteur de flux en tant que nœud de sortie dans la topologie. Pour plus d’informations sur l’énumération du récepteur de flux, consultez « énumération des récepteurs de flux » dans [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md).

L’exemple de code suivant crée et ajoute le nœud récepteur à la topologie d’encodage. Elle prend des pointeurs vers un objet de topologie précédemment créé, l’objet d’activation du récepteur de fichiers et le numéro d’identification du flux. L’appelant reçoit un pointeur vers le nœud de topologie source.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



L’exemple de code suivant énumère les récepteurs de flux pour un récepteur multimédia donné.


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>Connecter les nœuds source, de transformation et récepteur

Au cours de cette étape, vous allez connecter le nœud source au nœud de transformation qui référence l’activation de l’encodage que vous avez créée à l’étape décrite dans la section « instancier les encodeurs requis et créer les nœuds de transformation » de ce didacticiel. Le nœud de transformation sera connecté au nœud de sortie contenant l’objet d’activation pour le récepteur de fichiers.

## <a name="handling-the-encoding-session"></a>Gestion de la session d’encodage

À l’étape, vous allez effectuer les étapes suivantes :

1.  Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer une session d’encodage.
2.  Appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie d’encodage sur la session. Si l’appel se termine, la session de média évalue les nœuds de topologie et insère des objets de transformation supplémentaires tels qu’un décodeur qui convertit la source compressée spécifiée en échantillons non compressés en un flux en tant qu’entrée dans l’encodeur.
3.  Appelez [**IMFMediaSession :: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) pour demander les événements déclenchés par la session multimédia.

    Dans la boucle d’événements, vous allez démarrer et fermer la session d’encodage en fonction des événements déclenchés par la session multimédia. L’appel de [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) produit une session multimédia déclenchant l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec \_ l' \_ indicateur prêt TOPOSTATUS Ready défini. Tous les événements sont générés de manière asynchrone et une application peut récupérer ces événements de façon synchrone ou asynchrone. Étant donné que l’application de ce didacticiel est une application console et que le blocage des threads d’interface utilisateur n’est pas un problème, nous obtenons les événements de la session de média de façon synchrone.

    Pour récupérer les événements de façon asynchrone, votre application doit implémenter l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Pour plus d’informations et pour obtenir un exemple d’implémentation de cette interface, consultez « Gestion des événements de session » dans [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).

Dans la boucle d’événements pour l’obtention d’événements de session multimédia, attendez l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) déclenché lorsque [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se termine et que la topologie est résolue. Lors de l’obtention de l’événement MESessionTopologyStatus, démarrez la session d’encodage en appelant [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). La session multimédia génère l’événement [MEEndOfPresentation](meendofpresentation.md) lorsque toutes les opérations d’encodage sont terminées. Cet événement doit être géré pour l’encodage VBR et est abordé dans la section suivante « mettre à jour les propriétés d’encodage sur le récepteur de fichiers pour l’encodage VBR » de ce didacticiel.

La session multimédia génère l’objet d’en-tête ASF et finalise le fichier lorsque la session d’encodage est terminée, puis déclenche l’événement [MESessionClosed](mesessionclosed.md) . Cet événement doit être géré en effectuant des opérations d’arrêt appropriées sur la session multimédia. Pour commencer les opérations d’arrêt, appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Une fois la session d’encodage fermée, vous ne pouvez pas définir une autre topologie pour l’encodage sur la même instance de session de support. Pour encoder un autre fichier, la session de média en cours doit être fermée et libérée et la nouvelle topologie doit être définie sur une session multimédia nouvellement créée. L’exemple de code suivant crée la session multimédia, définit la topologie d’encodage et gère les événements de session multimédia.

L’exemple de code suivant crée la session multimédia, définit la topologie d’encodage et contrôle la session d’encodage en gérant les événements de la session multimédia.


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
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

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>Mettre à jour les propriétés d’encodage dans le récepteur de fichiers

Certaines propriétés d’encodage, telles que la vitesse de transmission d’encodage et les valeurs de compartiment de fuite exacte, ne sont pas connues tant que l’encodage n’est pas terminé, en particulier pour l’encodage VBR. Pour obtenir les valeurs correctes, l’application doit attendre l’événement [MEEndOfPresentation](meendofpresentation.md) qui indique que la session d’encodage est terminée. Les valeurs de compartiment avec fuite doivent être mises à jour dans le récepteur afin que l’objet d’en-tête ASF puisse refléter les valeurs précises.

La procédure suivante décrit les étapes requises pour parcourir les nœuds de la topologie d’encodage afin d’extraire le nœud récepteur de fichiers et de définir les propriétés de compartiment perdues requises.

**Pour mettre à jour les valeurs des propriétés de publication de l’encodage sur le récepteur de fichiers ASF**

1.  Appelez [**IMFTopology :: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) pour récupérer la collection de nœuds de sortie à partir de la topologie d’encodage.
2.  Pour chaque nœud, vous pouvez obtenir un pointeur vers le récepteur de flux dans le nœud en appelant [**IMFTopologyNode :: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject). Recherchez l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) sur le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retourné par **IMFTopologyNode :: GetObject**.
3.  Pour chaque récepteur de flux, récupérez le nœud en aval (encodeur) en appelant [**IMFTopologyNode :: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).
4.  Interrogez le nœud pour obtenir le pointeur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) à partir du nœud de l’encodeur.
5.  Interrogez l’encodeur pour le pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour obtenir la Banque de propriétés d’encodage à partir de l’encodeur.
6.  Interrogez le récepteur de flux du pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour obtenir la Banque de propriétés du récepteur de flux.
7.  Appelez [**IPropertyStore :: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour récupérer les valeurs de propriété requises à partir de la Banque de propriétés de l’encodeur et les copier dans la Banque de propriétés du récepteur de flux en appelant **IPropertyStore :: SetValue**.

Le tableau suivant indique les valeurs des propriétés de publication de l’encodage qui doivent être définies sur le récepteur de flux pour le flux vidéo.



| Type d’encodage                                                                                  | Nom de la propriété (GetValue)                                                                        | Nom de la propriété (SetValue)                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Encodage à vitesse binaire constante](constant-bit-rate-encoding.md)                                   | MFPKEY \_ BAVG<br/> MFPKEY \_ RAVG<br/>                                                 | MFPKEY \_ Stat \_ BAVG<br/> MFPKEY \_ Stat \_ RAVG<br/>                                                             |
| [Encodage de la vitesse de transmission variable basée sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ BAVG<br/> MFPKEY \_ RAVG<br/> MFPKEY \_ BMAX<br/> MFPKEY \_ Rmax<br/> | MFPKEY \_ Stat \_ BAVG<br/> MFPKEY \_ Stat \_ RAVG<br/> MFPKEY \_ Stat \_ BMAX<br/> MFPKEY \_ Stat \_ Rmax<br/> |



 

L’exemple de code suivant définit les valeurs de propriété postérieures à l’encodage.


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>Implémenter main

L’exemple de code suivant montre la fonction principale de votre application console.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>Tester le fichier de sortie

La liste suivante décrit une liste de vérification pour tester le fichier encodé. Ces valeurs peuvent être vérifiées dans la boîte de dialogue Propriétés du fichier que vous pouvez afficher en cliquant avec le bouton droit sur le fichier encodé et en sélectionnant **Propriétés** dans le menu contextuel.

-   Le chemin d’accès du fichier encodé est exact.
-   La taille du fichier est supérieure à zéro Ko et la durée de lecture correspond à la durée du fichier source.
-   Pour le flux vidéo, vérifiez la largeur et la hauteur du frame, ainsi que la fréquence d’images. Ces valeurs doivent correspondre aux valeurs que vous avez spécifiées dans le profil ASF que vous avez créé à l’étape décrite dans la section « créer l’objet de profil ASF ».
-   Pour le flux audio, la vitesse de transmission doit être proche de la valeur que vous avez spécifiée sur le type de média cible.
-   Ouvrez le fichier dans le lecteur Windows Media et vérifiez la qualité de l’encodage.
-   Ouvrez le fichier ASF dans ASFViewer pour afficher la structure d’un fichier ASF. Cet outil peut être téléchargé à partir de ce [site Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="common-error-codes-and-debugging-tips"></a>Codes d’erreur courants et conseils de débogage

La liste suivante décrit les codes d’erreur courants que votre peut recevoir et les conseils de débogage.

-   L’appel à [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) bloque l’application.

    Assurez-vous que vous avez initialisé la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Cette fonction configure la plateforme asynchrone qui est utilisée par toutes les méthodes qui démarrent des opérations asynchrones, telles que [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), en interne.

-   [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) retourne HRESULT 0X80070002 «le système ne peut pas trouver le fichier spécifié.

    Assurez-vous que le nom du fichier d’entrée spécifié par l’utilisateur dans le premier argument existe.

-   HRESULT 0x80070020 "le processus ne peut pas accéder au fichier, car il est utilisé par un autre processus. "

    Assurez-vous que les fichiers d’entrée et de sortie ne sont pas en cours d’utilisation par une autre ressource du système.

-   Les appels aux méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retournent MF \_ E \_ INVALIDMEDIATYPE.

    Assurez-vous que les conditions suivantes sont remplies :

    -   Le type d’entrée ou le type de sortie que vous avez spécifié est compatible avec les types de médias pris en charge par l’encodeur.
    -   Les types de média que vous avez spécifiés sont terminés. Pour que les types de média soient terminés, consultez les attributs requis dans les sections « créer un type de média audio compressé » et « créer un type de média vidéo compressé » de ce didacticiel.
    -   Assurez-vous que vous avez défini la vitesse de transmission cible sur le type de média partiel auquel vous ajoutez les données privées du codec.

-   La session multimédia renvoie \_ \_ le type D3D non pris en charge MF E \_ \_ dans l’état de l’événement.

    Cette erreur est retournée lorsque le type de média de la source indique un mode entrelacé mixte qui n’est pas pris en charge par Windows Media Video encodeur. Si votre type de média vidéo compressé est défini pour utiliser le mode progressive, le pipeline doit utiliser une transformation de désentrelacement. Étant donné que le pipeline ne parvient pas à trouver une correspondance (indiquée par ce code d’erreur), vous devez insérer manuellement un décodeur (processeur vidéo de transcodage) entre le décodeur et les nœuds de l’encodeur.

-   La session multimédia renvoie E \_ INVALIDARG dans l’état de l’événement.

    Cette erreur est retournée lorsque les attributs de type de média de la source ne sont pas compatibles avec les attributs du type de média de sortie défini sur l’encodeur Windows Media.

-   [**IWMCodecPrivateData :: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) retourne HRESULT 0X80040203 « une erreur de syntaxe s’est produite lors de la tentative d’évaluation d’une chaîne de requête »

    Assurez-vous que le type d’entrée est défini sur la MFT de l’encodeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
