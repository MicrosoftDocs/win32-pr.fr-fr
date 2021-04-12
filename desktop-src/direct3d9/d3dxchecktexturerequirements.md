---
description: Vérifie les paramètres de création de texture.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: D3DXCheckTextureRequirements, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211806"
---
# <a name="d3dxchecktexturerequirements-function"></a>D3DXCheckTextureRequirements fonction)

Vérifie les paramètres de création de texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
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

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.

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

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de niveaux de mipmap demandés, ou **null**. Retourne le nombre corrigé de niveaux de mipmap.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

0 ou [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). L’affectation de la valeur D3DUSAGE RENDERTARGET à cet indicateur \_ indique que la surface doit être utilisée comme cible de rendu. La ressource peut ensuite être transmise au paramètre pNewRenderTarget de la méthode [**SetRenderTarget**](/windows/desktop/api) . Si **D3DUSAGE \_ RENDERTARGET** est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

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

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Notes

Si les paramètres de cette fonction ne sont pas valides, cette fonction retourne les paramètres corrigés.

Cette fonction utilise l’heuristique suivante lors de la comparaison des exigences demandées par rapport aux formats disponibles :

-   Ne choisissez pas un format comportant moins de canaux.
-   Évitez les formats [FourCC](d3dformat.md) et 24 bits sauf demande explicite.
-   Essayez de ne pas ajouter de nouveaux canaux.
-   Essayez de ne pas modifier le nombre de bits par canal.
-   Essayez d’éviter la conversion entre les types de formats. Par exemple, évitez de convertir un format ARVB en un format de profondeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
