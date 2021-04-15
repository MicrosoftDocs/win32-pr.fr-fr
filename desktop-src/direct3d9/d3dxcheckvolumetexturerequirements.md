---
description: Vérifie les paramètres de création de texture de volume.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: D3DXCheckVolumeTextureRequirements, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394152"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a>D3DXCheckVolumeTextureRequirements fonction)

Vérifie les paramètres de création de texture de volume.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
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

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers la largeur demandée en pixels, ou **null**. Retourne la taille corrigée.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers la hauteur demandée en pixels, ou **null**. Retourne la taille corrigée.

</dd> <dt>

*pDepth* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers la profondeur demandée en pixels, ou **null**. Retourne la taille corrigée.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de niveaux de mipmap demandés, ou **null**. Retourne le nombre corrigé de niveaux de mipmap.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Actuellement non utilisé, affectez la valeur 0 à.

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)\***

Pointeur vers un membre du type énuméré [D3DFORMAT](d3dformat.md) . Spécifie le format de pixel souhaité, ou **null**. Retourne le format corrigé.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture du volume doit être placée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Si les paramètres de cette fonction ne sont pas valides, cette fonction retourne les paramètres corrigés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
