---
description: Enregistrement d’un graphique de filtre dans un fichier baGraphEdit
ms.assetid: f7eeae3c-506b-484c-8fe5-ddd391af5a59
title: Enregistrement d’un graphique de filtre dans un fichier baGraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5fb24c40f11dbeb5dad8b542f0f152449f8951
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516752"
---
# <a name="saving-a-filter-graph-to-a-graphedit-file"></a><span data-ttu-id="1246b-103">Enregistrement d’un graphique de filtre dans un fichier baGraphEdit</span><span class="sxs-lookup"><span data-stu-id="1246b-103">Saving a Filter Graph to a GraphEdit File</span></span>

<span data-ttu-id="1246b-104">L’exemple de code suivant montre comment enregistrer un graphique de filtre dans un fichier GraphEdit (. GRF).</span><span class="sxs-lookup"><span data-stu-id="1246b-104">The following code example shows how to save a filter graph to a GraphEdit (.grf) file.</span></span> <span data-ttu-id="1246b-105">Cela peut être utile pour déboguer vos applications.</span><span class="sxs-lookup"><span data-stu-id="1246b-105">This can be useful for debugging your applications.</span></span>


```C++
HRESULT SaveGraphFile(IGraphBuilder *pGraph, WCHAR *wszPath) 
{
    const WCHAR wszStreamName[] = L"ActiveMovieGraph"; 
    HRESULT hr;
    
    IStorage *pStorage = NULL;
    hr = StgCreateDocfile(
        wszPath,
        STGM_CREATE | STGM_TRANSACTED | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0, &pStorage);
    if(FAILED(hr)) 
    {
        return hr;
    }

    IStream *pStream;
    hr = pStorage->CreateStream(
        wszStreamName,
        STGM_WRITE | STGM_CREATE | STGM_SHARE_EXCLUSIVE,
        0, 0, &pStream);
    if (FAILED(hr)) 
    {
        pStorage->Release();    
        return hr;
    }

    IPersistStream *pPersist = NULL;
    pGraph->QueryInterface(IID_IPersistStream, (void**)&pPersist);
    hr = pPersist->Save(pStream, TRUE);
    pStream->Release();
    pPersist->Release();
    if (SUCCEEDED(hr)) 
    {
        hr = pStorage->Commit(STGC_DEFAULT);
    }
    pStorage->Release();
    return hr;
}
```



<span data-ttu-id="1246b-106">Par exemple, le code suivant génère un graphique de lecture de fichier et l’enregistre dans un fichier nommé MyGraph. GRF :</span><span class="sxs-lookup"><span data-stu-id="1246b-106">For example, the following code builds a file playback graph and saves it to a file named MyGraph.grf:</span></span>


```C++
void __cdecl main(void)
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    CoInitialize(NULL);
    
    // Create the Filter Graph Manager and render a file.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
        IID_IGraphBuilder, reinterpret_cast<void**>(&pGraph));
    hr = pGraph->RenderFile(L"C:\\Video.avi", NULL);

    if (SUCCEEDED(hr))
    {
        hr = SaveGraphFile(pGraph, L"C:\\MyGraph.grf");
    }
    
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="1246b-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1246b-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1246b-108">Simulation de la génération de graphiques avec GraphEdit</span><span class="sxs-lookup"><span data-stu-id="1246b-108">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="1246b-109">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="1246b-109">**StgCreateDocfile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> </dl>

 

 
