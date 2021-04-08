---
description: 'Cette section contient des informations sur les interfaces système Effects suivantes :'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfaces d’effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1946e7b9e3711bf2d79c0876efca1c533e0ff4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748013"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfaces d’effet (Direct3D 10)

Cette section contient des informations sur les interfaces système Effects suivantes :



| Interfaces                                                                                     | Description                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interface ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Accède à l’état de fusion.                                            |
| [**Interface ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accède à une mémoire tampon de texture ou à une mémoire tampon constante.                  |
| [**Interface ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Accède à l’état du gabarit de profondeur.                                    |
| [**Interface ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accède à une vue de stencil de profondeur.                                   |
| [**Interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Encapsule l’état du pipeline dans une ou plusieurs techniques de rendu. |
| [**Interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Méthodes implémentées par l’utilisateur pour la lecture des fichiers include.              |
| [**Interface ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Accède à une matrice.                                               |
| [**Interface ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Encapsule l’état d’effet d’une passe.                             |
| [**Interface ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifie les variables à effet partagé.                              |
| [**Interface ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Accède à l’état du rastériseur.                                       |
| [**Interface ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Accède à une cible de rendu.                                        |
| [**Interface ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Accède à l’état de l’échantillonneur.                                          |
| [**Interface ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Accède à une variable scalaire.                                      |
| [**Interface ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accède à une ressource de nuanceur.                                      |
| [**Interface ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Accède à une variable de nuanceur.                                      |
| [**Interface ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Accède à une chaîne.                                               |
| [**Interface ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Encapsule une ou plusieurs passes.                                 |
| [**Interface ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implémente des méthodes pour accéder aux variables d’effet.               |
| [**Interface ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Accède à un vecteur.                                               |



 

Il existe deux types d’interfaces dans l’infrastructure Effect : les interfaces de rendu pour le rendu d’une interface d’effet et de réflexion pour l’obtention et la définition de variables d’effet avec l’API. Toutes les interfaces de réflexion dérivent de l' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence d’effet](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
