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
ms.openlocfilehash: 963653f3814d0d7984966328327d1f7ece8f9a30727f361daefb91a554db1265
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069619"
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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

