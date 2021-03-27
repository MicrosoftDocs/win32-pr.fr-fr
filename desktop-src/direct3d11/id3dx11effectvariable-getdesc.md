---
title: Méthode ID3DX11EffectVariable GetDesc (D3dx11effect. h)
description: Obtenir une description.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625b9d72b3ff4afe1880b48125d244da1f68844
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996285"
---
# <a name="id3dx11effectvariablegetdesc-method"></a>ID3DX11EffectVariable :: GetDesc, méthode

Obtenir une description.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* 
</dt> <dd>

Type : **[ **D3DX11 \_ Effect \_ variable \_ desc**](d3dx11-effect-variable-desc.md)\***

Pointeur vers une description de variable Effect (voir la [**\_ variable d’effet D3DX11 \_ \_ desc**](d3dx11-effect-variable-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





