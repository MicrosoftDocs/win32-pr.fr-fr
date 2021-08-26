---
title: Méthodes ID2D1Geometry ComputeArea
description: Calcule la zone de la géométrie.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Méthodes ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 344cb55314c3cafc2e84479944342633c74bd5a35754c9f7a4f6d53a30da58fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044169"
---
# <a name="id2d1geometrycomputearea-methods"></a>ID2D1Geometry :: ComputeArea, méthodes

Calcule la zone de la géométrie.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                      | Description                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance par défaut.<br/>    |
| [**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance par défaut.<br/> |
| [**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance spécifiée.<br/>  |
| [**ComputeArea (D2D1 \_ Matrix \_ matrice \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Calcule la zone de la géométrie après qu’elle a été transformée par la matrice spécifiée et aplatie à l’aide de la tolérance spécifiée.<br/>  |



## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **ComputeArea** pour calculer la zone d’un cercle spécifié (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
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

 

