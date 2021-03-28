---
title: Méthode ID3DX11EffectClassInstanceVariable GetClassInstance (D3dx11effect. h)
description: Obtient une instance de classe.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Méthode GetClassInstance Direct3D 11
- Méthode GetClassInstance Direct3D 11, interface ID3DX11EffectClassInstanceVariable
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11, méthode GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323393"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a>ID3DX11EffectClassInstanceVariable :: GetClassInstance, méthode

Obtient une instance de classe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppClassInstance* 
</dt> <dd>

Type : **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***

Pointeur vers un pointeur [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) qui sera défini sur l’instance de classe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

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

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





