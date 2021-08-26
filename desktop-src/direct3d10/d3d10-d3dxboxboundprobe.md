---
description: La fonction D3DXBoxBoundProbe (D3DX10math. h) détermine si un rayon croise le volume du cadre englobant d’une zone.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: D3DXBoxBoundProbe, fonction (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae06fa2e42e99dc64a0684844e341f26e30d797e75d3a822aa0b1ddee690703d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028809"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>D3DXBoxBoundProbe, fonction (D3DX10math. h)

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

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), décrivant l’angle inférieur gauche du rectangle englobant. Consultez la section Notes.

</dd> <dt>

*pMax* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , décrivant l’angle supérieur droit du cadre englobant. Consultez la section Notes.

</dd> <dt>

*pRayPosition* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers une structure D3DXVECTOR3, en spécifiant la coordonnée d’origine du rayon.

</dd> <dt>

*pRayDirection* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Pointeur vers une structure D3DXVECTOR3, en spécifiant la direction du rayon. Ce vecteur ne doit pas être (0, 0, 0), mais il n’a pas besoin d’être normalisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la zone. Sinon, retourne **false**.

## <a name="remarks"></a>Remarques

**D3DXBoxBoundProbe** détermine si le rayon croise le volume du cadre englobant de la zone, pas seulement la surface de la boîte.

Les valeurs passées à **D3DXBoxBoundProbe** sont xmin, xmax, ymin, ymax, zmin et Zmax. Ainsi, les éléments suivants définissent les angles du cadre englobant.


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
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête  | D3DX10math. h |
| Bibliothèque | D3DX10. lib  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
