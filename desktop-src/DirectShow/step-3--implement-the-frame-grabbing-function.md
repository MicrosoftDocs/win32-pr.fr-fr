---
description: Étape 3 implémentation de la fonction Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Étape 3 implémentation de la fonction Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75410c48765e9437cd328a220ccbecf2c207bdaae5242a9e41060bc13fa02eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904092"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Étape 3 : implémenter la fonction Frame-Grabbing

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Cette rubrique est l’étape 3 de [saisie d’un cadre d’affiche](grabbing-a-poster-frame.md).

L’étape suivante consiste à implémenter la fonction GetBitmap, qui utilise le détecteur de média pour saisir une image postérisée. À l’intérieur de cette fonction, procédez comme suit :

1.  Créez le détecteur de média.
2.  Spécifiez un fichier multimédia.
3.  Examinez chaque flux dans le fichier. S’il s’agit d’un flux vidéo, récupérez les dimensions natives de la vidéo.
4.  Obtenez un cadre d’affiche, en spécifiant l’heure de recherche et la dimension cible.

Créez l’objet de détecteur de média en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Spécifiez un nom de fichier à l’aide de la méthode [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) . Cette méthode prend un paramètre **BSTR** .


```C++
hr = pDet->put_Filename(bstrFilename);
```



Obtient le nombre de flux et parcourt en boucle chaque flux vérifiant le type de média. La méthode [**IMediaDet :: obtenir \_ OutputStreams**](imediadet-get-outputstreams.md) récupère le nombre de flux, tandis que la méthode [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md) spécifie le flux à examiner. Quittez la boucle sur le premier flux vidéo.


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



Si aucun flux vidéo n’a été trouvé, la fonction se termine.

Dans le code précédent, la méthode [**IMediaDet :: obten \_ StreamType**](imediadet-get-streamtype.md) retourne simplement le GUID du type principal. Cela est pratique si vous n’avez pas besoin d’examiner le type de support complet. Toutefois, pour obtenir les dimensions de la vidéo, il est nécessaire d’examiner le bloc de format, ce qui signifie que le type de support complet est nécessaire. Vous pouvez récupérer cela en appelant la méthode [**IMediaDet :: obtenir \_ StreamMediaType**](imediadet-get-streammediatype.md) , qui remplit une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Le détecteur de média convertit tous les flux vidéo au format non compressé, avec un bloc de format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



La méthode [**obtenir \_ StreamMediaType**](imediadet-get-streammediatype.md) alloue le bloc de format, que l’appelant doit libérer. Cet exemple utilise la fonction [**FreeMediaType**](freemediatype.md) de la bibliothèque de classes de base.

Vous êtes maintenant prêt à recevoir le cadre de l’affiche. Tout d’abord, appelez la méthode [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) avec un pointeur **null** pour la mémoire tampon :


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Cet appel retourne la taille de mémoire tampon requise dans le paramètre *lSize* . Le premier paramètre spécifie le temps de flux à rechercher ; Cet exemple utilise l’heure zéro. Pour la largeur et la hauteur, cet exemple utilise les dimensions Native Video obtenues précédemment. Si vous spécifiez d’autres valeurs, le détecteur de média étire le bitmap pour qu’il corresponde.

Si la méthode est réussie, allouez la mémoire tampon et rappelez [**GetBitmapBits**](imediadet-getbitmapbits.md) :


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



Voici la fonction complète, avec une meilleure gestion des erreurs.


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



Suivant : [étape 4 : dessiner l’image bitmap sur la zone cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Saisie d’un cadre d’affiche](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
