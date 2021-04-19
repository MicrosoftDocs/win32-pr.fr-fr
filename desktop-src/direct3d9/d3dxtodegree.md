---
description: Convertit les radians en degrés.
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: D3DXToDegree (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToDegree
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: ad77ea661f4d67318566079aa7c1072fe0f86c91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524850"
---
# <a name="d3dxtodegree"></a>D3DXToDegree

Convertit les radians en degrés.

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a>Paramètres



| Paramètre                                                           | Description                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="radian"></span><span id="RADIAN"></span>correspondantes radians<br/> | Valeur, en radians, à convertir en degrés.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

La macro retourne la valeur en radians en degrés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToRadian**](d3dxtoradian.md)
</dt> <dt>

[D3DX \_ pi](other-d3dx-constants.md)
</dt> </dl>

 

 




