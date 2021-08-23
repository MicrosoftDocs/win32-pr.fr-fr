---
description: Crée une copie d’un effet.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'ID3DXEffect :: CloneEffect, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ab5ebe2898c1525d3a539121d1e57708c4713df3a06b43bfa41572f0e7b23b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494259"
---
# <a name="id3dxeffectcloneeffect-method"></a>ID3DXEffect :: CloneEffect, méthode

Crée une copie d’un effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à l’effet.

</dd> <dt>

*ppEffect* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) contenant l’effet cloné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

> [!Note]  
> Cette fonction ne clone pas un effet si l’utilisateur spécifie que [D3DXFX \_ ne peut pas être \_ cloné](d3dxfx.md) pendant la création de l’effet.

 

Pour mettre à jour des paramètres partagés et non partagés dans une technique active d’un effet cloné, consultez [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
