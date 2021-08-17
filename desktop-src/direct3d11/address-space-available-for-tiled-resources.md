---
title: Espace d’adressage disponible pour les ressources en mosaïque
description: Cette section spécifie l’espace d’adressage virtuel disponible pour les ressources en mosaïque.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5753fdb9d700689c6ebfffdae4368399c0e4bb36d328c9ff1a8cfc284005214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734281"
---
# <a name="address-space-available-for-tiled-resources"></a>Espace d’adressage disponible pour les ressources en mosaïque

Cette section spécifie l’espace d’adressage virtuel disponible pour les ressources en mosaïque.

Sur les systèmes d’exploitation 64 bits, au moins 40 bits d’espace d’adressage virtuel (1 téraoctet) sont disponibles.

Pour les systèmes d’exploitation 32 bits, l’espace d’adressage est de 32 bits (4 Go). Pour les systèmes ARM 32 bits, la création individuelle de ressources en mosaïque peut échouer si l’allocation utilise plus de 27 bits d’espace d’adressage (128 Mo). Cela comprend tous les remplissages masqués dans l’espace d’adressage que le matériel peut utiliser pour des mipmaps, le remplissage de vignettes condensé et éventuellement le remplissage des dimensions de surface aux puissances de 2.

Sur les systèmes graphiques avec une table de page distincte pour l’unité de traitement graphique (GPU), la majeure partie de cet espace d’adressage est disponible pour les ressources GPU effectuées par l’application, bien que les allocations GPU effectuées par le pilote d’affichage tiennent dans le même espace.

Sur les systèmes futurs avec une table de pages partagée entre l’UC et le GPU, l’espace d’adressage disponible est partagé entre toutes les allocations de processeur et GPU dans un processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres de création de ressources en mosaïque](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




