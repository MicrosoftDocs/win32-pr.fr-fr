---
title: Liaison de ressource
description: La liaison est le processus qui consiste à lier des objets de ressource aux nuanceurs du pipeline Graphics.
ms.assetid: CB0065EF-4E53-4E16-9F7E-09A261C360FB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086a14beec32447cb91e2a345f4fecda8d5480fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012887"
---
# <a name="resource-binding"></a>Liaison de ressource

La liaison est le processus qui consiste à lier des objets de ressource aux nuanceurs du pipeline Graphics.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Vue d’ensemble de la liaison de ressources](resource-binding-flow-of-control.md) | La clé de la liaison de ressources dans DirectX 12 est l’un des concepts d’un *descripteur*, de *tables de descripteurs*, de *tas de descripteurs* et d’une *signature racine*. |
| [Différences dans le modèle de liaison de Direct3D 11](binding-model.md) | L’une des principales décisions de conception derrière la liaison DirectX12 est de la séparer des autres tâches de gestion. Cela impose des exigences sur l’application pour gérer certains dangers potentiels. |
| [Descripteurs](descriptors.md) | Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12. |
| [Tas de descripteurs](descriptor-heaps.md) | Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur. |
| [Tables de descripteurs](descriptor-tables.md) | Une table de descripteur est logiquement un tableau de descripteurs. |
| [Signatures racine](root-signatures.md) | La signature racine définit les types de ressources qui sont liés au pipeline Graphics. |
| [Interrogation des fonctionnalités](capability-querying.md) | Votre application peut découvrir le niveau de prise en charge de la liaison de ressources, ainsi que de nombreuses autres fonctionnalités, avec un appel à [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). |
| [Liaison de ressources dans HSL](resource-binding-in-hlsl.md) | Cette rubrique décrit certaines fonctionnalités spécifiques à l’utilisation du [modèle de nuanceur](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (High Level Shader Language) 5,1 avec Direct3D 12. Tout le matériel Direct3D 12 prend en charge le modèle de nuanceur 5,1. par conséquent, la prise en charge de ce modèle ne dépend pas du niveau de fonctionnalité matérielle. |
| [Optimisations UMA : textures accessibles par le processeur et Swizzle standard](default-texture-mapping.md) | Les GPU (Universal Memory Architecture, UMA) offrent des avantages en termes de performances par rapport aux GPU discrets, en particulier lors de l’optimisation des appareils mobiles. L’octroi d’un accès processeur aux ressources lorsque le GPU est UMA peut réduire la quantité de copie qui se produit entre le processeur et le GPU. Même si nous recommandons aux applications de ne pas donner un accès au processeur à toutes les ressources sur les conceptions UMA, il existe des possibilités d’améliorer l’efficacité en donnant les ressources nécessaires à l’accès au processeur. Contrairement aux GPU discrètes, le processeur peut techniquement avoir un pointeur vers toutes les ressources auxquelles le GPU peut accéder. |
| [Chargements de vues d’accès non ordonnées typées](typed-unordered-access-view-loads.md) | Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)spécifique. |
| [Ressources en mosaïque de volume](volume-tiled-resources.md) | Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions. |
| [Sous-ressources](subresources.md) | Décrit comment une ressource est divisée en sous-ressources et comment référencer une seule, plusieurs ou plusieurs sous-ressources. |

## <a name="related-topics"></a>Rubriques connexes

* [Guide de programmation de Direct3D 12](directx-12-programming-guide.md)
* [Didacticiels vidéo sur DirectX Advanced Learning : liaison de ressources dans DirectX 12](https://www.youtube.com/watch?v=Uwhhdktaofg)
* [Gestion de la mémoire](memory-management.md)