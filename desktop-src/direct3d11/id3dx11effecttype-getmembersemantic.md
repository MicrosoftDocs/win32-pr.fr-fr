---
title: Méthode ID3DX11EffectType GetMemberSemantic (D3dx11effect. h)
description: Obtient la sémantique attachée à un membre.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Méthode GetMemberSemantic Direct3D 11
- Méthode GetMemberSemantic Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetMemberSemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992185"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a>ID3DX11EffectType :: GetMemberSemantic, méthode

Obtient la sémantique attachée à un membre.

## <a name="syntax"></a>Syntaxe


```C++
LPCSTR GetMemberSemantic(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Chaîne qui contient la sémantique.

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

