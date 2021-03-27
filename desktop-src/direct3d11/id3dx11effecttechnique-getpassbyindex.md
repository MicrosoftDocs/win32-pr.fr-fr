---
title: Méthode ID3DX11EffectTechnique GetPassByIndex (D3dx11effect. h)
description: Obtenir un passage par index.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Méthode GetPassByIndex Direct3D 11
- Méthode GetPassByIndex Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetPassByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953967"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a>ID3DX11EffectTechnique :: GetPassByIndex, méthode

Obtenir un passage par index.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectPass* GetPassByIndex(
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

Type : **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Pointeur vers un [**ID3DX11EffectPass**](id3dx11effectpass.md).

## <a name="remarks"></a>Notes

Une technique contient une ou plusieurs passes ; obtenir une passe à l’aide d’un nom ou d’un index.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

