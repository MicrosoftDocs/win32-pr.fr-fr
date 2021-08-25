---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un code de Commission.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'ID3DXEffectStateManager :: SetFVF, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 828f6873ed9bf48de6a02d4195fdd1fa9d2bc39f99da1f8906fd8a2c53075cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026409"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a>ID3DXEffectStateManager :: SetFVF, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir un code de Commission.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commission* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Constante du prix de la Commission, qui détermine comment interpréter les données de vertex. Consultez [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
