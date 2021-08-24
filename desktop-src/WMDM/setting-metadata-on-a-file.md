---
title: Définition de métadonnées sur un fichier
description: Définition de métadonnées sur un fichier
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Windows Gestionnaire de périphériques de média, métadonnées
- Gestionnaire de périphériques, métadonnées
- Guide de programmation, métadonnées
- applications de bureau, métadonnées
- création d’applications de Gestionnaire de périphériques Windows Media, métadonnées
- écriture de fichiers sur des appareils, métadonnées
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64bdd173258272801886b90dca2265425eb65fd8ec3e5a25d01db37453d7eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766270"
---
# <a name="setting-metadata-on-a-file"></a>Définition de métadonnées sur un fichier

Vous pouvez définir des métadonnées sur un fichier avant de l’écrire sur l’appareil (lors de l’utilisation de [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) ou sur un stockage existant (en appelant [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)). Vous pouvez définir des attributs uniquement sur un stockage existant (en appelant [**IWMDMStorage :: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) ou [**IWMDMStorage2 :: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).

La définition des métadonnées s’effectue en créant et en remplissant une interface [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) transmise dans [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3). Toutefois, cette méthode peut effacer toutes les métadonnées existantes sur le fichier, à l’exception des métadonnées codées en dur stockées dans le système de fichiers lui-même, telles que le nom ou la taille du fichier. Par conséquent, vous devez copier toutes les métadonnées existantes que vous souhaitez conserver dans l’interface IWMDMMetaData que vous envoyez. étant donné que Windows media Gestionnaire de périphériques ne peut pas être utilisé pour récupérer des métadonnées à partir de fichiers locaux, vous devez utiliser le kit de développement logiciel (SDK) de Format multimédia Windows (ou tout autre outil) pour récupérer ces métadonnées.

pour utiliser le kit de développement logiciel (SDK) Windows Media Format pour récupérer les propriétés des fichiers ASF, procédez comme suit :

1.  Créez un objet d’éditeur de métadonnées en appelant **WMCreateEditor** et en demandant une interface **IWMMetadataEditor** .
2.  Ouvrez le fichier pour la lecture des métadonnées en appelant **IWMMetadataEditor :: Open**.
3.  Si le fichier est un fichier ASF valide et peut être ouvert, interrogez l’éditeur de l’interface **IWMHeaderInfo** .
4.  récupérez les propriétés de fichier en appelant **IWMHeaderInfo :: GetAttributeByName**, en passant la constante de propriété du kit de développement logiciel (SDK) du Format de média souhaité Windows. le tableau suivant répertorie les constantes du kit de développement logiciel (sdk) de Format correspondant aux constantes Windows Media Gestionnaire de périphériques sdk équivalentes.



| Windows Constante SDK Media format    | Windows Constante SDK Media Gestionnaire de périphériques      |
|--------------------------------------|------------------------------------------------|
| \_wszWMTitle g                        | \_wszWMDMTitle g                                |
| \_wszWMAuthor g                       | \_wszWMDMAuthor g                               |
| \_wszWMAlbumTitle g                   | \_wszWMDMAlbumTitle g                           |
| \_wszWMGenre g                        | \_wszWMDMGenre g                                |
| \_wszWMYear g                         | \_wszWMDMYear g                                 |
| g \_ wszWMTrackNumber ou g \_ wszWMTrack | \_wszWMDMTrack g                                |
| \_wszWMComposer g                     | \_wszWMDMComposer g                             |
| \_wszWMDuration g                     | \_wszWMDMDuration g                             |
| \_wszWMCopyright g                    | \_wszWMDMProviderCopyright g                    |
| \_wszWMDescription g                  | \_wszWMDMDescription g                          |
| \_wszWMBitrate g                      | \_wszWMDMBitrate g                              |
| \_wszWMRating g                       | \_wszWMDMUserRating g                           |
| \_wszWMAlbumArtist g                  | \_wszWMDMAlbumArtist g                          |
| \_wszWMParentalRating g               | \_wszWMDMParentalRating g                       |
| \_wszWMRadioStationName g             | \_wszWMDMMediaStationName g                     |
| \_wszWMSubTitle g                     | \_wszWMDMSubTitle g                             |
| \_wszWMVideoWidth g                   | \_wszWMDMWidth g                                |
| \_wszWMVideoHeight g                  | \_wszWMDMHeight g                               |
| \_wszWMMood g                         | \_wszWMDMTrackMood g                            |
| \_wszWMCodec g                        | g \_ wszAudioWAVECodec ou g \_ wszVideoFourCCCodec |



 

l’exemple de code C++ suivant illustre l’extraction d’un certain nombre de propriétés de métadonnées d’un fichier ASF à l’aide du kit de développement logiciel (SDK) Windows media Format et leur conversion en équivalent Windows Gestionnaire de périphériques valeurs de média.


```C++
// Structure and array to hold equivalent Windows Media Format SDK 
// and Windows Media Device Manager SDK metadata property names.
struct EquivalentProperty
{
    LPCWSTR FormatSDKConst;
    LPCWSTR WMDMSDKConst;
};
EquivalentProperty EquivalentProperties []= 
{
    {g_wszWMTitle,        g_wszWMDMTitle},
    {g_wszWMAuthor,      g_wszWMDMAuthor},
    {g_wszWMAlbumTitle,  g_wszWMDMAlbumTitle},
    {g_wszWMGenre,       g_wszWMDMGenre},
    {g_wszWMYear,        g_wszWMDMYear},
    {g_wszWMTrackNumber, g_wszWMDMTrack},
    {g_wszWMTrack,       g_wszWMDMTrack},
    {g_wszWMComposer,    g_wszWMDMComposer},
    {g_wszWMBitrate,     g_wszWMDMBitrate},
    {g_wszWMDuration,    g_wszWMDMDuration},
    {g_wszWMCopyright,   g_wszWMDMProviderCopyright},
    {g_wszWMDescription, g_wszWMDMDescription},
    {g_wszWMRating,      g_wszWMDMUserRating},
    {g_wszWMAlbumArtist, g_wszWMDMAlbumArtist},
    {g_wszWMParentalRating,    g_wszWMDMParentalRating},
    {g_wszWMRadioStationName,  g_wszWMDMMediaStationName},
    {g_wszWMSubTitle,    g_wszWMDMSubTitle},
    {g_wszWMVideoWidth,  g_wszWMDMWidth},
    {g_wszWMVideoHeight, g_wszWMDMHeight},
    {g_wszWMMood,        g_wszWMDMTrackMood},
    {g_wszWMCodec,       g_wszAudioWAVECodec},
    {g_wszWMCodec,       g_wszVideoFourCCCodec}
};
// Function that tries to get metadata by using the Format SDK. 
// If it cannot open the file, it returns E_FAIL.
HRESULT GetFileMetadataFromFormatSDK(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    if ((pMetaData == NULL) || (file == NULL)) return E_INVALIDPARAM;
    HRESULT hr = S_OK;
    CComPtr<IWMMetadataEditor> pEditor;

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do {
        hr = WMCreateEditor(&pEditor);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pEditor->Open(file);
        if (FAILED(hr)) 
            break;

        CComPtr<IWMHeaderInfo>pHeaderInfo;
        hr = pEditor->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHeaderInfo);
        if (FAILED(hr))
            break;

        // Copy values from Format SDK to equivalent WMDM SDK metadata values.

        // Loop through all known values
        WORD stream = 0;
        WMT_ATTR_DATATYPE wmfType;
        WORD len = 0;
        BYTE* value = NULL;
        WMDM_TAG_DATATYPE wmdmType;
        for (int i = 0; i < sizeof(EquivalentProperties) / sizeof(EquivalentProperties[0]); i++)
        {
            // Request each value from our equivalency list by name.
            // The function is called twice: once to get the buffer size,
            // and once to get the value in the allocated buffer.
            if (FAILED(pHeaderInfo->GetAttributeByName(
                &stream, EquivalentProperties[i].FormatSDKConst, &wmfType, NULL, &len)))
            {
                continue;
            }

            value = new BYTE[len];
            if (value == NULL) continue;

            if (FAILED(pHeaderInfo->GetAttributeByName(&stream, EquivalentProperties[i].FormatSDKConst, &wmfType, value, &len)))
            {
                delete[] value;
                continue;
            }

            // Send the data to the equivalent WMDM metadata value.
            // First, find the equivalent WMDM type for the WMF type.
            switch(wmfType)
            {
            case WMT_TYPE_BINARY:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            case WMT_TYPE_DWORD:
                wmdmType = WMDM_TYPE_DWORD;
                break;
            case WMT_TYPE_STRING:
                wmdmType = WMDM_TYPE_STRING;
                break;
            case WMT_TYPE_BOOL:
                wmdmType = WMDM_TYPE_BOOL;
                break;
            case WMT_TYPE_QWORD:
                wmdmType = WMDM_TYPE_QWORD;
                break;
            case WMT_TYPE_WORD:
                wmdmType = WMDM_TYPE_WORD;
                break;
            case WMT_TYPE_GUID:
                wmdmType = WMDM_TYPE_GUID;
                break;
            default:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            }

            // Don't worry about trapping errors, because there's nothing 
            // we can do about it.
            pMetadata->AddItem(wmdmType, 
                EquivalentProperties[i].WMDMSDKConst, value, len);
            delete[] value;
        } // Add next value.
    } while (FALSE); // End Do loop error trap.

    // Close the file opened with IWMMetadataEditor.
    pEditor->Close();
    return hr;
}
```



l’exemple de fonction C++ suivant montre comment utiliser DirectShow pour récupérer des informations de fichier et les ajouter aux métadonnées.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
HRESULT GetFileMetadataFromDShow(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    HRESULT hr = S_OK;

    // Add file metadata properties from DirectShow. 
    // This is good for non-ASF files, or to add any information
    // that the Format SDK didn't get.

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do
    {
        // Create the Media Detector object.
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pIMediaDet->put_Filename(BSTR(file));
        if (FAILED(hr))
            break;

        // Get the media type for the default stream.
        AM_MEDIA_TYPE mediaType;
        hr = pIMediaDet->get_StreamMediaType(&mediaType);
        if (FAILED(hr))
            break;

        // We have the file open, so start requesting information from the 
        // Media Detector and adding it to the metadata. When adding 
        // individual metadata values, ignore the HRESULT, because failure 
        // to add these metadata values is not a breaking issue.

        // Get major and minor types.
        WCHAR strMediaType[64];
        ZeroMemory(strMediaType, 64);

        //Change the major type to a string, then add to IWMDMMetaData.
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.majortype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
             g_wszWMDMediaClassPrimaryID, 
            (BYTE*) strMediaType, 
             sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Clear local string, then retrieve subtype the same way.
        ZeroMemory(strMediaType, 64);
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.subtype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
            g_wszWMDMMediaClassSecondaryID, (BYTE*) strMediaType,
            sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Get the duration. Duration is retrieved in seconds, but set 
        // in 100-nanosecond units.
        double duration = 0;
        hr = pIMediaDet->get_StreamLength(&duration);
        if (duration > 0)
        {
            duration *= 10E7;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMDuration, (BYTE*) &duration, sizeof(duration));
        }

        // Get the frame rate.
        double frameRate = 0;
        hr = pIMediaDet->get_FrameRate(&frameRate);
        if (frameRate > 0)
        {
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFrameRate, 
                (BYTE*) &frameRate,
                sizeof(frameRate));
        }

        // Get the structure for the default stream's major type and 
        // fill in additional information.

        if (IsEqualGUID(mediaType.formattype, FORMAT_VideoInfo))
        {
            VIDEOINFOHEADER* data = (VIDEOINFOHEADER*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMVideoBitrate, 
               (BYTE*) &data->dwBitRate, sizeof(DWORD));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMHeight, 
               (BYTE*) &data->bmiHeader.biHeight, sizeof(LONG));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMWidth, 
               (BYTE*) &data->bmiHeader.biWidth, sizeof(LONG));
        }

        if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
        {
            WAVEFORMATEX* data = (WAVEFORMATEX*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMBlockAlignment, 
                (BYTE*) &data->nBlockAlign, sizeof(WORD));
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMNumChannels, 
               (BYTE*) &data->nChannels, sizeof(WORD));
        }
    } while (FALSE); // End of error loop.
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers sur l’appareil**](writing-files-to-the-device.md)
</dt> </dl>

 

 




