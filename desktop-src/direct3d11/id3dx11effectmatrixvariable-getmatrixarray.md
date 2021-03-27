---
title: Méthode ID3DX11EffectMatrixVariable GetMatrixArray (D3dx11effect. h)
description: Obtient un tableau de matrices.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Méthode GetMatrixArray Direct3D 11
- Méthode GetMatrixArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode GetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953914"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a>ID3DX11EffectMatrixVariable :: GetMatrixArray, méthode

Obtient un tableau de matrices.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMatrixArray(
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

Pointeur vers le premier élément de la première matrice dans un tableau de matrices.

</dd> <dt>

*Offset* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Décalage (en nombre de matrices) entre le début du tableau et la première matrice retournée.

</dd> <dt>

*Count* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de matrices dans le tableau retourné.

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

 

