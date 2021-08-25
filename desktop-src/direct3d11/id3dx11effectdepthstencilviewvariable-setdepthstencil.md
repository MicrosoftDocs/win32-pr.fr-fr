---
title: Méthode ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect. h)
description: Définissez une ressource de vue de gabarit de profondeur.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Méthode SetDepthStencil Direct3D 11
- Méthode SetDepthStencil Direct3D 11, interface ID3DX11EffectDepthStencilViewVariable
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, méthode SetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae1e8b984bb15e083360ef99036549c534d8e047a2375ad0b0a6e5469b9191c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069679"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a>ID3DX11EffectDepthStencilViewVariable :: SetDepthStencil, méthode

Définissez une ressource de vue de gabarit de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Préversion* 
</dt> <dd>

Type : **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***

Pointeur vers une interface de vue de stencil-profondeur. Consultez [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).

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

 

 





