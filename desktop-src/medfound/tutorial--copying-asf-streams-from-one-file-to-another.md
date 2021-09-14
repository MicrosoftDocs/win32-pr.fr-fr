---
description: Une façon de créer un fichier ASF consiste à copier des flux ASF à partir d’un fichier existant.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'didacticiel : copie de Flux ASF à l’aide d’objets WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235818"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>didacticiel : copie de Flux ASF à l’aide d’objets WMContainer

Une façon de créer un fichier ASF consiste à copier des flux ASF à partir d’un fichier existant. Pour ce faire, vous pouvez récupérer les données du média à partir du fichier source et écrire dans le fichier de sortie. Si le fichier source est un fichier ASF, vous pouvez copier des exemples de flux sans les décompresser et les recompresser.

Ce didacticiel présente ce scénario en extrayant le premier flux audio d’un fichier vidéo audio ASF (. wmv) et en le copiant dans un nouveau fichier audio ASF (. WMA). Dans ce didacticiel, vous allez créer une application console qui accepte les noms de fichiers d’entrée et de sortie comme arguments. L’application utilise le séparateur ASF pour analyser les exemples de flux d’entrée, puis les envoie au multiplexeur ASF pour écrire les paquets de données ASF pour le flux audio.

Ce didacticiel comprend les étapes suivantes :

