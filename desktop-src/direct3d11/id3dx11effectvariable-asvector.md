---
title: Méthode ID3DX11EffectVariable AsVector (D3dx11effect. h)
description: Obtenir une variable vectorielle.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Méthode AsVector Direct3D 11
- Méthode AsVector Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df994536c818461b0307cdee726e704aaaf8a43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518849"
---
# <a name="id3dx11effectvariableasvector-method"></a>ID3DX11EffectVariable :: AsVector, méthode

Obtenir une variable vectorielle.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***

Pointeur vers une variable vectorielle. Consultez [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).

## <a name="remarks"></a>Remarques

AsVector retourne une version de la variable Effect qui a été spécialisée pour une variable Vector. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données vectorielles.

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

 

 





