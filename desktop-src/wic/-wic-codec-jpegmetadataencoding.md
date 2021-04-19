---
description: L’exemple suivant montre comment recoder une image et ses métadonnées dans un nouveau fichier de même format.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Comment recoder une image JPEG avec des métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106525317"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Comment recoder une image JPEG avec des métadonnées

L’exemple suivant montre comment recoder une image et ses métadonnées dans un nouveau fichier de même format. En outre, cet exemple ajoute des métadonnées pour illustrer une expression à un seul élément utilisée par un enregistreur de requête.

Cette rubrique contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Partie 1 : décoder une image](#part-1-decode-an-image)
-   [Partie 2 : créer et initialiser l’encodeur d’image](#part-2-create-and-initialize-the-image-encoder)
-   [Partie 3 : copier les informations de trame décodées](#part-3-copy-decoded-frame-information)
-   [Partie 4 : copier les métadonnées](#part-4-copy-the-metadata)
-   [Partie 5 : ajouter des métadonnées supplémentaires](#part-5-add-additional-metadata)
-   [Partie 6 : finaliser l’image encodée](#part-6-finalize-the-encoded-image)
-   [Exemple de code de recodage JPEG](#jpeg-re-encode-example-code)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Pour comprendre cette rubrique, vous devez être familiarisé avec le système de métadonnées WIC (Windows Imaging Component), comme décrit dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md). Vous devez également être familiarisé avec les composants du codec WIC comme décrit dans la [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).

## <a name="part-1-decode-an-image"></a>Partie 1 : décoder une image

Avant de pouvoir copier des données image ou des métadonnées dans un nouveau fichier image, vous devez d’abord créer un décodeur pour l’image existante que vous souhaitez recoder. Le code suivant montre comment créer un décodeur WIC pour le fichier image test.jpg.


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



L’appel à **CreateDecoderFromFilename** a utilisé la valeur WICDecodeMetadataCacheOnDemand de l’énumération [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) comme quatrième paramètre. Cela indique au décodeur de mettre en cache les métadonnées lorsque les métadonnées sont nécessaires, soit en obtenant un lecteur de requête, soit en utilisant le lecteur de métadonnées sous-jacent. L’utilisation de cette option vous permet de conserver le flux vers les métadonnées, ce qui est nécessaire pour effectuer rapidement un encodage des métadonnées et active le décodage et l’encodage sans perte d’images JPEG. Vous pouvez également utiliser l’autre valeur **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, qui met en cache les métadonnées de l’image incorporée dès le chargement de l’image.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Partie 2 : créer et initialiser l’encodeur d’image

Le code suivant illustre la création de l’encodeur que vous allez utiliser pour encoder l’image que vous avez décodée précédemment.


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



Un flux de fichier WIC piFileStream est créé et initialisé pour l’écriture dans le fichier image « test2.jpg ». piFileStream est ensuite utilisé pour initialiser l’encodeur, en informant l’encodeur où écrire les bits de l’image lorsque l’encodage est terminé.

## <a name="part-3-copy-decoded-frame-information"></a>Partie 3 : copier les informations de trame décodées

Le code suivant copie chaque image d’une image vers un nouveau frame de l’encodeur. Cette copie comprend la taille, la résolution et le format de pixel. tout ce qui est nécessaire pour créer un frame valide.

> [!Note]  
> Les images JPEG n’ont qu’un seul Frame et la boucle ci-dessous n’est pas techniquement nécessaire, mais elle est incluse pour illustrer l’utilisation de plusieurs frames pour les formats qui la prennent en charge.

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



Le code suivant effectue une vérification rapide pour déterminer si les formats d’image source et de destination sont identiques. Cela est nécessaire, car la quatrième partie montre une opération qui est uniquement prise en charge lorsque le format source et le format de destination sont identiques.


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a>Partie 4 : copier les métadonnées

> [!Note]  
> Le code de cette section est valide uniquement lorsque les formats d’image source et de destination sont identiques. Vous ne pouvez pas copier toutes les métadonnées d’une image en une seule opération lors de l’encodage dans un format d’image différent.

 

Pour conserver les métadonnées tout en recodant une image au même format d’image, il existe des méthodes permettant de copier toutes les métadonnées en une seule opération. Chacune de ces opérations suit un modèle similaire. chaque définit les métadonnées de l’image décodée directement dans le nouveau Frame encodé. Notez que cette opération est effectuée pour chaque image individuelle.

La méthode recommandée pour copier les métadonnées consiste à initialiser le writer de bloc du nouveau Frame avec le lecteur de bloc du frame décodé. L’exemple de code suivant illustre cette méthode.


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



Dans cet exemple, vous obtenez simplement le lecteur de bloc et le writer de bloc à partir du frame source et du frame de destination, respectivement. Le writer de bloc est ensuite initialisé à partir du lecteur de bloc. Cela initialise le writer de bloc avec les métadonnées préremplies du lecteur de bloc. Pour découvrir d’autres méthodes de copie des métadonnées, consultez la section écriture de métadonnées dans la [vue d’ensemble de la lecture et de l’écriture de métadonnées d’image](-wic-codec-readingwritingmetadata.md).

Là encore, cette opération fonctionne uniquement lorsque les images source et de destination ont le même format. Cela est dû au fait que différents formats d’image stockent les blocs de métadonnées à différents emplacements. Par exemple, les formats JPEG et TIFF (Tagged Image File Format) prennent en charge les blocs de métadonnées XMP (Extensible Metadata Platform). Dans les images JPEG, le bloc XMP se trouve dans le bloc de métadonnées racine, comme illustré dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md). Toutefois, dans une image TIFF, le bloc XMP est incorporé dans le bloc IFD racine.

## <a name="part-5-add-additional-metadata"></a>Partie 5 : ajouter des métadonnées supplémentaires

L’exemple suivant montre comment ajouter des métadonnées à l’image de destination. Pour ce faire, appelez la méthode **SetMetadataByName** du writer de requête à l’aide d’une expression de requête et des données stockées dans un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



Pour plus d’informations sur l’expression de requête, consultez la [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Partie 6 : finaliser l’image encodée

La dernière étape de la copie de l’image consiste à écrire les données de pixels du frame, à valider le frame sur l’encodeur et à valider l’encodeur. La validation de l’encodeur écrit le flux d’image dans le fichier.


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



La méthode **WriteSource** du frame est utilisée pour écrire les données de pixels de l’image. Notez que cette opération est effectuée une fois que les métadonnées ont été écrites. Cela est nécessaire pour garantir que les métadonnées disposent d’un espace suffisant dans le fichier image. Une fois les données de pixels écrites, le frame est écrit dans le flux à l’aide de la méthode **Commit** du frame. Une fois que tous les frames ont été traités, l’encodeur (et donc l’image) est finalisé à l’aide de la méthode **Commit** de l’encodeur.

Une fois que vous avez validé le frame, vous devez libérer les objets COM créés dans la boucle.

## <a name="jpeg-re-encode-example-code"></a>Exemple de code de recodage JPEG

Voici le code des parties 1 à 6 dans un bloc convienient.


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
