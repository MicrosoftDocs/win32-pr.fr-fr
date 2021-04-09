---
title: Découverte du format d’un fichier
description: Découverte du format d’un fichier
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Media Gestionnaire de périphériques, formats de fichiers
- Gestionnaire de périphériques, formats de fichiers
- Guide de programmation, formats de fichiers
- applications de bureau, formats de fichiers
- création d’applications Windows Media Gestionnaire de périphériques, formats de fichiers
- écriture de fichiers sur des appareils, formats de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672669"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="401de-109">Découverte du format d’un fichier</span><span class="sxs-lookup"><span data-stu-id="401de-109">Discovering a File's Format</span></span>

<span data-ttu-id="401de-110">Avant d’envoyer un fichier à l’appareil, une application doit déterminer si l’appareil prend en charge ce format de fichier.</span><span class="sxs-lookup"><span data-stu-id="401de-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="401de-111">La découverte du format d’un fichier peut être complexe.</span><span class="sxs-lookup"><span data-stu-id="401de-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="401de-112">La méthode la plus simple consiste à créer une liste d’extensions de fichier mappées à des \_ valeurs d’énumération FORMATCODE WMDM spécifiques.</span><span class="sxs-lookup"><span data-stu-id="401de-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="401de-113">Toutefois, il existe quelques problèmes avec ce système : l’un est qu’un seul format peut avoir plusieurs extensions (telles que. jpg,. jpe et. jpeg pour les images JPEG).</span><span class="sxs-lookup"><span data-stu-id="401de-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="401de-114">En outre, la même extension de fichier peut être utilisée par différents programmes pour différents formats.</span><span class="sxs-lookup"><span data-stu-id="401de-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="401de-115">Pour surmonter les limitations d’un mappage strict, il est préférable pour une application de vérifier que le format correspond à l’extension.</span><span class="sxs-lookup"><span data-stu-id="401de-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="401de-116">Le kit de développement logiciel (SDK) DirectShow fournit des outils qui permettent à une application de découvrir un ensemble limité de détails sur la plupart des types de fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="401de-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="401de-117">Le kit de développement logiciel (SDK) du format Windows Media expose un grand nombre de détails, mais uniquement des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="401de-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="401de-118">Étant donné que le code de format de tous les types de fichiers doit être vérifié si possible, il est préférable d’utiliser DirectShow pour découvrir ou vérifier le code de format de base, et utiliser le kit de développement logiciel (SDK) de format Windows Media pour découvrir les métadonnées supplémentaires souhaitées sur les fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="401de-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="401de-119">DirectShow peut également être utilisé pour découvrir des métadonnées de base pour les fichiers non ASF.</span><span class="sxs-lookup"><span data-stu-id="401de-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="401de-120">Voici un moyen de découvrir un format de fichier à l’aide du mappage d’extension et de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="401de-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="401de-121">Tout d’abord, comparez l’extension de nom de fichier à une liste d’extensions connues.</span><span class="sxs-lookup"><span data-stu-id="401de-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="401de-122">Veillez à ne pas respecter la casse de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="401de-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="401de-123">Si l’extension n’est pas mappée, définissez le format sur WMDM \_ FORMATCODE non \_ défini.</span><span class="sxs-lookup"><span data-stu-id="401de-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="401de-124">Si le code de format est introuvable (ou si vous souhaitez vérifier qu’un fichier est un fichier multimédia), vous pouvez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="401de-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="401de-125">Créez un objet DirectShow Media Detection à l’aide de **CoCreateInstance**(CLSID \_ MediaDet) et récupérez l’interface **IMediaDet** .</span><span class="sxs-lookup"><span data-stu-id="401de-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="401de-126">Ouvrez le fichier en appelant **IMediaDet ::p ut \_ nom_fichier**.</span><span class="sxs-lookup"><span data-stu-id="401de-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="401de-127">Cet appel échoue si le fichier est protégé.</span><span class="sxs-lookup"><span data-stu-id="401de-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="401de-128">Obtient le type de média du flux par défaut en appelant **IMediaDet :: obten \_ StreamMediaType**, qui retourne **un \_ \_ type de média am**.</span><span class="sxs-lookup"><span data-stu-id="401de-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="401de-129">Récupérez le nombre de flux en appelant **IMediaDet :: obten \_ OutputStreams**.</span><span class="sxs-lookup"><span data-stu-id="401de-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="401de-130">S’il n’existe qu’un seul flux et qu’il s’agit de l’audio, le type de fichier est WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO</span><span class="sxs-lookup"><span data-stu-id="401de-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="401de-131">S’il n’existe qu’un seul flux et qu’il s’agit d’une vidéo, le type de fichier est WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO</span><span class="sxs-lookup"><span data-stu-id="401de-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="401de-132">S’il n’existe qu’un seul flux et qu’il s’agit d’une vidéo et que la vitesse de transmission est égale à zéro, le type de fichier est WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="401de-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="401de-133">Vous pouvez également essayer de mettre en correspondance les codecs audio ou Video à partir des membres **VIDEOINFOHEADER** ou **WAVEFORMATEX** récupérés à partir de la **\_ StreamMediaType**.</span><span class="sxs-lookup"><span data-stu-id="401de-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="401de-134">La fonction C++ suivante illustre la correspondance d’extension de fichier et l’utilisation de DirectShow pour essayer d’analyser les fichiers inconnus.</span><span class="sxs-lookup"><span data-stu-id="401de-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="401de-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="401de-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401de-136">**Écriture de fichiers sur l’appareil**</span><span class="sxs-lookup"><span data-stu-id="401de-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




