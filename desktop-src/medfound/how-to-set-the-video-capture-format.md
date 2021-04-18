---
description: Un périphérique de capture vidéo peut prendre en charge plusieurs formats de capture. Les formats sont généralement différents selon le type de compression, l’espace colorimétrique (YUV ou RVB), la taille du cadre ou la fréquence d’images.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Comment définir le format de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519056"
---
# <a name="how-to-set-the-video-capture-format"></a>Comment définir le format de capture vidéo

Un périphérique de capture vidéo peut prendre en charge plusieurs formats de capture. Les formats sont généralement différents selon le type de compression, l’espace colorimétrique (YUV ou RVB), la taille du cadre ou la fréquence d’images.

La liste des formats pris en charge est contenue dans le *descripteur de présentation*. Pour plus d’informations, consultez [descripteurs de présentation](presentation-descriptors.md).

Pour énumérer les formats pris en charge :

1.  Créez la source du média pour l’appareil de capture. Consultez [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).
2.  Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source du média pour récupérer le descripteur de présentation.
3.  Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour obtenir le descripteur de flux du flux vidéo.
4.  Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux.
5.  Appelez [**IMFMediaTypeHandler :: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) pour connaître le nombre de formats pris en charge.
6.  Dans une boucle, appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) pour obtenir chaque format. Le format est représenté par un *type de média*. Pour plus d’informations, consultez [Video Media types](video-media-types.md).

L’exemple suivant énumère les formats de capture d’un appareil :


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



La `LogMediaType` fonction utilisée dans cet exemple est indiquée dans la rubrique [Code de débogage du type de média](media-type-debugging-code.md).

Pour définir le format de capture :

1.  Obtenir un pointeur vers l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , comme indiqué dans l’exemple précédent.
2.  Appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) pour connaître le format souhaité, spécifié par index.
3.  Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) pour définir le format.

Si vous ne définissez pas le format de capture, l’appareil utilise son format par défaut.

L’exemple suivant définit le format de capture :


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



L’ordre dans lequel les formats sont retournés dépend de l’appareil. En règle générale, ils sont regroupés tout d’abord par type de compression ou espace colorimétrique. et de la taille d’image la plus petite à la plus grande taille de trame au sein de chaque groupe.

La fréquence d’images est traitée légèrement différemment des autres attributs de format. Pour plus d’informations, consultez [comment définir la fréquence d’images de capture vidéo](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> Dans certains appareils, la liste format contient une entrée dupliquée pour chaque format. Par exemple, si l’appareil prend en charge 15 formats de capture distincts, la liste contiendra 30 entrées. Au sein de chaque paire, l’un des types de média aura [**le \_ \_ type de \_ format \_ de fichier MF MT**](mf-mt-am-format-type-attribute.md) d’attribut égal au **format \_ videoinfo**, et l’autre aura un type de **\_ \_ format de AM \_ \_ MT MF** égal au **format \_ VideoInfo2**. (Ces deux valeurs sont définies dans le fichier d’en-tête UUID. h.) Le deuxième type peut également contenir des informations supplémentaires sur la couleur ([informations sur la couleur étendue](extended-color-information.md)) ou afficher une valeur différente pour l’entrelacement ([**\_ \_ \_ mode entrelacé MF MT**](mf-mt-interlace-mode-attribute.md)). Ces types dupliqués sont disponibles pour prendre en charge les anciennes applications DirectShow. Dans une application Media Foundation, vous devez ignorer le **format \_ videoinfo** type chaque fois qu’un type **\_ VideoInfo2 de format** dupliqué est listé.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



