---
title: Interface ID3DX11EffectTechnique (D3dx11effect. h)
description: Une interface ID3DX11EffectTechnique est une collection de passes. La durée de vie d’un objet ID3DX11EffectTechnique est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interface ID3DX11EffectTechnique Direct3D 11
- Interface ID3DX11EffectTechnique Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416065"
---
# <a name="id3dx11effecttechnique-interface"></a>Interface ID3DX11EffectTechnique

Une interface **ID3DX11EffectTechnique** est une collection de passes.

La durée de vie d’un objet **ID3DX11EffectTechnique** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectTechnique** possède ces méthodes.



| Méthode                                                                        | Description                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Calculez un masque de bloc d’État pour autoriser ou empêcher les modifications d’État.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Obtient une annotation par index.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Obtient une annotation par nom.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Obtenir une description technique.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Obtenir un passage par index.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Obtenir un passage par nom.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Testez une technique pour voir si elle contient une syntaxe valide.<br/>       |



 

## <a name="remarks"></a>Notes

Un effet contient une ou plusieurs techniques ; chaque technique contient une ou plusieurs passes ; chaque passe contient des attributions d’État.

Pour obtenir une interface d’action-technique, appelez une méthode telle que [**ID3DX11Effect :: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

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

 

 





