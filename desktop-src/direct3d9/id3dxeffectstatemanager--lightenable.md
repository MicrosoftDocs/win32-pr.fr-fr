---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour activer/désactiver une lumière.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'ID3DXEffectStateManager :: méthode éclaircie (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211846"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a>ID3DXEffectStateManager :: méthode éclaircie

Fonction de rappel qui doit être implémentée par un utilisateur pour activer/désactiver une lumière.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de base zéro de la lumière. Il s’agit du même index dans [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*Activer* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

True pour activer la lumière ; sinon, false.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel de l’état d’effet dynamique (tel que [**IDirect3DDevice9 :: Eclaircir**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
