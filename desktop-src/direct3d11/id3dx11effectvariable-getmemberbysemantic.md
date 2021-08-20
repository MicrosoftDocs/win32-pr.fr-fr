---
title: Méthode ID3DX11EffectVariable GetMemberBySemantic (D3dx11effect. h)
description: Obtenir un membre de structure par sémantique.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Méthode GetMemberBySemantic Direct3D 11
- Méthode GetMemberBySemantic Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetMemberBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46155fc961836b187e0a12ab3571a4edcb67740c7e4dd26fb92350009b95edef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045817"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a>ID3DX11EffectVariable :: GetMemberBySemantic, méthode

Obtenir un membre de structure par sémantique.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Équivalent* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Remarques

Si la variable d’effet est une structure, utilisez cette méthode pour rechercher un membre à l’aide de la sémantique jointe.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

