---
description: Fonction D3DXSphereBoundProbe (D3DX9Mesh. h)-détermine si un rayon croise le volume du cadre englobant d’une sphère.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: D3DXSphereBoundProbe, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2d3ea263d7ad8bc50b936fd1010c352c0c01783
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922467"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>D3DXSphereBoundProbe, fonction (D3DX9Mesh. h)

Détermine si un rayon croise le volume du cadre englobant d’une sphère.

## <a name="syntax"></a>Syntaxe


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCenter* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Pointeur vers une structure [**D3DXVECTOR3**](d3dxvector3.md) , en spécifiant la coordonnée centrale de la sphère.

</dd> <dt>

*Rayon* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Rayon de la sphère.

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

## <a name="return-value"></a>Valeur de retour

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le rayon croise le volume du cadre englobant de la sphère. Sinon, retourne **false**.

## <a name="remarks"></a>Notes

**D3DXSphereBoundProbe** détermine si le rayon croise le volume du cadre englobant de la sphère, pas seulement la surface de la sphère.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
