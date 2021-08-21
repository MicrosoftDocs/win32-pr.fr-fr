---
title: Méthode ID3DX11EffectDepthStencilViewVariable GetDepthStencil (D3dx11effect. h)
description: Obtenir une ressource de vue de gabarit de profondeur.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Méthode GetDepthStencil Direct3D 11
- Méthode GetDepthStencil Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, méthode GetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d31b5a947afc9a1b92349b20bc5d075599a16d12abae0ac7d375e8bc0a0de89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989739"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a>ID3DX11EffectDepthStencilViewVariable :: GetDepthStencil, méthode

Obtenir une ressource de vue de gabarit de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppResource* 
</dt> <dd>

Type : **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***

Adresse d’un pointeur vers une interface de vue de stencil-profondeur. Consultez [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





