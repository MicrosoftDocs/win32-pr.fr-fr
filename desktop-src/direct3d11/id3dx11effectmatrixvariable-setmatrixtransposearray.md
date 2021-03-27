---
title: Méthode ID3DX11EffectMatrixVariable SetMatrixTransposeArray (D3dx11effect. h)
description: Transposez et définissez un tableau de matrices à virgule flottante.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Méthode SetMatrixTransposeArray Direct3D 11
- Méthode SetMatrixTransposeArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode SetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953962"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a>ID3DX11EffectMatrixVariable :: SetMatrixTransposeArray, méthode

Transposez et définissez un tableau de matrices à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMatrixTransposeArray(
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

Pointeur vers un tableau de matrices.

</dd> <dt>

*Offset* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Décalage (en nombre de matrices) entre le début du tableau et la première matrice à définir.

</dd> <dt>

*Count* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de matrices dans le tableau à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

En transposant une matrice, vous réorganisez l’ordre des données de l’ordre des colonnes de lignes à l’ordre des lignes (ou vice versa).

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

 

