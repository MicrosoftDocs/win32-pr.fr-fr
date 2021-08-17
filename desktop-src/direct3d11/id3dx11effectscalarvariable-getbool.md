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
ms.openlocfilehash: d402507c009f46adb2dcb455c772f2102e0e0673675446e25cff0da3382c111a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377859"
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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

