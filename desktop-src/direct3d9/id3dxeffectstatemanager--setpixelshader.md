---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de pixels.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'ID3DXEffectStateManager :: SetPixelShader, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530981"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a>ID3DXEffectStateManager :: SetPixelShader, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de pixels.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pShader* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**

Pointeur vers un objet de nuanceur de pixels. Consultez [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
