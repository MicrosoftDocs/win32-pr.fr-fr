---
description: Appliquez les valeurs d’un bloc d’État à l’état du système d’effet actuel.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect :: ApplyParameterBlock, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8f5a382823da73df68ec0c32e120c0e94a2a7deba86e6aac4afe01e4e46acd7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951799"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>ID3DXEffect :: ApplyParameterBlock, méthode

Appliquez les valeurs d’un bloc d’État à l’état du système d’effet actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 *hParameterBlock* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle du bloc de paramètres. Il s’agit du handle retourné par [**ID3DXEffect :: EndParameterBlock**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Remarques

L’état du paramètre d’effet de capture change dans un bloc de paramètres en appelant BeginParameterBlock ; Arrêtez la capture des modifications d’État en appelant EndParameterBlock. Ces modifications d’État incluent les modifications de paramètres d’effet qui se produisent à l’intérieur d’une technique (y compris celles en dehors d’une passe). Une fois que vous avez terminé avec le bloc de paramètres, appelez DeleteParameterBlock pour récupérer de la mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect ::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




