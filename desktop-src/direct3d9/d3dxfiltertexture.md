---
description: Filtre les niveaux de mipmap d’une texture.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: D3DXFilterTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522958"
---
# <a name="d3dxfiltertexture-function"></a>D3DXFilterTexture fonction)

Filtre les niveaux de mipmap d’une texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBaseTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Pointeur vers une interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) qui représente l’objet de texture à filtrer.

</dd> <dt>

*pPalette* \[ à\]
</dt> <dd>

Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null** pour les formats nonpalettized. Si aucune palette n’est spécifiée, la palette Direct3D par défaut (une palette blanche opaque) est fournie. Consultez la section Notes.

</dd> <dt>

*SrcLevel* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Niveau dont l’image est utilisée pour générer les niveaux suivants. La spécification \_ de la valeur par défaut D3DX pour ce paramètre équivaut à spécifier 0.

</dd> <dt>

*MipFilter* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont le mipmap est filtré. La spécification \_ de la valeur D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ si la taille de la texture est une puissance de deux et le filtre de la zone de filtre D3DX dans le \_ \_ \| \_ \_ cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

Un filtre est appliqué de manière récursive à chaque niveau de texture pour générer le niveau de texture suivant.

L’écriture sur une surface non-niveau zéro de la texture n’entraîne pas la mise à jour du rectangle modifié. Si **D3DXFilterTexture** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur la texture.

Les textures créées dans le pool par défaut (D3DPOOL \_ par défaut) ne peuvent pas être utilisées avec **D3DXFilterTexture** (sauf si elles sont créées avec D3DUSAGE \_ Dynamic), car une opération de verrouillage est nécessaire sur l’objet. Notez que les verrous sont interdits sur les textures dans le pool par défaut (sauf s’ils sont dynamiques).

Pour plus d’informations sur [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consultez le kit de développement Platform SDK. Notez que à compter de DirectX 8,0, le membre peFlags de la structure **PaletteEntry** ne fonctionne pas comme décrit dans le kit de développement logiciel (SDK) de la plateforme. Le membre peFlags est maintenant le canal alpha pour les formats en palette de 8 bits.

Il n’existe qu’une seule fonction de filtrage de texture, mais deux macros qui appellent cette méthode.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
