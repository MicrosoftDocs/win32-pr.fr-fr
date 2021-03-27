---
title: Interface ID3DX11EffectVariable (D3dx11effect. h)
description: L’interface ID3DX11EffectVariable est la classe de base pour toutes les variables d’effet. La durée de vie d’un objet ID3DX11EffectVariable est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interface ID3DX11EffectVariable Direct3D 11
- Interface ID3DX11EffectVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762199"
---
# <a name="id3dx11effectvariable-interface"></a>Interface ID3DX11EffectVariable

L’interface **ID3DX11EffectVariable** est la classe de base pour toutes les variables d’effet.

La durée de vie d’un objet **ID3DX11EffectVariable** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectVariable** possède ces méthodes.



| Méthode                                                                           | Description                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**AsBlend**](id3dx11effectvariable-asblend.md)                                 | Obtenir une variable Effect-Blend.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Obtenir une variable d’instance de classe.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Obtient une mémoire tampon constante.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Obtenir une variable de stencil de profondeur.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Obtenir une variable de vue de gabarit de profondeur.<br/>          |
| [**AsInterface**](id3dx11effectvariable-asinterface.md)                         | Obtient une variable d’interface.<br/>                  |
| [**AsMatrix**](id3dx11effectvariable-asmatrix.md)                               | Obtenir une variable de matrice.<br/>                      |
| [**AsRasterizer**](id3dx11effectvariable-asrasterizer.md)                       | Obtenir une variable rastériseur.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Obtenir une variable Render-Target-View.<br/>          |
| [**AsSampler**](id3dx11effectvariable-assampler.md)                             | Obtenir une variable d’échantillonneur.<br/>                     |
| [**AsScalar**](id3dx11effectvariable-asscalar.md)                               | Obtenir une variable scalaire.<br/>                      |
| [**AsShader**](id3dx11effectvariable-asshader.md)                               | Obtenir une variable de nuanceur.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Obtenir une variable de nuanceur-ressource.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Obtenir une variable de chaîne.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Obtenir une variable de vue d’accès non ordonnée.<br/>      |
| [**AsVector**](id3dx11effectvariable-asvector.md)                               | Obtenir une variable vectorielle.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Obtient une annotation par index.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Obtient une annotation par nom.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Obtenir une description.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Obtient un élément de tableau.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Obtient un membre de structure par index.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Obtient un membre de structure par nom.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Obtenir un membre de structure par sémantique.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Obtient une mémoire tampon constante.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | obtenir des données<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Obtient les informations de type.<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | Comparez le type de données avec les données stockées.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Définir des données.<br/>                                   |



 

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

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





