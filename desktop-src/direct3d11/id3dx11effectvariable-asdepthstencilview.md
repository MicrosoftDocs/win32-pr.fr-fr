---
title: Méthode ID3DX11EffectVariable AsDepthStencilView (D3dx11effect. h)
description: Obtenir une variable de vue de gabarit de profondeur.
ms.assetid: 491ca6e1-a74c-4996-a25c-ea40910f0f36
keywords:
- Méthode AsDepthStencilView Direct3D 11
- Méthode AsDepthStencilView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsDepthStencilView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencilView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dc0ce53478da8d7057c142c87daea5fb83503b4ac7cd1a0dee5edda89246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531507"
---
# <a name="id3dx11effectvariableasdepthstencilview-method"></a>ID3DX11EffectVariable :: AsDepthStencilView, méthode

Obtenir une variable de vue de gabarit de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectDepthStencilViewVariable* AsDepthStencilView();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***

Pointeur vers une variable de vue de stencil de profondeur. Consultez [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).

## <a name="remarks"></a>Remarques

Cette méthode retourne une version de la variable Effect qui a été spécialisée pour une variable de vue de stencil de profondeur. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données Depth-View-View.

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

 

 





