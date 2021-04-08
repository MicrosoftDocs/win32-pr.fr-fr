---
description: Cette rubrique montre comment charger un IWICBitmapFrameDecode à partir d’une ressource d’application.
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: Chargement d’une image bitmap à partir d’une ressource (composant Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb33ad57b3b9dac1cb5d98719c681adb38c11de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865809"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a>Chargement d’une image bitmap à partir d’une ressource (composant Windows Imaging)

Cette rubrique montre comment charger un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) à partir d’une ressource d’application.

1.  Dans le fichier de définition de ressource d’application (. RC), définissez la ressource. L’exemple suivant définit une `Image` ressource nommée `IDR_SAMPLE_IMAGE` .

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

    

4.  Utilisez la méthode [**CreateStream,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) pour créer un objet [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) et l’initialiser à l’aide du pointeur mémoire d’image.

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

    

5.  Créez une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir du nouvel objet de flux à l’aide de la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

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

    

6.  Récupérez un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) à partir de l’image décodée.

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Ce code récupère uniquement la première ( `0` ) image de l’image. Pour les images multiframes, utilisez [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) pour déterminer le nombre de frames dans l’image.

## <a name="see-also"></a>Voir aussi

[Guide de programmation](-wic-programming-guide.md)


[Référence](-wic-codec-reference.md)


[Exemples](-wic-samples.md)


 

 



