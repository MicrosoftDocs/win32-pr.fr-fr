---
title: Méthode ID3DX11EffectVariable AsMatrix (D3dx11effect. h)
description: Obtenir une variable de matrice.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- Méthode AsMatrix Direct3D 11
- Méthode AsMatrix Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsMatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c26acd38124a976b53ea950f54e929e717d56555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996333"
---
# <a name="id3dx11effectvariableasmatrix-method"></a>ID3DX11EffectVariable :: AsMatrix, méthode

Obtenir une variable de matrice.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***

Pointeur vers une variable de matrice. Consultez [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).

## <a name="remarks"></a>Notes

AsMatrix retourne une version de la variable Effect qui a été spécialisée pour une variable de matrice. Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de matrice.

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

 

 





