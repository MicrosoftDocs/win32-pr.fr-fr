---
title: ID3DX11EffectScalarVariable setInt, méthode (D3dx11effect. h)
description: Définissez une variable de type entier.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- SetInt, méthode Direct3D 11
- SetInt, méthode Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode setInt
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4e2f44a3b67db12bd84f5dd23426c033b99b57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530997"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>ID3DX11EffectScalarVariable :: setInt, méthode

Définissez une variable de type entier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Valeur* 
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

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

 

