---
description: Vérifie les paramètres de création de texture de cube.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: D3DXCheckCubeTextureRequirements, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762350"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a>D3DXCheckCubeTextureRequirements fonction)

Vérifie les paramètres de création de texture de cube.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du cube.

</dd> <dt>

*psize* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers la largeur et la hauteur demandées en pixels, ou **null**. Retourne la taille corrigée.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de niveaux de mipmap demandés, ou **null**. Retourne le nombre corrigé de niveaux de mipmap.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou D3DUSAGE \_ RENDERTARGET. L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu. La ressource peut ensuite être transmise au paramètre pNewRenderTarget de la méthode [**SetRenderTarget**](/windows/desktop/api) . Si D3DUSAGE \_ RENDERTARGET est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)\***

Pointeur vers un membre du type énuméré [D3DFORMAT](d3dformat.md) . Spécifie le format de pixel souhaité, ou **null**. Retourne le format corrigé.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Si les paramètres de cette fonction ne sont pas valides, cette fonction retourne les paramètres corrigés.

Les textures de cube diffèrent des autres surfaces dans le fait qu’il s’agit de collections de surfaces. Pour appeler [**SetRenderTarget**](/windows/desktop/api) avec une texture de cube, vous devez sélectionner un visage individuel à l’aide de [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) et passer la surface résultante à **SetRenderTarget**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
