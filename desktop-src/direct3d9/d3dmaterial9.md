---
description: Spécifie les propriétés de matériau.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: D3DMATERIAL9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394156"
---
# <a name="d3dmaterial9-structure"></a>D3DMATERIAL9, structure

Spécifie les propriétés de matériau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>Membres

<dl> <dt>

**Diffus**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valeur spécifiant la couleur diffuse du matériau. Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Ambiant**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valeur spécifiant la couleur ambiante du matériau. Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Spéculaire**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valeur spécifiant la couleur spéculaire du matériau. Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Émissif**
</dt> <dd>

Type : **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valeur spécifiant la couleur émissif du matériau. Consultez [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Power**
</dt> <dd>

Type : **float**

</dd> <dd>

Valeur à virgule flottante spécifiant la netteté des surbrillances spéculaires. Plus la valeur est élevée, plus la mise en surbrillance est nette.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour désactiver les surbrillances spéculaires, affectez la valeur \_ **false** à D3DRS SpecularEnable, à l’aide de [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Il s’agit de l’option la plus rapide car aucune surbrillance spéculaire n’est calculée.

Pour plus d’informations sur l’utilisation du moteur d’éclairage pour calculer l’éclairage spéculaire, consultez [éclairage spéculaire (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9::GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
