---
title: Méthodes d’élargissement ID2D1Geometry
description: Élargit la géométrie par le trait spécifié et écrit le résultat dans un ID2D1SimplifiedGeometrySink.
ms.assetid: c951ab85-7980-41e3-95c4-291d2fb046c8
keywords:
- Méthodes étendues Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 73a1ce3f90192f49a719a92d80f448694ce43235
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112889"
---
# <a name="id2d1geometrywiden-methods"></a>ID2D1Geometry :: Widening, méthodes

Élargit la géométrie par le trait spécifié et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                          | Description                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Widening (FLOAT, ID2D1StrokeStyle \* , d2d1 \_ Matrix \_ matrice \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))             | Élargit la géométrie par le trait spécifié et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance par défaut.<br/>   |
| [**Widening (FLOAT, ID2D1StrokeStyle \* , d2d1 \_ Matrix \_ matrice \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))              | Élargit la géométrie par le trait spécifié et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance par défaut.<br/>   |
| [**Widening (FLOAT, ID2D1StrokeStyle \* , d2d1 \_ Matrix \_ matrice \_ F \* , float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Élargit la géométrie par le trait spécifié et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance spécifiée.<br/> |
| [**Widening (FLOAT, ID2D1StrokeStyle \* , d2d1 \_ Matrix \_ matrice \_ F&, float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))  | Élargit la géométrie par le trait spécifié et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance spécifiée.<br/> |



## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment utiliser **Widening** pour élargir la géométrie par le trait spécifié, puis écrire le résultat dans un objet [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) .


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

 

