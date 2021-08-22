---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir une lumière.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'ID3DXEffectStateManager :: SetLight, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 83250450a0510949267ffd52f17e6e9013a646d40229efcf7d5bcc7a396e1b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372079"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a>ID3DXEffectStateManager :: SetLight, méthode

Fonction de rappel qui doit être implémentée par un utilisateur pour définir une lumière.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de base zéro de la lumière. Il s’agit du même index dans [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*pLight* \[ dans\]
</dt> <dd>

Type : **const [**D3DLight9**](d3dlight9.md) \***

Objet Light. Consultez [**D3DLIGHT9**](d3dlight9.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La méthode implémentée par l’utilisateur doit retourner S \_ OK. Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :

-   L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).
-   L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) échouera.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
