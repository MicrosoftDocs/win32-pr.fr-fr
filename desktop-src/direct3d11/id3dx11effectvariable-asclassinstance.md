---
title: Méthode ID3DX11EffectVariable AsClassInstance (D3dx11effect. h)
description: Obtenir une variable d’instance de classe.
ms.assetid: c1d4adb5-7cd2-4ba2-9a91-3d03f9596a10
keywords:
- Méthode AsClassInstance Direct3D 11
- Méthode AsClassInstance Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17dc9124f4b9a24ead503694c10a4a2d2205ed3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012968"
---
# <a name="id3dx11effectvariableasclassinstance-method"></a>ID3DX11EffectVariable :: AsClassInstance, méthode

Obtenir une variable d’instance de classe.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectClassInstanceVariable* AsClassInstance();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***

Pointeur vers une variable d’instance de classe. Consultez [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).

## <a name="remarks"></a>Notes

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

 

 





