---
title: Méthodes ID2D1Geometry paver
description: Crée un ensemble de triangles enroulés dans le sens horaire qui couvrent la géométrie après avoir été transformés à l'aide de la matrice spécifiée et aplatis à l'aide de la tolérance spécifiée.
ms.assetid: 4e0af188-d14b-43c0-be11-16577f054b90
keywords:
- Méthodes paver Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 060fc42dddd7642f021d073b8addbe089d031393
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112894"
---
# <a name="id2d1geometrytessellate-methods"></a>ID2D1Geometry :: paver, méthodes

Crée un ensemble de triangles enroulés dans le sens horaire qui couvrent la géométrie après avoir été transformés à l'aide de la matrice spécifiée et aplatis à l'aide de la tolérance spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                    | Description                                                                                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Paver (D2D1 \_ Matrix \_ matrice \_ F \* , ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__id2d1tessellationsink))             | Crée un ensemble de triangles enroulés dans le sens des aiguilles d’une montre qui couvrent la géométrie après qu’elle a été transformée à l’aide de la matrice spécifiée et aplatie à l’aide de la tolérance par défaut. <br/>   |
| [**Paver (D2D1 \_ Matrix \_ matrice \_ F&, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_id2d1tessellationsink))              | Crée un ensemble de triangles enroulés dans le sens des aiguilles d’une montre qui couvrent la géométrie après qu’elle a été transformée à l’aide de la matrice spécifiée et aplatie à l’aide de la tolérance par défaut. <br/>   |
| [**Paver (D2D1 \_ Matrix \_ matrice \_ F \* , float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_float_id2d1tessellationsink)) | Crée un ensemble de triangles enroulés dans le sens horaire qui couvrent la géométrie après avoir été transformés à l'aide de la matrice spécifiée et aplatis à l'aide de la tolérance spécifiée. <br/> |
| [**Paver (D2D1 \_ Matrix \_ matrice \_ F&, float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__float_id2d1tessellationsink))  | Crée un ensemble de triangles enroulés dans le sens horaire qui couvrent la géométrie après avoir été transformés à l'aide de la matrice spécifiée et aplatis à l'aide de la tolérance spécifiée.<br/>  |



## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment utiliser paver pour créer un ensemble de triangles enroulés dans le sens des aiguilles d’une montre qui couvre la géométrie.


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
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

 

