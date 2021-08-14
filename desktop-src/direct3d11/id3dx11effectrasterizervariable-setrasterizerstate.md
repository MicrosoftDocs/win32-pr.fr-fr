---
title: Méthode ID3DX11EffectRasterizerVariable SetRasterizerState (D3dx11effect. h)
description: Définit l’état du rastériseur.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Méthode SetRasterizerState Direct3D 11
- Méthode SetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, méthode SetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da95b99a3707b9fd9d05e9343e36a095cf3d6a346180df69ad6ecd3f749febd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534327"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable :: SetRasterizerState, méthode

Définit l’état du rastériseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index dans un tableau d’interfaces de rastérisation. S’il n’existe qu’une seule interface rastériseur, utilisez 0.

</dd> <dt>

*pRasterizerState* 
</dt> <dd>

Type : **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***

Pointeur vers une interface [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) .

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

