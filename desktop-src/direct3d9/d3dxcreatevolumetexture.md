---
description: Crée une texture de volume vide, en ajustant les paramètres d’appel en fonction des besoins.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: D3DXCreateVolumeTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953855"
---
# <a name="d3dxcreatevolumetexture-function"></a>D3DXCreateVolumeTexture fonction)

Crée une texture de volume vide, en ajustant les paramètres d’appel en fonction des besoins.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture du volume.

</dd> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur en pixels. Cette valeur doit être différente de zéro. La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur en pixels. Cette valeur doit être différente de zéro. La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Profondeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Profondeur en pixels. Cette valeur doit être différente de zéro. La dimension maximale prise en charge par un pilote (pour la largeur, la hauteur et la profondeur) est disponible dans MaxVolumeExtent dans [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Miplevels a* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de niveaux MIP demandés. Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou D3DUSAGE \_ dynamique. Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture du volume. La texture de volume retournée peut avoir un format différent de celui spécifié par le format. Les applications doivent vérifier le format de la texture de volume retournée.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture du volume doit être placée.

</dd> <dt>

*ppVolumeTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Adresse d’un pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , représentant l’objet de texture de volume créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

En interne, D3DXCreateVolumeTexture utilise [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) pour ajuster les paramètres d’appel. Par conséquent, les appels à D3DXCreateVolumeTexture aboutissent souvent lorsque les appels à [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) échouent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
