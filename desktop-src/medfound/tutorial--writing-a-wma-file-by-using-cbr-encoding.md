---
description: Ce didacticiel illustre l’écriture d’un nouveau fichier audio (. WMA) en extrayant du contenu multimédia à partir d’un fichier audio non compressé (. wav), puis en le compressant au format ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Didacticiel : écriture d’un fichier WMA à l’aide d’objets WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aed89eb9ef656fe9240a1ed56e712f92209ba5c7e6d5bea2cca3d909d4315ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972768"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Didacticiel : écriture d’un fichier WMA à l’aide d’objets WMContainer

Ce didacticiel illustre l’écriture d’un nouveau fichier audio (. WMA) en extrayant du contenu multimédia à partir d’un fichier audio non compressé (. wav), puis en le compressant au format ASF. Le mode d’encodage utilisé pour la conversion est le CBR ( [constant bit rate encodage](constant-bit-rate-encoding.md) ). Dans ce mode, avant la session d’encodage, l’application spécifie une vitesse de transmission cible que l’encodeur doit atteindre.

Dans ce didacticiel, vous allez créer une application console qui accepte les noms de fichiers d’entrée et de sortie comme arguments. L’application obtient les exemples de supports non compressés à partir d’une application d’analyse de fichiers wave, qui est fournie dans ce didacticiel. ces exemples sont envoyés à l’encodeur pour la conversion au format Windows Media Audio 9. L’encodeur est configuré pour l’encodage CBR et utilise le premier taux de bits disponible pendant la négociation de type de média comme vitesse de transmission cible. Les exemples encodés sont envoyés au multiplexeur pour la transmission de paquets au format de données ASF. Ces paquets sont écrits dans un flux d’octets qui représente l’objet de données ASF. Une fois la section des données prête, vous allez créer un fichier audio ASF et écrire le nouvel objet d’en-tête ASF qui consolide toutes les informations d’en-tête, puis ajouter le flux d’octets de l’objet de données ASF.

Ce didacticiel contient les sections suivantes :

