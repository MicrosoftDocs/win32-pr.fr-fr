---
title: Méthode ID3DX11Effect CloneEffect (D3dx11effect. h)
description: Crée une copie d’une interface d’effet.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Méthode CloneEffect Direct3D 11
- Méthode CloneEffect Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982602"
---
# <a name="id3dx11effectcloneeffect-method"></a>ID3DX11Effect :: CloneEffect, méthode

Crée une copie d’une interface d’effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicateurs qui affectent la création de l’effet cloné. Peut avoir la valeur 0 ou l’une des valeurs suivantes.



| Indicateur                                    | Description                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Effet de \_ clonage de la \_ force \_ D3DX11 | Ignore tous les qualificateurs « uniques » sur cbuffers. Toutes les cbuffers auront leur propre [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)créé dans l’effet cloné. |



 

</dd> <dt>

*ppClonedEffect* 
</dt> <dd>

Type : **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Pointeur vers un pointeur [**ID3DX11Effect**](id3dx11effect.md) qui sera défini sur la copie de l’effet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

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

 

