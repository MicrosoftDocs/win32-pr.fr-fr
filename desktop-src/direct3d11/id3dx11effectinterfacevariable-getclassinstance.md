---
title: Méthode ID3DX11EffectInterfaceVariable GetClassInstance (D3dx11effect. h)
description: Obtient une instance de classe.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Méthode GetClassInstance Direct3D 11
- Méthode GetClassInstance Direct3D 11, interface ID3DX11EffectInterfaceVariable
- Interface ID3DX11EffectInterfaceVariable Direct3D 11, méthode GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6fb05473b2671e0224fe36214fa7d8be93dc3bea17ceb90b0b8f0a871cc755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988459"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a>ID3DX11EffectInterfaceVariable :: GetClassInstance, méthode

Obtient une instance de classe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEffectClassInstance* 
</dt> <dd>

Type : **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***

Pointeur vers un pointeur [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) qui sera défini sur l’instance de classe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

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

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





