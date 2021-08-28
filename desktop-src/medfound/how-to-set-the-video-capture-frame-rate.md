---
description: Un périphérique de capture vidéo peut prendre en charge une plage de fréquences d’images.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Comment définir la fréquence d’images de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0e80c26c5a53a89cbc87ca509f25db1ebccf4571b4dda2e83ea63717c7d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827969"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Comment définir la fréquence d’images de capture vidéo

Un périphérique de capture vidéo peut prendre en charge une plage de fréquences d’images. Si ces informations sont disponibles, les fréquences d’images minimale et maximale sont stockées en tant qu’attributs de type de média :



| Attribut                                                         | Description         |
|-------------------------------------------------------------------|---------------------|
| [\_plage de \_ fréquence d’images MF MT \_ \_ \_ Max](mf-mt-frame-rate-range-max.md) | Fréquence d’images maximale. |
| [plage de fréquence d’images MF- \_ \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md) | Fréquence d’images minimale. |



 

La plage peut varier en fonction du format de capture. Par exemple, avec des tailles d’image supérieures, la fréquence d’images maximale peut être réduite.

Pour définir la fréquence d’images :

1.  Créez la source du média pour l’appareil de capture. Consultez [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).
2.  Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source du média pour récupérer le descripteur de présentation.
3.  Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour obtenir le descripteur de flux du flux vidéo.
4.  Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux.
5.  Énumérez les formats de capture, comme décrit dans [comment définir le format de capture vidéo](how-to-set-the-video-capture-format.md).
6.  Sélectionnez le format de sortie souhaité dans la liste.
7.  Interrogez le type de média pour les attributs de plage de fréquence d’images [MF \_ MT \_ \_ \_ \_ Max](mf-mt-frame-rate-range-max.md) et [MF à \_ \_ \_ fréquence d' \_ \_ images MF](mf-mt-frame-rate-range-min.md) . Ces valeurs donnent la plage de fréquences d’images prises en charge. L’appareil peut prendre en charge d’autres fréquences d’images dans cette plage.
8.  Définissez l’attribut de [**\_ \_ Frame MT MF**](mf-mt-frame-rate-attribute.md) sur le type de média pour spécifier la fréquence d’images souhaitée.
9.  Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) avec le type de média modifié.

L’exemple suivant définit la fréquence d’images égale à la fréquence d’images maximale prise en charge par l’appareil :


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



