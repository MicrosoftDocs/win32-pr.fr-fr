---
title: Méthode ID3DX11EffectType GetMemberTypeBySemantic (D3dx11effect. h)
description: Obtient un type de membre par sémantique.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Méthode GetMemberTypeBySemantic Direct3D 11
- Méthode GetMemberTypeBySemantic Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetMemberTypeBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e1add6ddc485f803512050795b9ba240f2a29d145fb01e864b88bc8ba84ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532331"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a>ID3DX11EffectType :: GetMemberTypeBySemantic, méthode

Obtient un type de membre par sémantique.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
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

 

