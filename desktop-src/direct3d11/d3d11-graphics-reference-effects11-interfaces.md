---
title: Effets 11 interfaces
description: Cette section contient des informations de référence sur les interfaces COM (Component Object Model) de la source Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20713f5a40b2d8b85edb92166b7e64af18fefee62e5267adcffa25356c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537701"
---
# <a name="effects-11-interfaces"></a>Effets 11 interfaces

Cette section contient des informations de référence sur les interfaces COM (Component Object Model) de la source Effects 11.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                   | Description                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Une interface [**ID3DX11Effect**](id3dx11effect.md) gère un ensemble d’objets d’État, de ressources et de nuanceurs pour l’implémentation d’un effet de rendu.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | L’interface de variable Blend accède à l’État Blend.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Accède à une instance de classe.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Une interface de mémoire tampon constante accède aux mémoires tampons constantes ou aux mémoires tampons de texture.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Une interface à profondeur variable de gabarit accède à l’état de gabarit de profondeur.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Une interface à profondeur variable de vue de gabarit accède à une vue de stencil de profondeur.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | L’interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) accède à un groupe d’effets.<br/> La durée de vie d’un objet [**ID3DX11EffectGroup**](id3dx11effectgroup.md) est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Accède à une variable d’interface.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Une interface à matrice variable accède à une matrice.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Une interface [**ID3DX11EffectPass**](id3dx11effectpass.md) encapsule les assignations d’État au sein d’une technique.<br/> La durée de vie d’un objet [**ID3DX11EffectPass**](id3dx11effectpass.md) est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Une interface de la variable rastériseur accède à l’état du rastériseur.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Une interface de rendu-cible-vue accède à une cible de rendu.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Une interface d’échantillonneur accède à l’état de l’échantillonneur.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Une interface de variable Effect-scalaire accède à des valeurs scalaires.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Une interface de nuanceur-ressource accède à une ressource de nuanceur.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Une interface de variable de nuanceur accède à une variable de nuanceur.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Une interface de variable de chaîne accède à une variable de chaîne.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Une interface [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) est une collection de passes.<br/> La durée de vie d’un objet [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | L’interface [**ID3DX11EffectType**](id3dx11effecttype.md) accède aux variables d’effet par type.<br/> La durée de vie d’un objet [**ID3DX11EffectType**](id3dx11effecttype.md) est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Accède à une vue d’accès non ordonnée.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | L’interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est la classe de base pour toutes les variables d’effet.<br/> La durée de vie d’un objet [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Une interface de variable vectorielle accède à un vecteur à quatre composants.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur Effects 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





