---
description: Démarre une technique active.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect :: Begin, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f4e41830b0bb4507e3969c327c84a85c5336e5f07389fa12e05f3a92f4089a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675459"
---
# <a name="id3dxeffectbegin-method"></a>ID3DXEffect :: Begin, méthode

Démarre une technique active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPasses* \[ à\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers une valeur retournée qui indique le nombre de passes nécessaires pour restituer la technique actuelle.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Valeur DWORD qui détermine si l’état modifié par un effet est enregistré et restauré. La valeur par défaut 0 spécifie que **ID3DXEffect :: Begin** et [**ID3DXEffect :: end**](id3dxeffect--end.md) vont enregistrer et restaurer tous les États modifiés par l’effet (y compris les constantes de nuanceur de pixels et de vertex). Les indicateurs valides peuvent être affichés à l' [État Effects Save et Restore Flags](d3dxfx.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

Une application définit une technique active dans le système d’effet en appelant **ID3DXEffect :: Begin**. Le système d’effet répond en capturant tout l’état du pipeline qui peut être modifié par la technique dans un bloc d’État. Une application signale la fin d’une technique en appelant [**ID3DXEffect :: end**](id3dxeffect--end.md), qui utilise le bloc d’État pour restaurer l’état d’origine. Le système d’effet prend donc en charge l’enregistrement de l’État lorsqu’une technique devient active et la restauration de l’État lorsqu’une technique se termine. Si vous choisissez de désactiver cette fonctionnalité d’enregistrement et de restauration, consultez [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

Dans la paire **ID3DXEffect :: Begin** et [**ID3DXEffect :: end**](id3dxeffect--end.md) , une application utilise [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) pour définir la passe active, [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) si des modifications d’État se sont produites après l’activation de la passe, et [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) pour terminer la passe active.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
