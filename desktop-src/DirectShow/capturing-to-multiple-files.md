---
description: Capture dans plusieurs fichiers
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Capture dans plusieurs fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108894"
---
# <a name="capturing-to-multiple-files"></a><span data-ttu-id="3189a-103">Capture dans plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="3189a-103">Capturing to Multiple Files</span></span>

<span data-ttu-id="3189a-104">Une fois que vous avez capturé une vidéo dans un fichier, vous pouvez basculer vers un nouveau fichier en arrêtant le graphique et en définissant le nom de fichier dans le filtre du [writer de fichier](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3189a-104">After you have captured some video to a file, you can switch to a new file by stopping the graph and setting the file name on the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="3189a-105">Appelez la méthode [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) sur le writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="3189a-105">Call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method on the File Writer.</span></span> <span data-ttu-id="3189a-106">Vous pouvez obtenir un pointeur vers l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) lorsque vous générez le graphique, par le biais du paramètre *pSink* de la méthode SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="3189a-106">You can get a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface when you build the graph, through the *pSink* parameter of the SetOutputFileName method.</span></span> <span data-ttu-id="3189a-107">Le code suivant illustre comment procéder :</span><span class="sxs-lookup"><span data-stu-id="3189a-107">The following code shows how to do this:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3189a-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3189a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3189a-109">Capture vidéo dans un fichier</span><span class="sxs-lookup"><span data-stu-id="3189a-109">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



