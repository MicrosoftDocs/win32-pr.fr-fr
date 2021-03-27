---
title: Interface ID3DX11EffectPass (D3dx11effect. h)
description: Une interface ID3DX11EffectPass encapsule les assignations d’État au sein d’une technique. La durée de vie d’un objet ID3DX11EffectPass est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interface ID3DX11EffectPass Direct3D 11
- Interface ID3DX11EffectPass Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211896"
---
# <a name="id3dx11effectpass-interface"></a>Interface ID3DX11EffectPass

Une interface **ID3DX11EffectPass** encapsule les assignations d’État au sein d’une technique.

La durée de vie d’un objet **ID3DX11EffectPass** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectPass** possède ces méthodes.



| Méthode                                                                   | Description                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Appliquer**](id3dx11effectpass-apply.md)                                 | Définit l’État contenu dans un passage à l’appareil.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Générez un masque pour autoriser ou empêcher les modifications d’État.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Obtient une annotation par index.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Obtient une annotation par nom.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Obtenir une description du nuanceur de calcul.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Obtenir une description du passage.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Obtenir une description du nuanceur de domaine.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Obtient une géométrie-Description du nuanceur.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Obtient la description de la coque-Shader.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Obtenir une description de nuanceur de pixels.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Obtenir une description du nuanceur de sommets.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Testez un passage pour voir s’il contient une syntaxe valide.<br/>        |



 

## <a name="remarks"></a>Notes

Une passe est un bloc de code qui définit des objets d’état de rendu et des nuanceurs. Une passe est déclarée au sein d’une technique.

Pour obtenir une interface Effect-Pass, appelez une méthode comme [**ID3DX11EffectTechnique :: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

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

 

 





