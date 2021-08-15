---
title: Méthode ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect. h)
description: Obtenir une variable de vue d’accès non ordonnée.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Méthode AsUnorderedAccessView Direct3D 11
- Méthode AsUnorderedAccessView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4cf3a1f146af7ca6faf3ff3e704285ac19f01a117809429842b45df9b7dcfd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531207"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a>ID3DX11EffectVariable :: AsUnorderedAccessView, méthode

Obtenir une variable de vue d’accès non ordonnée.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***

Pointeur vers une variable d’affichage d’accès non ordonnée. Consultez [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).

## <a name="remarks"></a>Remarques

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

 

 





