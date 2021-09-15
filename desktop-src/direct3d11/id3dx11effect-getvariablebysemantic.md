---
title: Méthode ID3DX11Effect GetVariableBySemantic (D3dx11effect. h)
description: Obtenir une variable par sémantique.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Méthode GetVariableBySemantic Direct3D 11
- Méthode GetVariableBySemantic Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403547"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a>ID3DX11Effect :: GetVariableBySemantic, méthode

Obtenir une variable par sémantique.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Équivalent* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Pointeur vers la variable d’effet indiquée par la sémantique. Consultez [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Remarques

Chaque variable Effect peut avoir une sémantique jointe, qui est une chaîne de métadonnées définie par l’utilisateur. Certaines [sémantiques de valeurs système](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) sont des mots réservés qui déclenchent des fonctionnalités intégrées par étapes de pipeline.

La méthode retourne un pointeur vers une [**interface de variable Effect**](id3dx11effectvariable.md) si une variable est introuvable ; vous pouvez appeler [**ID3DX11Effect :: IsValid**](id3dx11effect-isvalid.md) pour vérifier si la sémantique existe.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

