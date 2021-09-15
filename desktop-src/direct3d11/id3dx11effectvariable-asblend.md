---
title: Méthode ID3DX11EffectVariable AsBlend (D3dx11effect. h)
description: Obtenir une variable Effect-Blend.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- Méthode AsBlend Direct3D 11
- Méthode AsBlend Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsBlend
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f7e3d09a1299d00482e9a5cfbb75f563d4bba5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403737"
---
# <a name="id3dx11effectvariableasblend-method"></a>ID3DX11EffectVariable :: AsBlend, méthode

Obtenir une variable Effect-Blend.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***

Pointeur vers une variable d’effet de fusion. Consultez [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).

## <a name="remarks"></a>Notes

AsBlend retourne une version de la variable Effect qui a été spécialisée pour une variable Effect-Blend. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données Effect-Blend.

Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).

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

 

 





