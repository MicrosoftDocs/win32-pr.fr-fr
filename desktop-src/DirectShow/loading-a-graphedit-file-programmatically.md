---
description: Chargement d’un fichier baGraphEdit par programmation
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Chargement d’un fichier baGraphEdit par programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481745"
---
# <a name="loading-a-graphedit-file-programmatically"></a><span data-ttu-id="4ba3f-103">Chargement d’un fichier baGraphEdit par programmation</span><span class="sxs-lookup"><span data-stu-id="4ba3f-103">Loading a GraphEdit File Programmatically</span></span>

<span data-ttu-id="4ba3f-104">Une application peut utiliser l’interface **IPersistStream** pour charger un fichier GraphEdit (. GRF).</span><span class="sxs-lookup"><span data-stu-id="4ba3f-104">An application can use the **IPersistStream** interface to load a GraphEdit (.grf) file.</span></span> <span data-ttu-id="4ba3f-105">Utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4ba3f-105">Use the following code:</span></span>


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> <span data-ttu-id="4ba3f-106">L’appel à **IPersistStream :: Load** dans l’exemple de code précédent peut retourner un code d’erreur ou de réussite DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4ba3f-106">The call to **IPersistStream::Load** in the previous code example can return a DirectShow error or success code.</span></span> <span data-ttu-id="4ba3f-107">Pour obtenir la liste des valeurs de retour possibles, consultez [codes d’erreur et de réussite](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4ba3f-107">For a list of possible return values, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 

<span data-ttu-id="4ba3f-108">Les fichiers GraphEdit sont destinés uniquement à des fins de test et de débogage.</span><span class="sxs-lookup"><span data-stu-id="4ba3f-108">GraphEdit files are intended only for testing and debugging.</span></span> <span data-ttu-id="4ba3f-109">Elles ne sont pas destinées à être utilisées par les applications de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="4ba3f-109">They are not meant for use by end-user applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ba3f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ba3f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ba3f-111">Simulation de la génération de graphiques avec GraphEdit</span><span class="sxs-lookup"><span data-stu-id="4ba3f-111">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="4ba3f-112">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="4ba3f-112">**StgIsStorageFile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[<span data-ttu-id="4ba3f-113">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="4ba3f-113">**StgOpenStorage**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
