---
title: Méthode ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView (D3dx11effect. h)
description: Obtenir un mode d’accès non ordonné.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Méthode GetUnorderedAccessView Direct3D 11
- Méthode GetUnorderedAccessView Direct3D 11, interface ID3DX11EffectUnorderedAccessViewVariable
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, méthode GetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996184"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a>ID3DX11EffectUnorderedAccessViewVariable :: GetUnorderedAccessView, méthode

Obtenir un mode d’accès non ordonné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppResource* 
</dt> <dd>

Type : **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***

Pointeur vers un pointeur [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) qui sera défini lors du retour.

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

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





