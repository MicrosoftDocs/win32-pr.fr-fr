---
title: Méthodes ID2D1Geometry CompareWithGeometry
description: Décrit l’intersection entre cette géométrie et la géométrie spécifiée.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Méthodes CompareWithGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: eee64e51d4717a9fe0983be849c78f99602cac9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112937"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>ID2D1Geometry :: CompareWithGeometry, méthodes

Décrit l’intersection entre cette géométrie et la géométrie spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                            | Description                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ matrice \_ F&, \_ relation Geometry d2d1 \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Décrit l’intersection entre cette géométrie et la géométrie spécifiée. La comparaison est effectuée à l’aide de la tolérance d’aplatissement par défaut.<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ matrice \_ F \* , d2d1 \_ Geometry \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Décrit l’intersection entre cette géométrie et la géométrie spécifiée. La comparaison est effectuée à l’aide de la tolérance d’aplatissement par défaut.<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ matrice \_ F&, float, d2d1 \_ Geometry \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Décrit l’intersection entre cette géométrie et la géométrie spécifiée. La comparaison est effectuée à l’aide de la tolérance d’aplatissement spécifiée.<br/>    |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ matrice \_ F \* , float, d2d1 \_ Geometry \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Décrit l’intersection entre cette géométrie et la géométrie spécifiée. La comparaison est effectuée à l’aide de la tolérance d’aplatissement spécifiée.<br/> |



## <a name="remarks"></a>Notes

Lors de l’interprétation de la valeur de *relation* retournée, il est important de se souvenir que la [**relation de géométrie de d2d1 membre \_ \_ \_ est \_ contenue**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) dans le type d’énumération de **\_ \_ relation Geometry d2d1** signifie que cette géométrie est contenue dans *inputGeometry*, et non que cette géométrie contient *inputGeometry*.

Pour plus d’informations sur la façon d’interpréter d’autres valeurs de retour possibles, consultez [**\_ \_ relation Geometry d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

