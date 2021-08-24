---
description: Cette rubrique montre comment faire pivoter un IWICBitmapSource à l’aide d’un composant IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Comment retourner et faire pivoter une source bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a61a1546f5a0191d2e20cc3079af3e4d772e6d2c3c07a5dd1e1e4aa331dc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331543"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Comment retourner et faire pivoter une source bitmap

Cette rubrique montre comment faire pivoter un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’aide d’un composant [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .

Pour retourner et faire pivoter une source bitmap

1.  créez un objet [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    Le format de fichier JPEG ne prend en charge qu’une seule trame. Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé. Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.

4.  Créez le [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) à utiliser pour le retournement de l’image.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Initialise l’objet Flip/Rotate avec les données image du frame bitmap retourné horizontalement (le long de l’axe vertical y).

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    Consultez [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) pour obtenir des rotations et des options de retournement supplémentaires.

6.  Dessinez ou traitez la source bitmap retournée.

    > [!Note]  
    > L’interface [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) hérite de l’interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . vous pouvez donc utiliser l’objet Flip/Rotate initialisé n’importe où qui accepte un **IWICBitmapSource**.

     

    L’illustration suivante montre le basculement d’une image horizontale (le long de l’axe vertical x).

    ![Illustration montrant un retournement horizontal (le long de l’axe x de vérité) d’une image](graphics/fliphorizontal.png)

## <a name="see-also"></a>Voir aussi

[Guide de programmation](-wic-programming-guide.md)


[Référence](-wic-codec-reference.md)


[Exemples](-wic-samples.md)


 

 



