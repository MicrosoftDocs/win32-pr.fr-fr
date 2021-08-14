---
title: Méthode ID3DX11EffectBlendVariable SetBlendState (D3dx11effect. h)
description: Définit l’état de fusion d’un effet.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Méthode SetBlendState Direct3D 11
- Méthode SetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, méthode SetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a8f945faaf7f07846ea58b91378bbf2e6c06eeb1c3d0d041a6e0a71e2e9ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046497"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a>ID3DX11EffectBlendVariable :: SetBlendState, méthode

Définit l’état de fusion d’un effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexez dans un tableau d’interfaces d’état de fusion. S’il n’existe qu’une seule interface d’état de fusion, utilisez 0.

</dd> <dt>

*pBlendState* 
</dt> <dd>

Type : **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***

Pointeur vers une interface [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) contenant l’état de fusion à définir.

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

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

