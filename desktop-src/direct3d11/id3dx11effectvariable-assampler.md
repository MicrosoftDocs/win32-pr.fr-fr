---
title: Méthode ID3DX11EffectVariable AsSampler (D3dx11effect. h)
description: Obtenir une variable d’échantillonneur.
ms.assetid: dff699f7-758a-442b-93eb-23a09468251f
keywords:
- Méthode AsSampler Direct3D 11
- Méthode AsSampler Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a6c71e8e2cdc89860c8edf82a0c008c03f4a154ab23cee882ed1e9eaaad2939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894599"
---
# <a name="id3dx11effectvariableassampler-method"></a>ID3DX11EffectVariable :: AsSampler, méthode

Obtenir une variable d’échantillonneur.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectSamplerVariable* AsSampler();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***

Pointeur vers une variable d’échantillonneur. Consultez [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md).

## <a name="remarks"></a>Remarques

AsSampler retourne une version de la variable Effect qui a été spécialisée pour une variable d’échantillonneur. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données d’échantillonnage.

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

 

 





