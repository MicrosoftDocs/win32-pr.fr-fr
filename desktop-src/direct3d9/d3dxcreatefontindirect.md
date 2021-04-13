---
description: Crée un objet de police indirectement pour un appareil et une police.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: D3DXCreateFontIndirect, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323161"
---
# <a name="d3dxcreatefontindirect-function"></a>D3DXCreateFontIndirect fonction)

Crée un objet de police indirectement pour un appareil et une police.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’appareil à associer à l’objet font.

</dd> <dt>

*pDesc* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFONT \_ desc**](d3dxfont-desc.md) \***

Pointeur vers une structure [**D3DXFONT \_ desc**](d3dxfont-desc.md) , décrivant les attributs de l’objet font à créer. Si les paramètres du compilateur requièrent Unicode, le type de données D3DXFONT \_ desc correspond à D3DXFONT \_ DESCW ; dans le cas contraire, le type de données est résolu en D3DXFONT \_ DESCA. Consultez la section Notes.

</dd> <dt>

*ppFont* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXFONT**](id3dxfont.md)\***

Retourne un pointeur vers une interface [**ID3DXFont**](id3dxfont.md) représentant l’objet de police créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontIndirectW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontIndirectA, car les chaînes ANSI sont utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
