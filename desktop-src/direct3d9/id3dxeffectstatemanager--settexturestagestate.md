---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de l’étape de texture.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'ID3DXEffectStateManager :: SetTextureStageState, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538346"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a>ID3DXEffectStateManager :: SetTextureStageState, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de l’étape de texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Stage* \[in\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Étape à laquelle la texture est assignée. Il s’agit de la valeur d’index dans [**IDirect3DDevice9 :: SetTexture**](/windows/desktop/api) ou [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*Type* \[ dans\]
</dt> <dd>

Type : **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**

Définit le type d’opération que doit effectuer une étape de texture. Consultez [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Il peut s’agir d’une opération ([**D3DTEXTUREOP**](./d3dtextureop.md)) ou d’une valeur d’argument ([D3DTA](d3dta.md)), en fonction de ce qui est choisi pour le type.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
