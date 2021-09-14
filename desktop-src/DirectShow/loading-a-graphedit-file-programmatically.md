---
description: Chargement d’un fichier baGraphEdit par programmation
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Chargement d’un fichier baGraphEdit par programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007498"
---
# <a name="loading-a-graphedit-file-programmatically"></a>Chargement d’un fichier baGraphEdit par programmation

Une application peut utiliser l’interface **IPersistStream** pour charger un fichier GraphEdit (. GRF). Utilisez le code suivant :


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
> l’appel à **IPersistStream :: Load** dans l’exemple de code précédent peut retourner un DirectShow code d’erreur ou de réussite. Pour obtenir la liste des valeurs de retour possibles, consultez [codes d’erreur et de réussite](error-and-success-codes.md).

 

Les fichiers GraphEdit sont destinés uniquement à des fins de test et de débogage. Elles ne sont pas destinées à être utilisées par les applications de l’utilisateur final.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[simulation d’Graph génération avec GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgIsStorageFile**](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[**StgOpenStorage**](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
