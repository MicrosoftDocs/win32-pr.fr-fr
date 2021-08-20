---
description: capture vidéo sur un fichier multimédia Windows
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: capture vidéo sur un fichier multimédia Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3268d3a3df4a24c5836dba81f7ef4cf0b872907f09367d3212d27c38c0dd4414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158702"
---
# <a name="capturing-video-to-a-windows-media-file"></a>capture vidéo sur un fichier multimédia Windows

pour capturer une vidéo et l’encoder dans un fichier Windows Media Video (WMV), connectez le code confidentiel de capture au filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) , comme indiqué dans le diagramme suivant.

![graphique de capture Windows Media](images/vidcap03.png)

Le moyen le plus simple de créer ce graphique est de spécifiez MEDIASUBTYPE \_ ASF dans la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



la valeur MEDIASUBTYPE \_ Asf indique à l’Graph de Capture que le générateur utilise le filtre d’enregistreur asf WM comme récepteur de fichiers. le générateur de Graph de Capture crée le filtre, l’ajoute au graphique et appelle [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) pour définir le nom du fichier de sortie. Elle retourne un pointeur vers le filtre en tant que paramètre sortant (


```
pASFWriter
```



dans l’exemple précédent).

utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) sur le Writer WM ASF pour définir le profil de média Windows. Vous devez effectuer cette opération avant de connecter des broches sur le writer WM ASF.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Pour plus d’informations sur la définition du profil, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).

Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre de capture à l’enregistreur ASF :


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



chaque broche d’entrée sur le filtre de l’enregistreur ASF WM correspond à un flux dans le profil de média Windows. Vous devez connecter chaque code confidentiel afin que le contenu du fichier corresponde au profil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



