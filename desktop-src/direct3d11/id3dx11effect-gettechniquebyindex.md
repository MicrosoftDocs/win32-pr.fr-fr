---
title: Méthode ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
description: Obtient une technique par index. | Méthode ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Méthode GetTechniqueByIndex Direct3D 11
- Méthode GetTechniqueByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953954"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a>ID3DX11Effect :: GetTechniqueByIndex, méthode

Obtient une technique par index.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
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

Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).

## <a name="remarks"></a>Notes

Un effet contient une ou plusieurs techniques ; chaque technique contient une ou plusieurs passes. Vous pouvez accéder à une technique à l’aide de son nom ou d’un index.

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

 

