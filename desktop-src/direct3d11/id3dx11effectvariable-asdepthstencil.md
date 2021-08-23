---
title: Méthode ID3DX11EffectVariable AsDepthStencil (D3dx11effect. h)
description: Obtenir une variable de stencil de profondeur.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Méthode AsDepthStencil Direct3D 11
- Méthode AsDepthStencil Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771f22b6b757b9144fca7e2637a3a702232b3d2a4a837938454b2acd5237cfae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729129"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a>ID3DX11EffectVariable :: AsDepthStencil, méthode

Obtenir une variable de stencil de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***

Pointeur vers une variable de stencil de profondeur. Consultez [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).

## <a name="remarks"></a>Remarques

AsDepthStencil retourne une version de la variable Effect qui a été spécialisée pour une variable de stencil de profondeur. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de stencil de profondeur.

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

 

 





