---
description: La création de rapports sur la sollicitation de la mémoire permet à une application Direct3D de déterminer quand sa plage de travail de la mémoire vidéo est devenue trop importante.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Rapport de sollicitation de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dc0df8db30281c6f7225309bdca5edfdbd3759f21a9e61cdc848f534dcce41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723769"
---
# <a name="memory-pressure-reporting"></a>Rapport de sollicitation de la mémoire

La création de rapports sur la sollicitation de la mémoire permet à une application Direct3D de déterminer quand sa plage de travail de la mémoire vidéo est devenue trop importante.

La *sollicitation* de la mémoire est la demande placée sur le sous-système de mémoire par une application. Si une application Direct3D peut utiliser la création de rapports de sollicitation de la mémoire, cette fonctionnalité est particulièrement utile pour les applications qui affichent des vidéos à l’aide de Direct3D. La lecture vidéo tire généralement parti de grandes quantités de mémoire tampon, afin que les frames puissent être décodés à l’avance. Si la mise en mémoire tampon entraîne généralement une lecture plus lisse, elle peut en fait dégrader les performances si la plage de travail devient trop volumineuse, en raison des facteurs suivants :

-   La mémoire peut être expulsée du cache. Dans le pire des cas, cela peut se produire sur chaque image vidéo.
-   Les allocations de mémoire peuvent être placées dans des segments de mémoire non optimaux.

à partir de Windows 7, Direct3D peut signaler des statistiques sur la sollicitation de la mémoire vidéo :

-   Nombre d’octets évincés par le processus sur un intervalle de temps.
-   Quantité de mémoire placée dans des segments de mémoire non optimaux.
-   Une indication approximative de l’efficacité globale des allocations de mémoire placées dans une mémoire non optimale.

Ces informations peuvent aider une application à conserver une plage de travail raisonnable.

## <a name="using-memory-pressure-reporting"></a>Utilisation des rapports de sollicitation de la mémoire

La signalisation de sollicitation de la mémoire utilise l’interface **IDirect3DQuery9** existante pour interroger l’appareil. Un nouveau type de requête a été ajouté à l’énumération **D3DQUERYTYPE** .


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Pour utiliser cette requête, procédez comme suit :

1.  Appelez **IDirect3DDevice9Ex :: CreateQuery** avec l' **indicateur \_ MEMORYPRESSURE D3DQUERYTYPE** . Cette méthode retourne un pointeur vers l’interface **IDirect3DQuery9** .
2.  Appelez **IDirect3DQuery9 :: issue** avec l’indicateur de **\_ début D3DISSUE** pour commencer l’intervalle de mesure.
3.  Appelez **IDirect3DQuery9 :: issue** avec l’indicateur de **\_ fin D3DISSUE** .
4.  Appelez **IDirect3DQuery9 :: GetData** pour obtenir le résultat de la requête. La requête retourne une structure [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

## <a name="example-code"></a>Exemple de code

L’exemple suivant montre deux fonctions qui mesurent la sollicitation de la mémoire. Le premier commence l’intervalle de mesure, tandis que le second extrait les résultats de la mesure.


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 