-   [Composants requis](#prerequisites)
-   [Terminologie](#terminology)
-   [1. Configurez le Project](#1-set-up-the-project)
-   [2. déclarer des fonctions d’assistance](#2-declare-helper-functions)
-   [3. Ouvrez le fichier ASF d’entrée](#3-open-the-input-asf-file)
-   [4. initialiser des objets pour le fichier d’entrée](#4-initialize-objects-for-the-input-file)
-   [5. créer un profil audio](#5-create-an-audio-profile)
-   [6. initialiser des objets pour le fichier de sortie](#6-initialize-objects-for-the-output-file)
-   [7. générer de nouveaux paquets de données ASF](#7-generate-new-asf-data-packets)
-   [8. écrire les objets ASF dans le nouveau fichier](#8-write-the-asf-objects-in-the-new-file)
-   [9 écrire la fonction Entry-Point](#9-write-the-entry-point-function)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Ce didacticiel part des principes suivants :

-   Vous êtes familiarisé avec la structure d’un fichier ASF et les composants fournis par Media Foundation pour travailler avec des objets ASF. Ces composants incluent les objets ContentInfo, Splitter, multiplexer et Profile. Pour plus d’informations, consultez [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   Vous êtes familiarisé avec le processus d’analyse de l’objet d’en-tête ASF et des paquets de données ASF d’un fichier existant et de génération d’exemples de flux compressés à l’aide du séparateur. Pour plus d’informations, consultez [Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md).
-   Vous êtes familiarisé avec les mémoires tampons de média et les flux d’octets : en particulier, les opérations de fichier utilisant un flux d’octets et l’écriture du contenu d’une mémoire tampon de média dans un flux d’octets. (Voir [2. Déclarer des fonctions d’assistance](#2-declare-helper-functions).)

## <a name="terminology"></a>Terminologie

Ce didacticiel utilise les termes suivants :

-   Source d’octet source : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui contient le contenu du fichier d’entrée.
-   Objet ContentInfo source : objet ContentInfo, qui expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , qui représente l’objet d’en-tête ASF du fichier d’entrée.
-   Profil audio : objet de profil, expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , qui contient uniquement les flux audio du fichier d’entrée.
-   Exemple de flux : Sample Media, expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , générée par le séparateur, représente les données multimédia du flux sélectionné obtenues à partir du fichier d’entrée dans un État compressé.
-   Objet de sortie ContentInfo : objet ContentInfo, qui expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , qui représente l’objet d’en-tête ASF du fichier de sortie.
-   Flux d’octets de données : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui représente la partie entière de l’objet de données ASF du fichier de sortie.
-   Paquet de données : l’exemple de support, expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , généré par le multiplexeur représente un paquet de données ASF qui sera écrit dans le flux d’octets de données.
-   Sortie d’octet de sortie : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui contient le contenu du fichier de sortie.

## <a name="1-set-up-the-project"></a>1. Configurez le Project

Incluez les en-têtes suivants dans votre fichier source :


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



Lien vers les fichiers de bibliothèque suivants :

-   mfplat. lib
-   MF. lib
-   mfuuid. lib

Déclarez la fonction [SafeRelease](saferelease.md) :


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



## <a name="2-declare-helper-functions"></a>2. déclarer des fonctions d’assistance

Ce didacticiel utilise les fonctions d’assistance suivantes pour lire et écrire à partir d’un flux d’octets.

La `AllocReadFromByteStream` fonction lit les données à partir d’un flux d’octets et alloue une nouvelle mémoire tampon de média pour contenir les données. Pour plus d’informations, consultez [**IMFByteStream :: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



La `WriteBufferToByteStream` fonction écrit des données à partir d’une mémoire tampon de média dans un flux d’octets. Pour plus d’informations, consultez [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


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



La `AppendToByteStream` fonction ajoute le contenu d’un flux d’octets à un autre :


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



## <a name="3-open-the-input-asf-file"></a>3. Ouvrez le fichier ASF d’entrée

Ouvrez le fichier d’entrée en appelant la fonction [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . La méthode retourne un pointeur vers l’objet de flux d’octets qui contient le contenu du fichier. Le nom de fichier est spécifié par l’utilisateur via les arguments de ligne de commande de l’application.

L’exemple de code suivant prend un nom de fichier et retourne un pointeur vers un objet de flux d’octets qui peut être utilisé pour lire le fichier.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. initialiser des objets pour le fichier d’entrée

Ensuite, vous allez créer et initialiser l’objet de la source ContentInfo et le séparateur pour générer des exemples de flux.

Ce flux d’octet source créé à l’étape 2 sera utilisé pour analyser l’objet d’en-tête ASF et remplir l’objet de la source ContentInfo. Cet objet sera utilisé pour initialiser le séparateur afin de faciliter l’analyse des paquets de données ASF pour le flux audio dans le fichier d’entrée. Vous allez également récupérer la longueur de l’objet de données ASF dans le fichier d’entrée et le décalage vers le premier paquet de données ASF relatif au début du fichier. Ces attributs seront utilisés par le séparateur pour générer des exemples de flux audio.

Pour créer et initialiser des composants ASF pour le fichier d’entrée :

1.  Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer l’objet ContentInfo. Cette fonction retourne un pointeur vers l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Appelez [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) pour analyser l’en-tête ASF. Pour plus d’informations sur cette étape, consultez [lecture de l’objet d’en-tête ASF d’un fichier existant](reading-the-asf-header-object-of-an-existing-file.md).
3.  Appelez [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) pour créer l’objet Splitter ASF. Cette fonction retourne un pointeur vers l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
4.  Appelez [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), en passant le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo). Pour plus d’informations sur cette étape, consultez [création de l’objet Splitter ASF](creating-the-asf-splitter-object.md).
5.  Appelez [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) pour obtenir un descripteur de présentation pour le fichier ASF.
6.  Obtient la valeur de l’attribut de [**\_ décalage de \_ \_ \_ début \_ de données ASF**](mf-pd-asf-data-start-offset-attribute.md) pour la norme MF PD à partir du descripteur de présentation. Cette valeur correspond à l’emplacement de l’objet de données ASF dans le fichier, sous la forme d’un décalage d’octet par rapport au début du fichier.
7.  Obtient la valeur de l’attribut de [**\_ \_ \_ \_ longueur de données ASF**](mf-pd-asf-data-length-attribute.md) pour la norme MF PD à partir du descripteur de présentation. Cette valeur correspond à la taille totale de l’objet de données ASF, en octets. Pour plus d’informations, consultez [obtention d’informations à partir d’objets d’en-tête ASF](getting-information-from-asf-header-objects.md).

L’exemple de code suivant montre une fonction qui consolide toutes les étapes. Cette fonction accepte un pointeur vers le flux d’octets source et retourne des pointeurs vers l’objet ContentInfo source et le séparateur. En outre, il reçoit la longueur et les décalages de l’objet de données ASF.


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a>5. créer un profil audio

Ensuite, vous allez créer un objet de profil pour le fichier d’entrée en l’obtenant à partir de l’objet de la source ContentInfo. Vous allez ensuite configurer le profil afin qu’il ne contienne que les flux audio du fichier d’entrée. Pour ce faire, énumérez les flux et supprimez les flux non audio du profil. L’objet profil audio sera utilisé ultérieurement dans ce didacticiel pour initialiser l’objet ContentInfo de sortie.

Pour créer un profil audio

1.  Récupérez l’objet de profil du fichier d’entrée à partir de l’objet de la source ContentInfo en appelant [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). La méthode retourne un pointeur vers un objet de profil qui contient tous les flux du fichier d’entrée. Pour plus d’informations, consultez [création d’un profil ASF](creating-an-asf-profile.md).
2.  Supprimez tous les objets d’exclusion mutuelle du profil. Cette étape est requise car les flux non audio seront supprimés du profil, ce qui pourrait invalider les objets d’exclusion mutuelle.
3.  Supprimez tous les flux non audio du profil, comme suit :
    -   Appelez [**IMFASFProfile :: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) pour connaître le nombre de flux.
    -   Dans une boucle, appelez [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) pour obtenir chaque flux par index.
    -   Appelez [**IMFASFStreamConfig :: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) pour accéder au type de flux.
    -   Pour les flux non audio, appelez [**IMFASFProfile :: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) pour supprimer le flux.
4.  Stocke le numéro de flux du premier flux audio. Ce sera sélectionné sur le séparateur pour générer des exemples de flux. Si le numéro de flux est égal à zéro, l’appelant peut supposer qu’il n’y avait pas de fichier de flux audio.

Le code suivant décrit ces étapes :


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



La `RemoveMutexes` fonction supprime tous les objets d’exclusion mutuelle du profil :


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a>6. initialiser des objets pour le fichier de sortie

Ensuite, vous allez créer l’objet ContentInfo de sortie et le multiplexeur pour générer des paquets de données pour le fichier de sortie.

Le profil audio créé à l’étape 4 sera utilisé pour remplir l’objet ContentInfo de sortie. Cet objet contient des informations telles que des attributs de fichier globaux et des propriétés de flux. L’objet ContentInfo de sortie sera utilisé pour initialiser le multiplexeur qui générera des paquets de données pour le fichier de sortie. Une fois les paquets de données générés, l’objet ContentInfo doit être mis à jour pour refléter les nouvelles valeurs.

Pour créer et initialiser des composants ASF pour le fichier de sortie

1.  Créez un objet ContentInfo vide en appelant [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) et remplissez-le avec les informations du profil audio créé à l’étape 3 en appelant [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Pour plus d’informations, consultez [initialisation de l’objet ContentInfo d’un nouveau fichier ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).
2.  Créez et initialisez l’objet multiplexeur à l’aide de l’objet ContentInfo de sortie. Pour plus d’informations, consultez [création de l’objet multiplexeur](creating-the-multiplexer-object.md).

L’exemple de code suivant montre une fonction qui consolide les étapes. Cette fonction accepte un pointeur vers un objet de profil et retourne des pointeurs vers l’objet ContentInfo de sortie et le multiplexeur.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. générer de nouveaux paquets de données ASF

Ensuite, vous allez générer des exemples de flux audio à partir du flux d’octets source à l’aide du séparateur et les envoyer au multiplexeur pour créer des paquets de données ASF. Ces paquets de données constituent l’objet de données ASF final pour le nouveau fichier.

Pour générer des exemples de flux audio

1.  Sélectionnez le premier flux audio sur le séparateur en appelant [**IMFASFSplitter :: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).
2.  Lit les blocs de taille fixe des données multimédias à partir du flux d’octets source dans une mémoire tampon de média.
3.  Collectez les exemples de flux en tant qu’exemples de supports à partir du séparateur en appelant [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) dans une boucle, à condition qu’il reçoive l' \_ indicateur ASF STATUSFLAGS \_ incomplet dans le paramètre *pdwStatusFlags* . Pour plus d’informations, consultez génération d’exemples pour les paquets de données ASF» dans [génération d’exemples de flux à partir d’un objet de données ASF existant](generating-stream-samples-from-an-existing-asf-data-object.md).
4.  Pour chaque exemple de support, appelez [**IMFASFMultiplexer ::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) pour envoyer l’exemple de support au multiplexeur. Le multiplexeur génère les paquets de données pour l’objet de données ASF.
5.  Écrire le paquet de données généré par le multiplexeur dans le flux d’octets de données.
6.  Une fois tous les paquets de données générés, appelez [**IMFASFMultiplexer :: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) pour mettre à jour l’objet ContentInfo de sortie avec les informations collectées pendant la génération des paquets de données ASF.

L’exemple de code suivant génère des exemples de flux à partir du séparateur ASF et les envoie au multiplexeur. Le multiplexeur génère des paquets de données ASF et les écrit dans un flux.


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



Pour recevoir des paquets du séparateur ASF, le code précédent appelle la `GetPacketsFromSplitter` fonction, comme indiqué ici :


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



La `GenerateDataPackets` fonction obtient les paquets de données du multiplexeur. Pour plus d’informations, consultez [obtention de paquets de données ASF](generating-new-asf-data-packets.md).


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. écrire les objets ASF dans le nouveau fichier

Ensuite, vous allez écrire le contenu de l’objet ContentInfo de sortie dans une mémoire tampon de média en appelant [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Cette méthode convertit les données stockées dans l’objet ContentInfo en données binaires au format d’objet d’en-tête ASF. Pour plus d’informations, consultez [génération d’un nouvel objet d’en-tête ASF](generating-a-new-asf-header-object.md).

Une fois le nouvel objet d’en-tête ASF généré, écrivez le fichier de sortie en écrivant d’abord l’objet d’en-tête dans le flux d’octets de sortie créé à l’étape 2 en appelant la fonction d’assistance WriteBufferToByteStream. Suivez l’objet d’en-tête avec l’objet de données contenu dans le flux d’octets de données. L’exemple de code montre une fonction qui transfère le contenu du flux d’octets de données vers le flux d’octets de sortie.


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a>9 écrire la fonction Entry-Point

Vous pouvez maintenant mettre ensemble les étapes précédentes dans une application complète. Avant d’utiliser l’un des objets Media Foundation, initialisez la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Lorsque vous avez terminé, appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Pour plus d’informations, consultez [initialisation des Media Foundation](initializing-media-foundation.md).

Le code suivant illustre l’application console complète. L’argument de ligne de commande spécifie le nom du fichier à convertir et le nom du nouveau fichier audio.


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
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

 

 



