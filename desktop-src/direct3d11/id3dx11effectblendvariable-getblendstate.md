---
title: Méthode ID3DX11EffectBlendVariable GetBlendState (D3dx11effect. h)
description: Obtient un pointeur vers une interface d’état de fusion.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Méthode GetBlendState Direct3D 11
- Méthode GetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, méthode GetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323186"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a>ID3DX11EffectBlendVariable :: GetBlendState, méthode

Obtient un pointeur vers une interface d’état de fusion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexez dans un tableau d’interfaces d’état de fusion. S’il n’existe qu’une seule interface d’état de fusion, utilisez 0.

</dd> <dt>

*ppBlendState* 
</dt> <dd>

Type : **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***

Adresse d’un pointeur vers une interface d’état de fusion (voir [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

