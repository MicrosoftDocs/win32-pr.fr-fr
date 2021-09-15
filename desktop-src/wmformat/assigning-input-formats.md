---
title: Assigner des formats d’entrée
description: Assigner des formats d’entrée
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- ASF (Advanced Systems Format), affectation de formats d’entrée
- ASF (format des systèmes avancés), assigner des formats d’entrée
- profils, assigner des formats d’entrée
- codecs, assigner des formats d’entrée
- ASF (Advanced Systems Format), attributions de format d’entrée
- ASF (format des systèmes avancés), attributions de format d’entrée
- profils, affectations de format d’entrée
- codecs, affectations de format d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c6ad1bcdf161b335d9367d7de4df84b7eb2e6ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523077"
---
# <a name="assigning-input-formats"></a>Assigner des formats d’entrée

Une fois que vous avez identifié le format d’entrée qui correspond à vos données, vous pouvez le configurer pour qu’il soit utilisé par le writer en appelant [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).

Pour les flux vidéo, vous devez définir la taille des frames dans les exemples d’entrée. L’exemple de code suivant montre comment configurer et définir une entrée vidéo. Elle utilise la fonction **FindInputFormat** définie dans la section [pour énumérer les formats d’entrée](to-enumerate-input-formats.md) pour obtenir le format d’entrée pour la vidéo RVB 24 bits. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Get the size of the media type structure.
    hr = pProps->GetMediaType(NULL, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Allocate memory for the media type structure.
    pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
    if (pType == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }
    
    // Get the media type structure.
    hr = pProps->GetMediaType(pType, &cbSize);
    if (FAILED(hr))
    {
        goto Exit;
    }

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> </dl>

 

 




