---
title: Méthode ID3DX11EffectScalarVariable GetBool (D3dx11effect. h)
description: Obtenir une variable booléenne.
ms.assetid: 9d2789af-c59f-4d2d-87c6-9f36286e8a15
keywords:
- Méthode GetBool Direct3D 11
- Méthode GetBool Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode GetBool
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 754dd8856876ca441e83267250dcfad4f4011c69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762320"
---
# <a name="id3dx11effectscalarvariablegetbool-method"></a>ID3DX11EffectScalarVariable :: GetBool, méthode

Obtenir une variable booléenne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBool(
   BOOL *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pValue* 
</dt> <dd>

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

Pointeur vers la variable.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

