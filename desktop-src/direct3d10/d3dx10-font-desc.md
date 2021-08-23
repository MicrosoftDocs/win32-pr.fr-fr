---
description: Définit les attributs de police.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Structure D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: f3ee6dea032475eb94a723229751d9523c12d118f7319da8f0296cc8c8c42a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634949"
---
# <a name="d3dx10_font_desc-structure"></a>Structure de la \_ police d3dx10 \_

Définit les attributs de police.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
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

Nombre de niveaux de mipmap demandés. Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée. Si la valeur est 1, l’espace de texture est mappé de manière identique à l’espace à l’écran.

</dd> <dt>

**Italique**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Affectez la valeur **true** à une police en italique.

</dd> <dt>

**Caractères**
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

**FaceName \[ LF- \_ face\]**
</dt> <dd>

Type : **TCHAR**

</dd> <dd>

Chaîne terminée par le caractère NULL qui spécifie le nom de la police de la police. La longueur de la chaîne ne doit pas dépasser 32 caractères, y compris le caractère **null** de fin. Si FaceName est une chaîne vide, la première police qui correspond aux autres attributs spécifiés sera utilisée. Si les paramètres du compilateur requièrent Unicode, le type de données TCHAR correspond à WCHAR ; dans le cas contraire, le type de données correspond à CHAR. Consultez la section Notes.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également le type de structure. Si Unicode est défini, le \_ type de \_ structure Description de la police d3dx10 correspond à un \_ DESCW de police d3dx10 ; dans \_ le cas contraire, le type de structure est résolu en une \_ police d3dx10 \_ DESCA.

Les valeurs possibles des membres ci-dessus sont fournies dans la structure GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
