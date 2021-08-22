---
title: Méthode ID3DX11EffectType GetMemberTypeByName (D3dx11effect. h)
description: Obtient un type de membre par nom.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Méthode GetMemberTypeByName Direct3D 11
- Méthode GetMemberTypeByName Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5988a987816ad7e5a1797d60619605228647c3dd81945b63bac9c74701bf77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460709"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a>ID3DX11EffectType :: GetMemberTypeByName, méthode

Obtient un type de membre par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom d’un membre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Pointeur vers un [**ID3DX11EffectType**](id3dx11effecttype.md).

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

 

