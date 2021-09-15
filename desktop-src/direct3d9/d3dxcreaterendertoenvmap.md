---
description: Crée un mappage d’environnement de rendu.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: D3DXCreateRenderToEnvMap, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526080"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>D3DXCreateRenderToEnvMap fonction)

Crée un mappage d’environnement de rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , qui est l’appareil à associer à la surface de rendu.

</dd> <dt>

*Taille* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Taille de la surface de rendu.

</dd> <dt>

*Miplevels a* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de niveaux de mipmap.

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Membre du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le format de pixel de la carte d’environnement.

</dd> <dt>

*DepthStencil* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, la surface de rendu prend en charge une surface de stencil de profondeur. Dans le cas contraire, ce membre est défini sur **false**.

</dd> <dt>

*DepthStencilFormat* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Si DepthStencil a la valeur **true**, ce paramètre est un membre du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le format de stencil de profondeur de la carte d’environnement.

</dd> <dt>

*ppRenderToEnvMap* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Adresse d’un pointeur vers une interface [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) qui représente le mappage d’environnement de rendu créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
