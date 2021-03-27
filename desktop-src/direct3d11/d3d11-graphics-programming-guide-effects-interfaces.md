---
title: Effets des interfaces système (Direct3D 11)
description: Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671897"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Effets des interfaces système (Direct3D 11)

Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet. Il existe deux types d’interfaces : ceux utilisés par le runtime pour restituer des interfaces d’effet et de réflexion afin d’obtenir et de définir des variables d’effet.

-   [Interfaces d’exécution Effect](#effect-runtime-interfaces)
-   [Interfaces d’effet de réflexion](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces d’exécution Effect

Utilisez les interfaces Runtime pour rendre un effet.



| Interfaces d’exécution                                       | Description                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Collection d’un ou plusieurs groupes et techniques pour le rendu. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Collection d’assignations d’État.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Collection d’une ou de plusieurs passes.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Collection d’une ou de plusieurs techniques.                        |



 

## <a name="effect-reflection-interfaces"></a>Interfaces d’effet de réflexion

La réflexion est implémentée dans le système d’effet pour prendre en charge l’état d’effet de lecture (et d’écriture). Il existe plusieurs façons d’accéder aux variables d’effet.

### <a name="setting-groups-of-effect-state"></a>Définition de groupes d’état d’effet

Utilisez ces interfaces pour obtenir et définir un groupe d’États.



| Interfaces de réflexion                                                          | Description                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Obtient et définit l’état de fusion.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Obtient et définit l’état du gabarit de profondeur. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Obtient et définit l’état du rastériseur.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Obtient et définit l’état de l’échantillonneur.       |



 

### <a name="setting-effect-resources"></a>Définition des ressources d’effet

Utilisez ces interfaces pour récupérer et définir des ressources.



| Interfaces de réflexion                                                                        | Description                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Accéder aux données dans une mémoire tampon de texture ou une mémoire tampon constante. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Accédez aux données dans une ressource de stencil de profondeur.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Accéder aux données dans une cible de rendu.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Accéder aux données dans une ressource de nuanceur.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Accédez aux données dans une vue d’accès non ordonnée.            |



 

### <a name="setting-other-effect-variables"></a>Définition d’autres variables d’effet

Utilisez ces interfaces pour récupérer et définir l’État par le type de variable.



| Interfaces de réflexion                                                            | Description               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Obtient une instance de classe.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Obtient et définit une interface. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Obtenir et définir une matrice.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Obtient et définit une valeur scalaire.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Obtenir une variable de nuanceur.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Obtient et définit une chaîne.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Obtient un type de variable.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Obtient et définit un vecteur.     |



 

Toutes les interfaces de réflexion dérivent de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Guide de programmation pour Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 




