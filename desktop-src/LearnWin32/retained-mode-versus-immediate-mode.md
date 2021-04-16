---
title: Mode de conservation et mode immédiat
description: Les API Graphics peuvent être divisées en API en mode mémorisé et en API en mode immédiat.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104565825"
---
# <a name="retained-mode-versus-immediate-mode"></a>Mode de conservation et mode immédiat

Les API Graphics peuvent être divisées en API *en mode mémorisé* et *en API en mode immédiat* . Direct2D est une API en mode immédiat. Windows Presentation Foundation (WPF) est un exemple d’API en mode conservé.

Une API en mode mémorisé est déclarative. L’application construit une scène à partir de primitives graphiques, telles que des formes et des lignes. La bibliothèque Graphics stocke un modèle de la scène en mémoire. Pour dessiner un frame, la bibliothèque de graphiques transforme la scène en un ensemble de commandes de dessin. Entre les frames, la bibliothèque Graphics conserve la scène en mémoire. Pour modifier ce qui est affiché, l’application émet une commande pour mettre à jour la scène, par exemple pour ajouter ou supprimer une forme. La bibliothèque est alors chargée de redessiner la scène.

![diagramme qui affiche des graphiques en mode mémorisé.](images/graphics06.png)

Une API en mode immédiat est procédurale. Chaque fois qu’un nouveau frame est dessiné, l’application émet directement les commandes de dessin. La bibliothèque Graphics ne stocke pas de modèle de scène entre les frames. Au lieu de cela, l’application effectue le suivi de la scène.

![diagramme qui affiche des graphiques en mode immédiat.](images/graphics07.png)

Les API en mode mémorisé peuvent être plus simples à utiliser, car l’API effectue davantage de tâches pour vous, telles que l’initialisation, la maintenance de l’État et le nettoyage. En revanche, ils sont souvent moins flexibles, car l’API impose son propre modèle de scène. En outre, une API en mode mémorisé peut avoir des exigences de mémoire plus élevées, car elle doit fournir un modèle de scène à usage général. Avec une API en mode immédiat, vous pouvez implémenter des optimisations ciblées.

## <a name="next"></a>Suivant

[Votre premier programme Direct2D](your-first-direct2d-program.md)

 

 




