---
title: Méthodes ID2D1Geometry ComputePointAtLength
description: Calcule le vecteur de point et de tangente à la distance spécifiée le long de la géométrie \ 160 ;.
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- Méthodes ComputePointAtLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5b49be0b5a17dd828c9bd86ca41b4a3ff115f47a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525662"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a>ID2D1Geometry :: ComputePointAtLength, méthodes

Calcule le vecteur de point et de tangente à la distance spécifiée le long de la géométrie.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                        | Description                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ matrice \_ F&, d2d1 \_ point \_ 2F \* , d2d1 \_ point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))              | Calcule le vecteur point et tangent à la distance spécifiée le long de la géométrie après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance par défaut.<br/>   |
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ matrice \_ F \* , d2d1 \_ point \_ 2F \* , d2d1 \_ point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))             | Calcule le vecteur point et tangent à la distance spécifiée le long de la géométrie après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance par défaut.<br/>   |
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ matrice \_ F&, float, d2d1 \_ point \_ 2F \* , d2d1 \_ point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))  | Calcule le vecteur point et tangent à la distance spécifiée le long de la géométrie après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance spécifiée.<br/> |
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ matrice \_ F \* , float, d2d1 \_ point \_ 2F \* , d2d1 \_ point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f)) | Calcule le vecteur point et tangent à la distance spécifiée le long de la géométrie après qu’il a été transformé par la matrice spécifiée et aplati à l’aide de la tolérance spécifiée.<br/> |



## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment utiliser **ComputePointAtLength** pour calculer le vecteur de point et de tangente à la distance spécifiée le long de la géométrie.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

