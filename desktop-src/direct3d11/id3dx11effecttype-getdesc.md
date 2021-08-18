---
title: Méthode ID3DX11EffectType GetDesc (D3dx11effect. h)
description: Obtient une description de type d’effet.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381f885a15dede6a500e82b08a1f24e4f0542ffa46211e5b68ef7f73f40d0f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460779"
---
# <a name="id3dx11effecttypegetdesc-method"></a>ID3DX11EffectType :: GetDesc, méthode

Obtient une description de type d’effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* 
</dt> <dd>

Type : type d' **[ **\_ effet D3DX11 \_ \_ desc**](d3dx11-effect-type-desc.md)\***

Pointeur vers une description de type d’effet. Consultez [**la \_ \_ \_ Description du type d’effet D3DX11**](d3dx11-effect-type-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

La description de la variable Effect contient des données sur le nom, les annotations, la sémantique, les indicateurs et le décalage de la mémoire tampon du type d’effet.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

 





