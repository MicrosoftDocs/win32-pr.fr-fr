---
title: ID3DX11EffectVariable GetElement, méthode (D3dx11effect. h)
description: Obtient un élément de tableau.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- Méthode GetElement Direct3D 11
- GetElement, méthode Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetElement
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61bd208bb9dfecd861a0fd9e25a974da4daeb40fbcaad2316d677cb61f44315
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894589"
---
# <a name="id3dx11effectvariablegetelement-method"></a>ID3DX11EffectVariable :: GetElement, méthode

Obtient un élément de tableau.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro ; Sinon, 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Remarques

Si la variable d’effet est un tableau, utilisez cette méthode pour retourner l’un des éléments.

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

 

