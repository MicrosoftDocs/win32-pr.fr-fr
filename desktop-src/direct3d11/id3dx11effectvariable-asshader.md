---
title: Méthode ID3DX11EffectVariable AsShader (D3dx11effect. h)
description: Obtenir une variable de nuanceur.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Méthode AsShader Direct3D 11
- Méthode AsShader Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsShader
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518857"
---
# <a name="id3dx11effectvariableasshader-method"></a>ID3DX11EffectVariable :: AsShader, méthode

Obtenir une variable de nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

Pointeur vers une variable de nuanceur. Consultez [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).

## <a name="remarks"></a>Remarques

AsShader retourne une version de la variable Effect qui a été spécialisée pour une variable de nuanceur. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de nuanceur.

Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





