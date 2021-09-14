---
description: Capture dans plusieurs fichiers
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Capture dans plusieurs fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296887"
---
# <a name="capturing-to-multiple-files"></a>Capture dans plusieurs fichiers

Une fois que vous avez capturé une vidéo dans un fichier, vous pouvez basculer vers un nouveau fichier en arrêtant le graphique et en définissant le nom de fichier dans le filtre du [writer de fichier](file-writer-filter.md) . Appelez la méthode [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) sur le writer de fichier. Vous pouvez obtenir un pointeur vers l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) lorsque vous générez le graphique, par le biais du paramètre *pSink* de la méthode SetOutputFileName. Le code suivant illustre comment procéder :


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



