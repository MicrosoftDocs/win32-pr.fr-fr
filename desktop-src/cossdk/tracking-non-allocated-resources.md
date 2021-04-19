---
description: Suivi des ressources non allouées
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Suivi des ressources non allouées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513946"
---
# <a name="tracking-non-allocated-resources"></a>Suivi des ressources non allouées

Le gestionnaire de distribution peut effectuer le suivi d’une ressource qui n’est pas inventoriée, en fonction de la connaissance de la durée de vie de l’objet. Lorsqu’une ressource suivie non allouée est libérée, elle est détruite et n’est donc pas renvoyée à l’inventaire. Ce mode de suivi uniquement pour les ressources qui sont peu coûteuses à créer et à détruire est plus utile que de les stocker dans l’inventaire. Ce mode est également utile pour gérer un distributeur de mémoire ou pour une ressource difficile à inventorier, car il existe trop de types différents.

En mode suivi uniquement, un distributeur de ressources crée directement une ressource demandée au lieu de demander au gestionnaire de distribution d’en allouer un à partir de l’inventaire. Avant de renvoyer cette ressource au composant d’application demandeur, le distributeur de ressources indique au gestionnaire du distributeur d’effectuer le suivi de la ressource, ce qui garantit que même si le composant oublie de libérer la ressource, le gestionnaire du distributeur le fera quand la durée de vie du composant est supérieure à.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



