---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de rendu.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager :: SetRenderState, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c7d34dae1d0789b80d896b72be7e35420daf587986ac2725e880b81597b15e88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119459619"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>ID3DXEffectStateManager :: SetRenderState, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de rendu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*État* \[ dans\]
</dt> <dd>

Type : **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

État de rendu à définir. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Valeur de l’état de rendu. Consultez [États d’effet (Direct3D 9)](effect-states.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
