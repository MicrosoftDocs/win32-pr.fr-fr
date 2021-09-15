---
title: Interface ID3DX11EffectType (D3dx11effect. h)
description: L’interface ID3DX11EffectType accède aux variables d’effet par type. La durée de vie d’un objet ID3DX11EffectType est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interface ID3DX11EffectType Direct3D 11
- Interface ID3DX11EffectType Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403740"
---
# <a name="id3dx11effecttype-interface"></a>Interface ID3DX11EffectType

L’interface **ID3DX11EffectType** accède aux variables d’effet par type.

La durée de vie d’un objet **ID3DX11EffectType** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectType** possède ces méthodes.



| Méthode                                                                       | Description                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | Obtient une description de type d’effet.<br/>        |
| [**GetMemberName**](id3dx11effecttype-getmembername.md)                     | Obtient le nom d’un membre.<br/>              |
| [**GetMemberSemantic**](id3dx11effecttype-getmembersemantic.md)             | Obtient la sémantique attachée à un membre.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Obtient un type de membre par index.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Obtient un type de membre par nom.<br/>            |
| [**GetMemberTypeBySemantic**](id3dx11effecttype-getmembertypebysemantic.md) | Obtient un type de membre par sémantique.<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | Teste que le type d’effet est valide.<br/>   |



 

## <a name="remarks"></a>Notes

Pour obtenir des informations sur un type d’effet à partir d’une variable Effect, appelez [**ID3DX11EffectVariable :: GetType**](id3dx11effectvariable-gettype.md).

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





