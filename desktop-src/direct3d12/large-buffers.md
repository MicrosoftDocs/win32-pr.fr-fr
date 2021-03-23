---
title: Sous-allocation dans des mémoires tampons
description: Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU. Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104620"
---
# <a name="suballocation-within-buffers"></a>Sous-allocation dans des mémoires tampons

Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU. Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.

Comme pour D3D11, les applications dans D3D12 doivent toujours déclarer l’utilisation de la mémoire lors de l’allocation de mémoires tampons dans D3D12 par rapport aux ressources dynamiques/intermédiaires dans D3D11, mais dans D3D12, les développeurs disposent d’une plus grande flexibilité et d’un contrôle plus étroit de l’utilisation de la mémoire. Les mémoires tampons, via la sous-allocation, disposent de toutes les fonctionnalités nécessaires à la gestion de la mémoire de bas niveau.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Téléchargement de différents types de ressources](uploading-resources.md)<br/>                 | Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons. L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire. Montre également les différences entre les modèles D3D11 et D3D12 pour le téléchargement de différents types de ressources.<br/> |
| [Chargement de données de texture dans des mémoires tampons](upload-and-readback-of-texture-data.md)<br/> | Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas. Les mémoires tampons peuvent être utilisées de façon orthogonale et simultanée à partir de plusieurs parties du pipeline graphique, et sont très flexibles. <br/>                                                                                                                       |
| [Lire les données à l’aide d’une mémoire tampon](readback-data-using-heaps.md)<br/>                    | La lecture de données à partir du GPU, telles que la capture d’écran, implique l’utilisation du tas readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Gestion des ressources basée sur les délimiteurs](fence-based-resource-management.md)<br/>            | Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs. La mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un tas de chargement. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de la mémoire](memory-management.md)
</dt> </dl>

 

 





