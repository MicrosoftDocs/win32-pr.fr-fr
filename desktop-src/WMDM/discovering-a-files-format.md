---
title: Découverte du format d’un fichier
description: Découverte du format d’un fichier
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Gestionnaire de périphériques de média, formats de fichiers
- Gestionnaire de périphériques, formats de fichiers
- Guide de programmation, formats de fichiers
- applications de bureau, formats de fichiers
- création d’applications Windows Media Gestionnaire de périphériques, formats de fichiers
- écriture de fichiers sur des appareils, formats de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585328"
---
# <a name="discovering-a-files-format"></a>Découverte du format d’un fichier

Avant d’envoyer un fichier à l’appareil, une application doit déterminer si l’appareil prend en charge ce format de fichier.

La découverte du format d’un fichier peut être complexe. La méthode la plus simple consiste à créer une liste d’extensions de fichier mappées à des \_ valeurs d’énumération FORMATCODE WMDM spécifiques. Toutefois, il existe quelques problèmes avec ce système : l’un est qu’un seul format peut avoir plusieurs extensions (telles que .jpg,. jpe et. jpeg pour les images JPEG). En outre, la même extension de fichier peut être utilisée par différents programmes pour différents formats.

Pour surmonter les limitations d’un mappage strict, il est préférable pour une application de vérifier que le format correspond à l’extension. le kit de développement logiciel (SDK) DirectShow fournit des outils qui permettent à une application de découvrir un ensemble limité de détails sur la plupart des types de fichiers multimédias. le kit de développement logiciel (SDK) Windows Media Format expose un grand nombre de détails, mais uniquement des fichiers ASF. étant donné que le code de format de tous les types de fichiers doit être vérifié si possible, il est préférable d’utiliser DirectShow pour découvrir ou vérifier le code de format de base, et utiliser le kit de développement logiciel (SDK) Windows Media format pour découvrir les métadonnées supplémentaires souhaitées sur les fichiers ASF. DirectShow peut également être utilisé pour découvrir des métadonnées de base pour les fichiers non ASF.

Voici un moyen de découvrir un format de fichier à l’aide du mappage d’extension et de DirectShow.

Tout d’abord, comparez l’extension de nom de fichier à une liste d’extensions connues. Veillez à ne pas respecter la casse de la comparaison. Si l’extension n’est pas mappée, définissez le format sur WMDM \_ FORMATCODE non \_ défini.

-   Si le code de format est introuvable (ou si vous souhaitez vérifier qu’un fichier est un fichier multimédia), vous pouvez effectuer les étapes suivantes :
    1.  créez un objet de détecteur de média DirectShow à l’aide de **CoCreateInstance**(CLSID \_ MediaDet) et récupérez l’interface **IMediaDet** .
    2.  Ouvrez le fichier en appelant **IMediaDet ::p ut \_ nom_fichier**. Cet appel échoue si le fichier est protégé.
    3.  Obtient le type de média du flux par défaut en appelant **IMediaDet :: obten \_ StreamMediaType**, qui retourne **un \_ \_ type de média am**.
    4.  Récupérez le nombre de flux en appelant **IMediaDet :: obten \_ OutputStreams**.
        -   S’il n’existe qu’un seul flux et qu’il s’agit de l’audio, le type de fichier est WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO
        -   S’il n’existe qu’un seul flux et qu’il s’agit d’une vidéo, le type de fichier est WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO
        -   S’il n’existe qu’un seul flux et qu’il s’agit d’une vidéo et que la vitesse de transmission est égale à zéro, le type de fichier est WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.

Vous pouvez également essayer de mettre en correspondance les codecs audio ou Video à partir des membres **VIDEOINFOHEADER** ou **WAVEFORMATEX** récupérés à partir de la **\_ StreamMediaType**.

la fonction C++ suivante illustre la correspondance d’extension de fichier et l’utilisation de DirectShow pour essayer d’analyser des fichiers inconnus.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers sur l’appareil**](writing-files-to-the-device.md)
</dt> </dl>

 

 




