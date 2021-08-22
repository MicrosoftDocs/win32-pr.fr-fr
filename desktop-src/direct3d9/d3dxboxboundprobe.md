---
description: Détermine si un rayon croise le volume du cadre englobant d’une zone.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: D3DXBoxBoundProbe, fonction (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 197582c2f404124edd5a49c9d7780ce35cac61b15438a81d120839f283b82373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676389"
---
# <a name="d3dxboxboundprobe-function"></a>D3DXBoxBoundProbe fonction)

Détermine si un rayon croise le volume du cadre englobant d’une zone.

## <a name="syntax"></a>Syntaxe


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMin* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant l’angle inférieur gauche du cadre englobant. Consultez la section Notes.

</dd> <dt>

*pMax* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , décrivant l’angle supérieur droit du cadre englobant. Consultez la section Notes.

</dd> <dt>

*pRayPosition* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la coordonnée d’origine du rayon.

</dd> <dt>

*pRayDirection* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la direction du rayon. Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la zone. Sinon, retourne **false**.

## <a name="remarks"></a>Remarques

**D3DXboxBoundProbe** détermine si le rayon croise le volume du cadre englobant de la zone, pas seulement la surface de la boîte.

Les valeurs passées à **D3DXboxBoundProbe** sont xmin, xmax, ymin, ymax, zmin et Zmax. Ainsi, les éléments suivants définissent les angles du cadre englobant.


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



La profondeur du cadre englobant dans la direction z est zmax-zmin, la direction y est ymax-ymin, et la direction x est Xmax-xmin. Par exemple, avec les vecteurs minimal et maximal suivants, min (-1,-1,-1) et Max (1, 1, 1), le cadre englobant est défini de la manière suivante.


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
