---
title: ID3DX11EffectScalarVariable GetFloat, méthode (D3dx11effect. h)
description: Obtenir une variable à virgule flottante.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Méthode GetFloat Direct3D 11
- Méthode GetFloat Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode GetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1d8f7ae63bc8312c2432e50f5b6dcfeccdf525
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403654"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a>ID3DX11EffectScalarVariable :: GetFloat, méthode

Obtenir une variable à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pValue* 
</dt> <dd>

Type : **float \***

Pointeur vers la variable.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





