---
title: Méthode ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect. h)
description: Rétablit un État du stencil de profondeur précédemment défini.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Méthode UndoSetDepthStencilState Direct3D 11
- Méthode UndoSetDepthStencilState Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, méthode UndoSetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626c430c268c7c8c63e006bdde9e62a49d139d2212e08d7a3e4cedeea3d31722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989815"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a>ID3DX11EffectDepthStencilVariable :: UndoSetDepthStencilState, méthode

Rétablit un État du stencil de profondeur précédemment défini.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index dans un tableau d’interfaces de stencil de profondeur. S’il n’existe qu’une seule interface de stencil de profondeur, utilisez 0.

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

