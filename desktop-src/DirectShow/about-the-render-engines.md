---
description: À propos des moteurs de rendu
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: À propos des moteurs de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522236"
---
# <a name="about-the-render-engines"></a>À propos des moteurs de rendu

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Cet article décrit comment les [services d’édition DirectShow](directshow-editing-services.md) affichent un projet de montage vidéo.

Dans DES, un projet est représenté sous la forme d’une chronologie. La chronologie est utile, car elle simplifie les tâches les plus courantes lors de l’édition vidéo, telles que la réorganisation des éléments sources et l’ajout d’effets vidéo. L’architecture du flux DirectShow, en revanche, nécessite un graphique de filtre. Par conséquent, pour restituer votre projet, vous devez convertir une chronologie en un graphique de filtre. Le composant qui s’en sert est appelé *moteur de rendu*. DirectShow fournit deux moteurs de rendu :

-   Moteur de rendu de base : crée un graphique de filtre qui fournit une sortie non compressée.
-   Moteur de rendu intelligent : crée un graphique de filtre qui fournit une sortie compressée.

Le moteur de rendu intelligent utilise la recompression intelligente pour améliorer les performances. Avec la recompression intelligente, les fichiers sources sont recompressés uniquement lorsque le format de fichier d’origine est différent du format de sortie final. Si les formats correspondent, la source n’est jamais décompressée. La recompression intelligente est prise en charge uniquement pour la compression vidéo, et non pour la compression audio.

Pour la version préliminaire, utilisez le moteur de rendu de base. Le moteur de rendu intelligent peut également afficher un aperçu, mais moins efficacement car il doit décompresser le flux compressé. Pour écrire des fichiers, utilisez le moteur de rendu intelligent si vous souhaitez la recompression intelligente. Dans le cas contraire, utilisez le moteur de rendu de base. La recompression intelligente peut réduire de manière considérable le temps nécessaire à l’écriture du fichier.

> [!IMPORTANT]
> N’utilisez pas le moteur de rendu intelligent pour lire ou écrire des fichiers Windows Media.

 

> [!IMPORTANT]
> Les deux moteurs de rendu créent une fenêtre invisible qui traite les messages. Le thread qui crée le moteur de rendu doit avoir une boucle de message pour distribuer les messages. En outre, ce thread ne doit pas quitter tant que le moteur de rendu et le gestionnaire de graphes de filtre ne sont pas libérés. Dans le cas contraire, l’application peut se bloquer.

 

Construction du graphique de filtre

Le graphique de filtre est construit en deux étapes. Dans la première étape, le moteur de rendu construit un « frontal », qui est un graphique de filtre partiel. Le diagramme suivant illustre un frontal classique :

![filtrer le graphique frontal](images/rendeng1.png)

Les sous-systèmes contiennent différents filtres spécialisés, que le moteur de rendu assemble automatiquement. Le serveur frontal contient une broche de sortie pour chaque groupe dans la chronologie. Les broches de sortie fournissent des données non compressées si vous utilisez le moteur de rendu de base, ou des données compressées si vous utilisez le moteur de rendu intelligent.

Dans la deuxième étape, les broches de sortie sont connectées aux filtres de rendu. Pour la version préliminaire, les filtres de rendu sont des convertisseurs vidéo et audio. Pour l’écriture de fichier, les filtres de rendu sont des filtres multiplexeur (multiplexeur) et des filtres d’écriture de fichier.

![remplissage du graphique de filtre](images/rendeng2.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Aperçu d’un projet](previewing-a-project.md)
</dt> <dt>

[Écriture d’un projet dans un fichier](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



