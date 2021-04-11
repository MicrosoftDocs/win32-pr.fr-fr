---
description: Capture vidéo sur un fichier Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Capture vidéo sur un fichier Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211244"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Capture vidéo sur un fichier Windows Media

Pour capturer une vidéo et l’encoder dans un fichier Windows Media Video (WMV), connectez le code confidentiel de capture au filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) , comme indiqué dans le diagramme suivant.

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



La valeur MEDIASUBTYPE \_ ASF indique au générateur de graphiques de capture d’utiliser le filtre de l’enregistreur ASF WM comme récepteur de fichiers. Le générateur de graphiques de capture crée le filtre, l’ajoute au graphique et appelle [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) pour définir le nom du fichier de sortie. Elle retourne un pointeur vers le filtre en tant que paramètre sortant (


```
pASFWriter
```



dans l’exemple précédent).

Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) sur le writer WM ASF pour définir le profil Windows Media. Vous devez effectuer cette opération avant de connecter des broches sur le writer WM ASF.


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



Chaque broche d’entrée sur le filtre de l’enregistreur ASF WM correspond à un flux dans le profil Windows Media. Vous devez connecter chaque code confidentiel afin que le contenu du fichier corresponde au profil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



