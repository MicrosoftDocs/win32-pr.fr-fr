---
title: Méthode ID3DX11EffectVariable AsRasterizer (D3dx11effect. h)
description: Obtenir une variable rastériseur.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Méthode AsRasterizer Direct3D 11
- Méthode AsRasterizer Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsRasterizer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfaf83debc6c7e73a89f78b0c8c3899cce2fb83fb6a5884fa5a5ed9ed5b35912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858099"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>ID3DX11EffectVariable :: AsRasterizer, méthode

Obtenir une variable rastériseur.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Pointeur vers une variable de rastériseur. Consultez [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).

## <a name="remarks"></a>Remarques

AsRasterizer retourne une version de la variable Effect qui a été spécialisée pour une variable rastériseur. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données rastériseur.

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

 

 





