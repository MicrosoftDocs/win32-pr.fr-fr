---
title: Comment énumérer des adaptateurs
description: Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour énumérer les cartes graphiques disponibles sur un ordinateur.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa74a41f95095c4de9ad58615c5b860153c72d1fcd706286b295653a8004d187
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098254"
---
# <a name="how-to-enumerate-adapters"></a>Comment : énumérer des adaptateurs

Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour énumérer les cartes graphiques disponibles sur un ordinateur. Direct3D 10 et 11 peuvent utiliser DXGI pour énumérer les adaptateurs.

En général, vous devez énumérer les adaptateurs pour les raisons suivantes :

-   Pour déterminer le nombre de cartes graphiques installées sur un ordinateur.
-   Pour vous aider à choisir la carte à utiliser pour créer un appareil Direct3D.
-   Pour récupérer un objet [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) que vous pouvez utiliser pour récupérer les fonctionnalités de l’appareil.

**Pour énumérer des adaptateurs**

1.  Créez un objet [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) en appelant la fonction [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) . L’exemple de code suivant montre comment initialiser un objet **IDXGIFactory** .
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Énumérez chaque adaptateur en appelant la méthode [**IDXGIFactory :: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) . Le paramètre *adapter* vous permet de spécifier un numéro d’index de base zéro de l’adaptateur à énumérer. Si aucun adaptateur n’est disponible à l’index spécifié, la méthode retourne l' [**\_ erreur dxgi \_ \_ introuvable**](/windows/desktop/direct3ddxgi/dxgi-error).

    L’exemple de code suivant montre comment énumérer les adaptateurs sur un ordinateur.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

L’exemple de code suivant montre comment énumérer tous les adaptateurs d’un ordinateur.

> [!Note]  
> Pour Direct3D 11,0 et versions ultérieures, nous recommandons que les applications utilisent toujours [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) et [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) à la place.

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 