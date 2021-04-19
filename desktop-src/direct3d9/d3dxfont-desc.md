---
description: Définit les attributs d’une police.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Structure D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527105"
---
# <a name="d3dxfont_desc-structure"></a>D3DXFONT \_ desc, structure

Définit les attributs d’une police.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Height**
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur, en unités logiques, de la cellule de caractère ou du caractère de la police.

</dd> <dt>

**Width**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur, en unités logiques, des caractères de la police.

</dd> <dt>

**Poids**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Poids de la police dans la plage comprise entre 0 et 1000.

</dd> <dt>

**Miplevels a**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre de niveaux MIP demandés. Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée. Si la valeur est 1, l’espace de texture est mappé de manière identique à l’espace à l’écran.

</dd> <dt>

**Italique**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Affectez la valeur **true** à une police en italique.

</dd> <dt>

**CharSet**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Jeu de caractères.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Précision de sortie. La précision de sortie définit la précision selon laquelle la sortie doit correspondre à la hauteur de police, à la largeur, à l’orientation des caractères, à l’échappement, au tangage et au type de police demandés.

</dd> <dt>

**Qualité**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualité de sortie.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Type : **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur et largeur de la police.

</dd> <dt>

**FaceName**
</dt> <dd>

Type : **TCHAR**

</dd> <dd>

Chaîne ou caractères se terminant par un caractère null qui spécifie le nom de la police de la police. La longueur de la chaîne ne doit pas dépasser 32 caractères, y compris le caractère null de fin. Si FaceName est une chaîne vide, la première police qui correspond aux autres attributs spécifiés sera utilisée. Si les paramètres du compilateur requièrent Unicode, le type de données TCHAR correspond à WCHAR ; dans le cas contraire, le type de données correspond à CHAR. Consultez la section Notes.

</dd> </dl>

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également le type de structure. Si Unicode est défini, le \_ type de structure D3DXFONT DESC correspond à un DESCW D3DXFONT \_ ; sinon, le type de structure est résolu en D3DXFONT \_ DESCA.

Les valeurs possibles des membres ci-dessus sont fournies dans la structure GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
