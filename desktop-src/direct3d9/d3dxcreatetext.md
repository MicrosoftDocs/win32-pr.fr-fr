---
description: Crée un maillage contenant le texte spécifié, à l’aide de la police associée au contexte de périphérique.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: D3DXCreateText, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538336"
---
# <a name="d3dxcreatetext-function"></a>D3DXCreateText fonction)

Crée un maillage contenant le texte spécifié, à l’aide de la police associée au contexte de périphérique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers l’appareil qui a créé le maillage.

</dd> <dt>

*HDC* \[ dans\]
</dt> <dd>

Type : **HDC**

Contexte de périphérique, contenant la police de sortie. La police sélectionnée par le contexte de périphérique doit être une police TrueType.

</dd> <dt>

*pText* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le texte à générer. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*Écart* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Écart de corde maximal à partir des contours de police TrueType.

</dd> <dt>

*Extrusion* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Quantité d’extrusion du texte dans l’axe z négatif.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Pointeur vers le maillage retourné.

</dd> <dt>

*ppAdjacency* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers une mémoire tampon qui contient des informations d’adjacence. Peut avoir la **valeur null**.

</dd> <dt>

*pGlyphMetrics* \[ à\]
</dt> <dd>

Type : **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Pointeur vers un tableau de structures [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) qui contiennent les données de métrique de glyphe. Chaque élément contient des informations sur la position et l’orientation du glyphe correspondant dans la chaîne. Le nombre d’éléments dans le tableau doit être égal au nombre de caractères de la chaîne. Notez que l’origine dans chaque structure n’est pas relative à la chaîne entière, mais qu’elle est relative à cette cellule de caractère. Pour calculer l’intégralité du cadre englobant, ajoutez l’incrément pour chaque glyphe tout en parcourant la chaîne. Si vous n’êtes pas concerné par les tailles de glyphe, définissez ce paramètre sur la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextA, car les chaînes ANSI sont utilisées.

Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de dessin de forme](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
