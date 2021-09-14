---
description: Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un nom de fichier image.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Comment créer un décodeur à l’aide d’un nom de fichier image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196159"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Comment créer un décodeur à l’aide d’un nom de fichier image

Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un nom de fichier image.

Pour créer un décodeur bitmap à l’aide d’un nom de fichier image

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

4.  Traitez le frame d’image. Pour plus d’informations sur les objets [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

## <a name="see-also"></a>Voir aussi

[Guide de programmation](-wic-programming-guide.md)


[Référence](-wic-codec-reference.md)


[Exemples](-wic-samples.md)


 

 



