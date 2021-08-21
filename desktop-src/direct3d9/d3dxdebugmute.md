---
description: Active ou désactive toute la sortie de débogage D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: D3DXDebugMute, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2bde5446e6e41568c1f9d6aa8408dacc276ab82112a176cf8a038536dd4d992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045077"
---
# <a name="d3dxdebugmute-function"></a>D3DXDebugMute fonction)

Active ou désactive toute la sortie de débogage D3DX.

## <a name="syntax"></a>Syntaxe


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Muet* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, la sortie du débogueur est interrompue ; Si la **valeur est false**, la sortie de débogage est activée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la valeur précédente de muet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
