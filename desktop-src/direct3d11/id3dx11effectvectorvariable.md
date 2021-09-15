---
title: Interface ID3DX11EffectVectorVariable (D3dx11effect. h)
description: Une interface de variable vectorielle accède à un vecteur à quatre composants.
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- Interface ID3DX11EffectVectorVariable Direct3D 11
- Interface ID3DX11EffectVectorVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9235a4047617dd2e5ff9f14925908ae7a0dc1060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517545"
---
# <a name="id3dx11effectvectorvariable-interface"></a>Interface ID3DX11EffectVectorVariable

Une interface de variable vectorielle accède à un vecteur à quatre composants.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectVectorVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectVectorVariable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectVectorVariable** possède ces méthodes.



| Méthode                                                                         | Description                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetBoolVector**](id3dx11effectvectorvariable-getboolvector.md)             | Obtenir un vecteur à quatre composants qui contient des données booléennes.<br/>                  |
| [**GetBoolVectorArray**](id3dx11effectvectorvariable-getboolvectorarray.md)   | Obtient un tableau de vecteurs à quatre composants qui contiennent des données booléennes.<br/>        |
| [**GetFloatVector**](id3dx11effectvectorvariable-getfloatvector.md)           | Obtenir un vecteur à quatre composants qui contient des données à virgule flottante.<br/>           |
| [**GetFloatVectorArray**](id3dx11effectvectorvariable-getfloatvectorarray.md) | Obtient un tableau de vecteurs à quatre composants qui contiennent des données à virgule flottante.<br/> |
| [**GetIntVector**](id3dx11effectvectorvariable-getintvector.md)               | Obtient un vecteur à quatre composants qui contient des données de type entier.<br/>                  |
| [**GetIntVectorArray**](id3dx11effectvectorvariable-getintvectorarray.md)     | Obtient un tableau de vecteurs à quatre composants qui contiennent des données de type entier.<br/>        |
| [**SetBoolVector**](id3dx11effectvectorvariable-setboolvector.md)             | Définissez un vecteur à quatre composants qui contient des données booléennes.<br/>                  |
| [**SetBoolVectorArray**](id3dx11effectvectorvariable-setboolvectorarray.md)   | Définissez un tableau de vecteurs à quatre composants qui contiennent des données booléennes.<br/>        |
| [**SetFloatVector**](id3dx11effectvectorvariable-setfloatvector.md)           | Définissez un vecteur à quatre composants qui contient des données à virgule flottante.<br/>           |
| [**SetFloatVectorArray**](id3dx11effectvectorvariable-setfloatvectorarray.md) | Définissez un tableau de vecteurs à quatre composants qui contiennent des données à virgule flottante.<br/> |
| [**SetIntVector**](id3dx11effectvectorvariable-setintvector.md)               | Définissez un vecteur à quatre composants qui contient des données de type entier.<br/>                  |
| [**SetIntVectorArray**](id3dx11effectvectorvariable-setintvectorarray.md)     | Définissez un tableau de vecteurs à quatre composants qui contiennent des données de type entier.<br/>        |



 

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

 

 





