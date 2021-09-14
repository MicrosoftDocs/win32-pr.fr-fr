---
title: Redimensionnement d’un pool de vignettes
description: Utilisez l’API ID3D11DeviceContext2 ResizeTilePool pour augmenter un pool de mosaïques si l’application a besoin d’une plus grande plage de travail pour le mappage des ressources en mosaïques, ou pour réduire l’espace nécessaire.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86368da46f7c2219f42b5ecbc122b79fee19e72c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918523"
---
# <a name="tile-pool-resizing"></a>Redimensionnement d’un pool de vignettes

Utilisez l’API [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) pour augmenter un pool de mosaïques si l’application a besoin d’une plus grande plage de travail pour le mappage des ressources en mosaïque, ou pour réduire l’espace nécessaire. Une autre option pour les applications consiste à allouer des pools de mosaïques supplémentaires pour les nouvelles ressources en mosaïque. Toutefois, si une seule ressource en mosaïque nécessite plus d’espace que la première disponible dans son pool de mosaïques, la croissance du pool de mosaïques est une bonne option. Une ressource en mosaïque ne peut pas avoir de mappages dans plusieurs pools de mosaïques en même temps.

Lorsqu’un pool de mosaïques est cultivé, des vignettes supplémentaires sont ajoutées à la fin via une ou plusieurs nouvelles allocations par le pilote d’affichage. Cette répartition des allocations n’est pas visible pour l’application. La mémoire existante dans le pool de mosaïques n’est pas touchée et les mappages de ressources en mosaïque existants dans cette mémoire restent intacts.

Quand un pool de mosaïques est réduit, les vignettes sont supprimées de la fin. Les vignettes sont supprimées, même en dessous de la taille d’allocation initiale, jusqu’à 0, ce qui signifie que les nouveaux mappages ne peuvent pas être créés après la nouvelle taille. Toutefois, les mappages existants qui se trouvent au-delà de la fin de la nouvelle taille restent intacts et utilisables. Le pilote d’affichage conserve la mémoire aussi longtemps que les mappages à une partie des allocations utilisées par le pilote pour la mémoire du pool de mosaïques sont conservés. Si, après la réduction, une partie de la mémoire est restée active parce que les mappages de vignette pointent vers elle et que le pool de mosaïques est à nouveau recroître (d’une quantité quelconque), la mémoire existante est réutilisée avant toute allocation supplémentaire pour traiter la taille de l’opération d’augmentation.

Pour pouvoir économiser de la mémoire, une application doit non seulement réduire un pool de mosaïques, mais également supprimer/remapper des mappages existants au-delà de la fin de la nouvelle taille de pool de mosaïques plus petite.

Le fait de réduire (et de supprimer des mappages) ne produit pas nécessairement des économies immédiates de mémoire. La libération de la mémoire dépend de la granularité des allocations sous-jacentes du pilote d’affichage pour le pool de mosaïques. Quand la réduction est suffisante pour rendre inutilisée une allocation de pilote d’affichage, le pilote d’affichage peut la libérer. Si un pool de mosaïques a été augmenté, la réduction aux tailles précédentes (et la suppression ou le remappage des mappages de vignette correspondant) est susceptible de produire des économies de mémoire, bien que cela ne soit pas garanti dans le cas où les tailles n’étaient pas exactement alignées sur les tailles d’allocation sous-jacentes choisies par le pilote d’affichage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappages dans un pool de vignettes](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




