---
description: Identifie les matrices de transformation suivantes qui peuvent être utilisées pour fusionner des vertex à l’aide de la matrice correspondante et une valeur de poids de fusion (bêta) spécifiée au format de vertex.
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: D3DTS_WORLDn (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7026308192f43b7290dedcb9572772c9eda45acdc87d018480bd59202a2dc2df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119399"
---
# <a name="d3dts_worldn"></a>D3DTS \_ worldn

Identifie les matrices de transformation suivantes qui peuvent être utilisées pour fusionner des vertex à l’aide de la matrice correspondante et une valeur de poids de fusion (bêta) spécifiée au format de vertex.

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a>Remarques

Ces macros sont fournies pour faciliter le portage d’applications existantes vers Direct3D 9.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
