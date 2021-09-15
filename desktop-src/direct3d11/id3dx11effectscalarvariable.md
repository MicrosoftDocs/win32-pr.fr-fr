---
title: Interface ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Une interface de variable Effect-scalaire accède à des valeurs scalaires.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Interface ID3DX11EffectScalarVariable Direct3D 11
- Interface ID3DX11EffectScalarVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413244"
---
# <a name="id3dx11effectscalarvariable-interface"></a>Interface ID3DX11EffectScalarVariable

Une interface de variable Effect-scalaire accède à des valeurs scalaires.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectScalarVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectScalarVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectScalarVariable** possède ces méthodes.



| Méthode                                                             | Description                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBool**](id3dx11effectscalarvariable-getbool.md)             | Obtenir une variable booléenne.<br/>                   |
| [**GetBoolArray**](id3dx11effectscalarvariable-getboolarray.md)   | Obtient un tableau de variables booléennes.<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | Obtenir une variable à virgule flottante.<br/>            |
| [**GetFloatArray**](id3dx11effectscalarvariable-getfloatarray.md) | Obtient un tableau de variables à virgule flottante.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Obtient une variable de type Integer.<br/>                  |
| [**GetIntArray**](id3dx11effectscalarvariable-getintarray.md)     | Obtient un tableau de variables de type entier.<br/>        |
| [**SetBool**](id3dx11effectscalarvariable-setbool.md)             | Définissez une variable booléenne.<br/>                   |
| [**SetBoolArray**](id3dx11effectscalarvariable-setboolarray.md)   | Définissez un tableau de variables booléennes.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Définissez une variable à virgule flottante.<br/>            |
| [**SetFloatArray**](id3dx11effectscalarvariable-setfloatarray.md) | Définissez un tableau de variables à virgule flottante.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Définissez une variable de type entier.<br/>                  |
| [**SetIntArray**](id3dx11effectscalarvariable-setintarray.md)     | Définissez un tableau de variables de type entier.<br/>        |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





