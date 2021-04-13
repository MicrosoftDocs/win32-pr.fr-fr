---
description: Met fin à une technique active.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect :: end, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322982"
---
# <a name="id3dxeffectend-method"></a>ID3DXEffect :: end, méthode

Met fin à une technique active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette méthode retourne toujours la valeur \_ OK.

## <a name="remarks"></a>Notes

Tout rendu dans un effet est effectué dans une paire correspondante d’appels [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) et **ID3DXEffect :: end** . Une fois toutes les passes rendues, **ID3DXEffect :: end** doit être appelé pour terminer la technique active. Le système d’effet répond à l’aide du bloc d’état créé lors de l’appel de **ID3DXEffect :: Begin** , afin de restaurer automatiquement l’état du pipeline avant **ID3DXEffect :: Begin**.

Par défaut, le système d’effet prend en charge l’enregistrement de l’état avant une technique et la restauration de l’état après une technique. Si vous choisissez de désactiver cette fonctionnalité d’enregistrement et de restauration, consultez [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




