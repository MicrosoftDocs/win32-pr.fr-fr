---
title: Méthode ID3DX11EffectMatrixVariable SetMatrixArray (D3dx11effect. h)
description: Définissez un tableau de matrices à virgule flottante.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Méthode SetMatrixArray Direct3D 11
- Méthode SetMatrixArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode SetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974623"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a>ID3DX11EffectMatrixVariable :: SetMatrixArray, méthode

Définissez un tableau de matrices à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **float \***

Pointeur vers la première matrice.

</dd> <dt>

*Offset* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments de matrice à ignorer à partir du début du tableau.

</dd> <dt>

*Count* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments à définir.

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

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

