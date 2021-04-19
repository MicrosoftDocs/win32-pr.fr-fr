---
description: Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un flux.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Comment créer un décodeur à l’aide d’un flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538376"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a>Comment créer un décodeur à l’aide d’un flux

Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un flux.

Pour créer un décodeur bitmap à l’aide d’un flux

1.  Charge un fichier image dans un flux. Dans cet exemple, un flux est créé pour une ressource d’application.

    Dans le fichier de définition de ressource d’application (. RC), définissez la ressource. L’exemple suivant définit une `Image` ressource nommée `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    La ressource sera ajoutée aux ressources de l’application lors de la génération de l’application.

2.  Chargez la ressource à partir de l’application.

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  Verrouillez la ressource et récupérez la taille.

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  Créez un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  Utilisez la méthode [**CreateStream,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) pour créer un objet [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) et l’initialiser à l’aide du pointeur mémoire d’image.

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  Créez une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir du nouvel objet de flux à l’aide de la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Le format de fichier JPEG ne prend en charge qu’une seule trame. Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé. Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.

8.  Traitez le frame d’image. Pour plus d’informations sur les objets [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

## <a name="see-also"></a>Voir aussi

[Guide de programmation](-wic-programming-guide.md)


[Référence](-wic-codec-reference.md)


[Exemples](-wic-samples.md)


 

 



