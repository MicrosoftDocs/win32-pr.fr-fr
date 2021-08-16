---
description: Créez un pool d’effets. Un pool est utilisé pour partager des paramètres entre les effets.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: D3DXCreateEffectPool, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 55df5e579b724a26e30223a0a0df7ffa815bda5a64b6f7d7e7e2c2c7f02f2fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804575"
---
# <a name="d3dxcreateeffectpool-function"></a>D3DXCreateEffectPool fonction)

Créez un pool d’effets. Un pool est utilisé pour partager des paramètres entre les effets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppPool* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Retourne un pointeur vers le pool créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK.

Si les arguments ne sont pas valides, la méthode retourne D3DERR \_ INVALIDCALL.

Si la méthode échoue, la valeur de retour est E \_ Fail.

## <a name="remarks"></a>Remarques

Pour les effets au sein d’un pool, les paramètres partagés portant le même nom partagent des valeurs.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Effect](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




