---
title: Méthode ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect. h)
description: Restaure un état de rastériseur précédemment défini.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Méthode UndoSetRasterizerState Direct3D 11
- Méthode UndoSetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, méthode UndoSetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211963"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable :: UndoSetRasterizerState, méthode

Restaure un état de rastériseur précédemment défini.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index dans un tableau d’interfaces de rastérisation. S’il n’existe qu’une seule interface rastériseur, utilisez 0.

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

