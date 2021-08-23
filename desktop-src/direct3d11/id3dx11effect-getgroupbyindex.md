---
title: Méthode ID3DX11Effect GetGroupByIndex (D3dx11effect. h)
description: Obtient un groupe d’effets par index.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Méthode GetGroupByIndex Direct3D 11
- Méthode GetGroupByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetGroupByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184971eea69f80f105aa29bb3dac9decbeb18d3452ca29656a150d4f1e5d9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632469"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a>ID3DX11Effect :: GetGroupByIndex, méthode

Obtient un groupe d’effets par index.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index du groupe d’effets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Pointeur vers une interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

