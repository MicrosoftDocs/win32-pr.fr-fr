---
description: 'Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet. Il existe deux types d’interfaces : ceux utilisés par le runtime pour restituer des interfaces d’effet et de réflexion afin d’obtenir et de définir des variables d’effet.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Effets des interfaces système (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110383"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Effets des interfaces système (Direct3D 10)

Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet. Il existe deux types d’interfaces : ceux utilisés par le runtime pour restituer des interfaces d’effet et de réflexion afin d’obtenir et de définir des variables d’effet.

-   [Interfaces d’exécution Effect](#effect-runtime-interfaces)
-   [Interfaces d’effet de réflexion](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces d’exécution Effect

Utilisez les interfaces Runtime pour rendre un effet.



| Interfaces d’exécution                                               | Description                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Collection d’une ou de plusieurs techniques de rendu.                  |
| [**Interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Interface pour l’ajout de comportements personnalisés lors de la lecture de fichiers include. |
| [**Interface ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Collection d’assignations d’État.                                   |
| [**Interface ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Créez un emplacement de mémoire pour les variables à partager entre les effets. |
| [**Interface ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Collection d’une ou de plusieurs passes.                                  |



 

## <a name="effect-reflection-interfaces"></a>Interfaces d’effet de réflexion

La réflexion est implémentée dans le système d’effet pour prendre en charge l’état d’effet de lecture (et d’écriture). Il existe plusieurs façons d’accéder aux variables d’effet.

### <a name="setting-groups-of-effect-state"></a>Définition de groupes d’état d’effet

Utilisez ces interfaces pour obtenir et définir un groupe d’États.



| Interfaces de réflexion                                                                  | Description                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**Interface ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Obtient et définit l’état de fusion.         |
| [**Interface ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Obtient et définit l’état du gabarit de profondeur. |
| [**Interface ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Obtient et définit l’état du rastériseur.    |
| [**Interface ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Obtient et définit l’état de l’échantillonneur.       |



 

### <a name="setting-effect-resources"></a>Définition des ressources d’effet

Utilisez ces interfaces pour récupérer et définir des ressources.



| Interfaces de réflexion                                                                          | Description                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**Interface ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accéder aux données dans une mémoire tampon de texture ou une mémoire tampon constante. |
| [**Interface ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accédez aux données dans une ressource de stencil de profondeur.            |
| [**Interface ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Accéder aux données dans une cible de rendu.                     |
| [**Interface ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accéder aux données dans une ressource de nuanceur.                   |



 

### <a name="setting-other-effect-variables"></a>Définition d’autres variables d’effet

Utilisez ces interfaces pour récupérer et définir l’État par le type de variable.



| Interfaces de réflexion                                                      | Description                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**Interface ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Obtenir et définir une matrice.          |
| [**Interface ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Obtient et définit une valeur scalaire.          |
| [**Interface ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Obtient et définit une variable de nuanceur. |
| [**Interface ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Obtient et définit une chaîne.          |
| [**Interface ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Obtient un type de variable.           |
| [**Interface ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Obtient et définit un vecteur.          |



 

Toutes les interfaces de réflexion dérivent de l' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
