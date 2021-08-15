---
description: Définit les dimensions de la fenêtre d’une surface de cible de rendu sur laquelle un projet de volume 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: D3DVIEWPORT9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 40162e4350e5a68670023701f1cdae973fb8a7bac3a6d4f5c301136c4e8c2702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527265"
---
# <a name="d3dviewport9-structure"></a>D3DVIEWPORT9, structure

Définit les dimensions de la fenêtre d’une surface de cible de rendu sur laquelle un projet de volume 3D.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a>Membres

<dl> <dt>

**X**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée de pixels de l’angle supérieur gauche de la fenêtre d’affichage sur la surface de rendu-cible. À moins que vous ne souhaitiez effectuer un rendu sur un sous-ensemble de la surface, ce membre peut être défini sur 0.

</dd> <dt>

**O**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordonnée de pixels de l’angle supérieur gauche de la fenêtre d’affichage sur la surface de rendu-cible. À moins que vous ne souhaitiez effectuer un rendu sur un sous-ensemble de la surface, ce membre peut être défini sur 0.

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur de la dimension du volume du clip, en pixels. À moins que vous ne soyez rendu qu’à un sous-ensemble de la surface, ce membre doit être défini sur la dimension de largeur de la surface de la cible de rendu.

</dd> <dt>

**Height**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimension de hauteur du volume du clip, en pixels. À moins d’être rendu uniquement à un sous-ensemble de la surface, ce membre doit être défini sur la dimension de hauteur de la surface de la cible de rendu.

</dd> <dt>

**MinZ**
</dt> <dd>

Type : **float**

</dd> <dd>

Avec MaxZ, valeur décrivant la plage de valeurs de profondeur dans laquelle une scène doit être rendue, les valeurs minimales et maximales du volume de clip. La plupart des applications définissent cette valeur sur 0,0. Le découpage est effectué après l’application de la matrice de projection.

</dd> <dt>

**MaxZ**
</dt> <dd>

Type : **float**

</dd> <dd>

Avec MinZ, valeur décrivant la plage de valeurs de profondeur dans laquelle une scène doit être rendue, les valeurs minimales et maximales du volume de clip. La plupart des applications définissent cette valeur sur 1,0. Le découpage est effectué après l’application de la matrice de projection.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les membres X, Y, Width et Height décrivent la position et les dimensions de la fenêtre d’affichage sur la surface de rendu-cible. En règle générale, les applications sont rendues sur l’ensemble de la surface cible. lors du rendu sur une surface 640 x 480, ces membres doivent être respectivement 0, 0, 640 et 480. MinZ et MaxZ sont généralement définis sur 0,0 et 1,0, mais peuvent être définis sur d’autres valeurs pour obtenir des effets spécifiques. Par exemple, vous pouvez les définir à la fois sur 0,0 pour forcer le système à restituer les objets au premier plan d’une scène, ou les deux à 1,0 pour forcer les objets en arrière-plan.

Lorsque les paramètres de la fenêtre d’affichage d’un appareil changent (en raison d’un appel à la méthode [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), le pilote crée une nouvelle matrice de transformation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
