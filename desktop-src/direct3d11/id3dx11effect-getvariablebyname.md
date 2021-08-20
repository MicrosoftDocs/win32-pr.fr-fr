---
title: Méthode ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Obtient une variable par nom.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Méthode GetVariableByName Direct3D 11
- Méthode GetVariableByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e8741eaf2ced1022a130ecb94c7f8553159e862ca23b50ba4d12786ad37620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099042"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>ID3DX11Effect :: GetVariableByName, méthode

Obtient une variable par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la variable.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Retourne une variable non valide si le nom spécifié est introuvable.

## <a name="remarks"></a>Remarques

Un effet peut contenir une ou plusieurs variables. Les variables en dehors d’une technique sont considérées comme globales pour tous les effets, celles qui se trouvent à l’intérieur d’une technique sont locales à cette technique. Vous pouvez accéder à une variable Effect à l’aide de son nom ou d’un index.

La méthode retourne un pointeur vers une [**interface d’effet-variable,**](id3dx11effectvariable.md) qu’il existe ou non une variable. [**ID3DX11Effect :: IsValid**](id3dx11effect-isvalid.md) doit être appelé pour vérifier si le nom existe.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

