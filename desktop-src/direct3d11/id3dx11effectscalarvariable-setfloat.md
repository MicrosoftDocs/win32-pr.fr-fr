---
title: ID3DX11EffectScalarVariable SetFloat, méthode (D3dx11effect. h)
description: Définissez une variable à virgule flottante.
ms.assetid: e13f3ba1-437a-47f0-bd08-4423ffc25ddb
keywords:
- Méthode SetFloat Direct3D 11
- Méthode SetFloat Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode SetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad3c3e9f020e5094cd03f7b25ee907dcc6e2c2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122457"
---
# <a name="id3dx11effectscalarvariablesetfloat-method"></a>ID3DX11EffectScalarVariable :: SetFloat, méthode

Définissez une variable à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFloat(
   float Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Valeur* 
</dt> <dd>

Type : **float**

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

 

 





