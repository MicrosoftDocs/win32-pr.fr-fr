---
title: Sous-allocation au sein des tampons
description: Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU. Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63175bdb8b3937a01abe3ffc57032db78ea978768ee19e2c31d0c50db4103573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123812"
---
# <a name="suballocation-within-buffers"></a>Sous-allocation au sein des tampons

Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU. Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.

Comme pour D3D11, les applications dans D3D12 doivent toujours déclarer l’utilisation de la mémoire lors de l’allocation de mémoires tampons dans D3D12 par rapport aux ressources dynamiques/intermédiaires dans D3D11, mais dans D3D12, les développeurs disposent d’une plus grande flexibilité et d’un contrôle plus étroit de l’utilisation de la mémoire. Les mémoires tampons, via la sous-allocation, disposent de toutes les fonctionnalités nécessaires à la gestion de la mémoire de bas niveau.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Téléchargement de différents types de ressources](uploading-resources.md)<br/>                 | Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons. L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire. Montre également les différences entre les modèles D3D11 et D3D12 pour le téléchargement de différents types de ressources.<br/> |
| [Chargement de données de texture dans des mémoires tampons](upload-and-readback-of-texture-data.md)<br/> | Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas. Les mémoires tampons peuvent être utilisées de façon orthogonale et simultanée à partir de plusieurs parties du pipeline graphique, et sont très flexibles. <br/>                                                                                                                       |
| [Lire les données à l’aide d’une mémoire tampon](readback-data-using-heaps.md)<br/>                    | La lecture de données à partir du GPU, telles que la capture d’écran, implique l’utilisation du tas readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Gestion des ressources en fonction des limites](fence-based-resource-management.md)<br/>            | Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs. la mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un segment de Télécharger. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de la mémoire](memory-management.md)
</dt> </dl>

 

 





