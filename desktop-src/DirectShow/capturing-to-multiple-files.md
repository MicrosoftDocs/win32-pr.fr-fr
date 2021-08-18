---
description: Capture dans plusieurs fichiers
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Capture dans plusieurs fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ce7a1b4b91a0f78031a661e2c2e10895b4a21b1cfb068ca505429468a3af1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017577"
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

 

 



