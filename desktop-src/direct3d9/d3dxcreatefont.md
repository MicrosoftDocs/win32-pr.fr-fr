---
description: Crée un objet de police pour un appareil et une police.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: D3DXCreateFont, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762193"
---
# <a name="d3dxcreatefont-function"></a>D3DXCreateFont fonction)

Crée un objet de police pour un appareil et une police.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’appareil à associer à l’objet font.

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

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Jeu de caractères de la police.

</dd> <dt>

*OutputPrecision* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie comment Windows doit tenter de faire correspondre les tailles de police et les caractéristiques souhaitées avec les polices réelles. Utilisez \_ TT \_ uniquement \_ precis par exemple, pour vous assurer que vous recevez toujours une police TrueType.

</dd> <dt>

*Qualité* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie comment Windows doit correspondre à la police souhaitée avec une police réelle. Elle s’applique uniquement aux polices Raster et ne doit pas affecter les polices TrueType.

</dd> <dt>

*PitchAndFamily* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de la famille et de la hauteur.

</dd> <dt>

*pFacename* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de la police. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*ppFont* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXFONT**](id3dxfont.md)\***

Retourne un pointeur vers une interface [**ID3DXFont**](id3dxfont.md) représentant l’objet de police créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La création d’un objet ID3DXFont nécessite que l’appareil prenne en charge la couleur 32 bits.

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontA, car les chaînes ANSI sont utilisées.

Si vous souhaitez plus d’informations sur les paramètres de police, consultez [la police logique](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
