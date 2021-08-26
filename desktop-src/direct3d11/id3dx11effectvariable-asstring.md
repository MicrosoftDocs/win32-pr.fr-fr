---
title: Méthode ID3DX11EffectVariable AsString (D3dx11effect. h)
description: Obtenir une variable de chaîne.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- Méthode AsString Direct3D 11
- Méthode AsString Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsString
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69eecaabec6b7da49f7f36f6c75677fdd20cdb462f26fe5e02650e6746c01f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069609"
---
# <a name="id3dx11effectvariableasstring-method"></a>ID3DX11EffectVariable :: AsString, méthode

Obtenir une variable de chaîne.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Pointeur vers une variable de chaîne. Consultez [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).

## <a name="remarks"></a>Remarques

AsString retourne une version de la variable Effect qui a été spécialisée pour une variable de chaîne. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de chaîne.

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

 

 





