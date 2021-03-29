---
title: Méthode ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Obtient une variable par index.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Méthode GetVariableByIndex Direct3D 11
- Méthode GetVariableByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992340"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a>ID3DX11Effect :: GetVariableByIndex, méthode

Obtient une variable par index.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVariable* GetVariableByIndex(
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

Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Notes

Un effet peut contenir une ou plusieurs variables. Les variables en dehors d’une technique sont considérées comme globales pour tous les effets, celles qui se trouvent à l’intérieur d’une technique sont locales à cette technique. Vous pouvez accéder à n’importe quelle variable d’effet non statique locale à l’aide de son nom ou d’un index.

La méthode retourne un pointeur vers une [**interface de variable Effect**](id3dx11effectvariable.md) si une variable est introuvable ; vous pouvez appeler [**ID3DX11Effect :: IsValid**](id3dx11effect-isvalid.md) pour vérifier si l’index existe.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

