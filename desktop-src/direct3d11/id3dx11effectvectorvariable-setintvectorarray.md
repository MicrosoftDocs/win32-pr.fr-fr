---
title: Méthode ID3DX11EffectVectorVariable SetIntVectorArray (D3dx11effect. h)
description: Définissez un tableau de vecteurs à quatre composants qui contiennent des données de type entier.
ms.assetid: c9e522d7-5545-4b91-b6b3-6fad9a151cb0
keywords:
- Méthode SetIntVectorArray Direct3D 11
- Méthode SetIntVectorArray Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode SetIntVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5260fd85461b23d02d9aa33619fcf2c00a81fcb63212d612e6e8920728bbefd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894539"
---
# <a name="id3dx11effectvectorvariablesetintvectorarray-method"></a>ID3DX11EffectVectorVariable :: SetIntVectorArray, méthode

Définissez un tableau de vecteurs à quatre composants qui contiennent des données de type entier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Pointeur vers le début des données à définir.

</dd> <dt>

*Offset* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Doit avoir la valeur 0 ; elle est réservée à une utilisation ultérieure.

</dd> <dt>

*Count* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments de tableau à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

