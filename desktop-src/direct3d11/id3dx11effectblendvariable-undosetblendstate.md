---
title: Méthode ID3DX11EffectBlendVariable UndoSetBlendState (D3dx11effect. h)
description: Restaure un état de fusion précédemment défini.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Méthode UndoSetBlendState Direct3D 11
- Méthode UndoSetBlendState Direct3D 11, interface ID3DX11EffectBlendVariable
- Interface ID3DX11EffectBlendVariable Direct3D 11, méthode UndoSetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fefb1e59ef3ef30bcd21700a2573830e3178f574fe631ab4c7373b0bddd5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046477"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a>ID3DX11EffectBlendVariable :: UndoSetBlendState, méthode

Restaure un état de fusion précédemment défini.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexez dans un tableau d’interfaces d’état de fusion. S’il n’existe qu’une seule interface d’état de fusion, utilisez 0.

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

 