-   [Composants requis](#prerequisites)
-   [Terminologie](#terminology)
-   [1. Configurez le Project](#1-set-up-the-project)
-   [2. déclarer des fonctions d’assistance](#2-declare-helper-functions)
-   [3. ouvrir un fichier audio](#3-open-an-audio-file)
-   [4. configurer l’encodeur](#4-configure-the-encoder)
-   [5. Créez l’objet ASF ContentInfo.](#5-create-the-asf-contentinfo-object)
-   [6. créer le multiplexeur ASF](#6-create-the-asf-multiplexer)
-   [7. générer de nouveaux paquets de données ASF](#7-generate-new-asf-data-packets)
-   [8. écrire le fichier ASF](#8-write-the-asf-file)
-   [9. définir la fonction Entry-Point](#9-define-the-entry-point-function)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Ce didacticiel part des principes suivants :

-   Vous êtes familiarisé avec la structure d’un fichier ASF et les composants fournis par Media Foundation pour travailler avec des objets ASF. Ces composants incluent les objets ContentInfo, Splitter, multiplexer et Profile. Pour plus d’informations, consultez [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   vous êtes familiarisé avec les encodeurs Windows Media et les différents types d’encodage, particulièrement CBR. pour plus d’informations, consultez [Windows des encodeurs multimédias](windows-media-encoders.md) .
-   Vous êtes familiarisé avec les [mémoires tampons de média](media-buffers.md) et les flux d’octets : en particulier, les opérations de fichier utilisant un flux d’octets et l’écriture du contenu d’une mémoire tampon de média dans un flux d’octets.

## <a name="terminology"></a>Terminologie

Ce didacticiel utilise les termes suivants :

-   Type de média source : objet de type de média, expose l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui décrit le contenu du fichier d’entrée.
-   Profil audio : objet de profil, expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , qui contient uniquement les flux audio du fichier de sortie.
-   Exemple de flux : exemple de support, qui expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , représente les données multimédia du fichier d’entrée obtenues à partir de l’encodeur dans un État compressé.
-   Objet ContentInfo : [objet ASF ContentInfo](asf-contentinfo-object.md), qui expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , qui représente l’objet d’en-tête ASF du fichier de sortie.
-   Flux d’octets de données : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui représente la partie entière de l’objet de données ASF du fichier de sortie.
-   Paquet de données : exemple de support, expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , générée par le [multiplexeur ASF](asf-multiplexer.md); représente un paquet de données ASF qui sera écrit dans le flux d’octets de données.
-   Sortie d’octet de sortie : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui contient le contenu du fichier de sortie.

## <a name="1-set-up-the-project"></a>1. Configurez le Project

1.  Incluez les en-têtes suivants dans votre fichier source :

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Lien vers les fichiers de bibliothèque suivants :

    -   mfplat. lib
    -   MF. lib
    -   mfuuid. lib

3.  Déclarez la fonction [SafeRelease](saferelease.md) .
4.  Incluez la classe CWmaEncoder dans votre projet. Pour obtenir le code source complet de cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. déclarer des fonctions d’assistance

Ce didacticiel utilise les fonctions d’assistance suivantes pour lire et écrire à partir d’un flux d’octets.

-   `AppendToByteStream`: Ajoute le contenu d’un flux d’octets à un autre flux d’octets.
-   WriteBufferToByteStream : écrit les données d’une mémoire tampon de média dans un flux d’octets.

Pour plus d’informations, consultez [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). Le code suivant illustre ces fonctions d’assistance :


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a>3. ouvrir un fichier audio

Ce didacticiel part du principe que votre application génère un fichier audio non compressé pour l’encodage. À cet effet, deux fonctions sont déclarées dans ce didacticiel :


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



L’implémentation de ces fonctions est laissée au lecteur.

-   La `OpenAudioFile` fonction doit ouvrir le fichier multimédia spécifié par *pszURL* et retourner un pointeur vers un type de média qui décrit un flux audio.
-   La `GetNextAudioSample` fonction doit lire le fichier audio PCM non compressé à partir du fichier qui a été ouvert par `OpenAudioFile` . Lorsque la fin du fichier est atteinte, *pbEOS* reçoit la valeur **true**. Sinon, *ppSample* reçoit un exemple de support qui contient la mémoire tampon audio.

## <a name="4-configure-the-encoder"></a>4. configurer l’encodeur

Ensuite, créez l’encodeur, configurez-le pour produire des exemples de flux encodés CBR et négociez les types de médias d’entrée et de sortie.

Dans Media Foundation, les encodeurs (exposent l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) sont implémentés en tant que [Media Foundation des transformations](media-foundation-transforms.md) (MFT).

Dans ce didacticiel, l’encodeur est implémenté dans la `CWmaEncoder` classe qui fournit un wrapper pour la table MFT. Pour obtenir le code source complet de cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md).

> [!Note]  
> Vous pouvez éventuellement spécifier le type d’encodage CBR. Par défaut, l’encodeur est configuré pour utiliser l’encodage CBR. Pour plus d’informations, consultez [encodage à taux binaire constant](constant-bit-rate-encoding.md). Vous pouvez définir des propriétés supplémentaires en fonction du type d’encodage, pour obtenir des informations sur les propriétés qui sont spécifiques à un mode d’encodage, consultez encodage à taux binaire [variable basé](quality-based-variable-bit-rate--vbr--encoding.md)sur la qualité, encodage à vitesse de transmission variable non [contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)et [codage à vitesse de transmission variable à contrainte maximale](peak-constrained-variable-bit-rate--vbr--encoding.md).

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a>5. Créez l’objet ASF ContentInfo.

L' [objet ASF ContentInfo](asf-contentinfo-object.md) contient des informations sur les différents objets d’en-tête du fichier de sortie.

Tout d’abord, créez un profil ASF pour le flux audio :

1.  Appelez [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) pour créer un objet de profil ASF vide. Le profil ASF expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . Pour plus d’informations, consultez [création et configuration d’flux ASF](creating-and-configuring-asf-streams.md).
2.  Obtient le format audio encodé à partir de l' `CWmaEncoder` objet.
3.  Appelez [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) pour créer un flux pour le profil ASF. Transmettez un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui représente le format de flux.
4.  Appelez [**IMFASFStreamConfig :: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) pour assigner un identificateur de flux.
5.  Définissez les paramètres de la « plage perdue » en définissant l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) sur l’objet de flux.
6.  Appelez [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) pour ajouter le nouveau flux au profil.

Créez maintenant l’objet ASF ContentInfo comme suit :

1.  Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo vide.
2.  Appelez [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour définir le profil ASF.

Le code suivant illustre ces étapes :


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a>6. créer le multiplexeur ASF

Le [multiplexeur ASF](asf-multiplexer.md) génère des paquets de données ASF.

1.  Appelez [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) pour créer le multiplexeur ASF.
2.  Appelez [**IMFASFMultiplexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) pour initialiser le multiplexeur. Transmettez un pointeur vers l’objet d’informations de contenu ASF qui a été créé dans la section précédente.
3.  Appelez [**IMFASFMultiplexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) pour définir l’indicateur de **\_ vitesse de \_ \_ transmission du multiplexeur MFASF** . Lorsque ce paramètre est utilisé, le multiplexeur ajuste automatiquement la vitesse de transmission du contenu ASF pour qu’il corresponde aux caractéristiques des flux en cours de multiplexage.


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. générer de nouveaux paquets de données ASF

Générez ensuite des paquets de données ASF pour le nouveau fichier. Ces paquets de données constituent l’objet de données ASF final pour le nouveau fichier. Pour générer de nouveaux paquets de données ASF :

1.  Appelez [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) pour créer un flux d’octets temporaire qui contiendra les paquets de données ASF.
2.  Appelez la fonction définie par l’application `GetNextAudioSample` pour obtenir des données audio non compressées pour l’encodeur.
3.  Transmettez l’audio non compressé à l’encodeur pour la compression. Pour plus d’informations, consultez [traitement des données dans l’encodeur](processing-data-in-the-encoder.md) .
4.  Appelez [**IMFASFMultiplexer ::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) pour envoyer les échantillons audio compressés au multiplexeur ASF en vue de la paquetage.
5.  Récupérez les paquets ASF du multiplexeur et écrivez-les dans le flux d’octets temporaire. Pour plus d’informations, consultez [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).
6.  Lorsque vous atteignez la fin du flux source, drainez l’encodeur et tirez les échantillons compressés restants à partir de l’encodeur. Pour plus d’informations sur la vidange d’une table MFT, consultez [modèle de traitement MFT de base](basic-mft-processing-model.md).
7.  Une fois tous les exemples envoyés au multiplexeur, appelez [**IMFASFMultiplexer :: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) et tirez les paquets ASF restants à partir du multiplexeur.
8.  Appelez [**IMFASFMultiplexer :: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).

Le code suivant génère des paquets de données ASF. La fonction retourne un pointeur vers un flux d’octets qui contient l’objet de données ASF.


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



Le code de la `GenerateASFDataPackets` fonction est affiché dans la rubrique [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).

## <a name="8-write-the-asf-file"></a>8. écrire le fichier ASF

Ensuite, écrivez l’en-tête ASF dans une mémoire tampon de média en appelant [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Cette méthode convertit les données stockées dans l’objet ContentInfo en données binaires au format d’objet d’en-tête ASF. Pour plus d’informations, consultez [génération d’un nouvel objet d’en-tête ASF](generating-a-new-asf-header-object.md).

Une fois que le nouvel objet d’en-tête ASF a été généré, créez un flux d’octets pour le fichier de sortie. Tout d’abord, écrivez l’objet d’en-tête dans le flux d’octets de sortie. Suivez l’objet d’en-tête avec l’objet de données contenu dans le flux d’octets de données.


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a>9. définir la fonction Entry-Point

Vous pouvez maintenant mettre ensemble les étapes précédentes dans une application complète. Avant d’utiliser l’un des objets Media Foundation, initialisez la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Lorsque vous avez terminé, appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Pour plus d’informations, consultez [initialisation des Media Foundation](initializing-media-foundation.md).

Le code suivant illustre l’application console complète. L’argument de ligne de commande spécifie le nom du fichier à convertir et le nom du nouveau fichier audio.


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



