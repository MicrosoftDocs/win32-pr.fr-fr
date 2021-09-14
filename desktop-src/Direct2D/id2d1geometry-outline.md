---
title: Méthodes de plan ID2D1Geometry
description: Calcule le contour de la géométrie et écrit le résultat dans un ID2D1SimplifiedGeometrySink.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Méthodes de plan Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 40d4ff1122d4a00e11ea35914f001b6dc9e06e4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112914"
---
# <a name="id2d1geometryoutline-methods"></a>ID2D1Geometry :: Outline, méthodes

Calcule le contour de la géométrie et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                          | Description                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Outline (D2D1 \_ Matrix \_ matrice \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Calcule le contour de la géométrie et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). <br/> |
| [**Outline (D2D1 \_ Matrix \_ matrice \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Calcule le contour de la géométrie et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline (D2D1 \_ Matrix \_ matrice \_ F&, float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Calcule le contour de la géométrie et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline (D2D1 \_ Matrix \_ matrice \_ F \* , float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Calcule le contour de la géométrie et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |



## <a name="remarks"></a>Notes

La méthode [**Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) permet à l’appelant de produire une géométrie avec un remplissage équivalent à la géométrie d’entrée, avec les propriétés supplémentaires suivantes :

-   La géométrie de sortie ne contient aucune intersection transversale ; autrement dit, les segments peuvent toucher, mais ils ne se croisent jamais.
-   Les chiffres les plus à l’extérieur dans la géométrie de sortie sont tous orientés vers le sens inverse.
-   La géométrie de sortie est invariant en mode de remplissage ; autrement dit, le remplissage de la géométrie ne dépend pas du choix du mode de remplissage. Pour plus d’informations sur le mode de remplissage, consultez [**d2d1 \_ Fill \_ mode**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

En outre, la méthode [**Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) peut être utile pour supprimer des parties redondantes de ces géométries afin de simplifier les géométries complexes. Il peut également être utile en association avec [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) pour créer des unions entre plusieurs géométries simultanément.

## <a name="examples"></a>Exemples

Le code suivant montre comment utiliser **Outline** pour construire une géométrie équivalente sans auto-intersections. Elle utilise la tolérance d’aplatissement par défaut et ne doit donc pas être utilisée avec de très petites géométries.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

