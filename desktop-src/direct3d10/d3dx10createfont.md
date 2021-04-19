---
description: Crée un objet de police pour un appareil et une police. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser DirectWrite et la bibliothèque DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: D3DX10CreateFont, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538343"
---
# <a name="d3dx10createfont-function"></a>D3DX10CreateFont fonction)

Crée un objet de police pour un appareil et une police.

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser [DirectWrite](../directwrite/direct-write-portal.md) et la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Pointeur vers une interface ID3D10Device, l’appareil à associer à l’objet font.

</dd> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Type : **[ **int**](../winprog/windows-data-types.md)**

Hauteur des caractères dans les unités logiques.

</dd> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur des caractères en unités logiques.

</dd> <dt>

*Poids* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Épaisseur du caractère. Un exemple est le gras.

</dd> <dt>

*Miplevels a* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de niveaux de mipmap.

</dd> <dt>

*Italique* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

True pour la police en italique ; sinon, false.

</dd> <dt>

*Jeu* \[ de caractères dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Jeu de caractères de la police.

</dd> <dt>

*OutputPrecision* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Spécifie comment Windows doit tenter de faire correspondre les tailles de police et les caractéristiques souhaitées avec les polices réelles. Utilisez \_ TT \_ uniquement \_ precis par exemple, pour vous assurer que vous recevez toujours une police TrueType.

</dd> <dt>

*Qualité* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Spécifie comment Windows doit correspondre à la police souhaitée avec une police réelle. Elle s’applique uniquement aux polices Raster et ne doit pas affecter les polices TrueType.

</dd> <dt>

*PitchAndFamily* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de la famille et de la hauteur.

</dd> <dt>

*pFaceName* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de la police. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*ppFont* \[ à\]
</dt> <dd>

Type : **[ **LPD3DX10FONT**](id3dx10font.md)\***

Retourne un pointeur vers une interface ID3DX10Font représentant l’objet de police créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontA, car les chaînes ANSI sont utilisées.

Si vous souhaitez plus d’informations sur les paramètres de police, consultez [la police logique](/previous-versions//ms533985(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
