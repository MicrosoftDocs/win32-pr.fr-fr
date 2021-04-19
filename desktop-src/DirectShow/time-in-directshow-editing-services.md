---
description: Heure dans les services de modification DirectShow
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Heure dans les services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421831742a2805f58d61c2258dad89d339131f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523710"
---
# <a name="time-in-directshow-editing-services"></a>Heure dans les services de modification DirectShow

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Pour modifier la vidéo, vous devez utiliser des concepts de minuterie importants. Par exemple :

-   Chaque clip a une durée.
-   Les clips, les transitions et les effets apparaissent à certains moments dans un projet.
-   La vidéo a une fréquence d’images, exprimée en images par seconde (FPS).

Les [services d’édition DirectShow](directshow-editing-services.md) (des) fournissent différentes méthodes qui définissent ou récupèrent les heures et les fréquences d’images. La signification de ces valeurs dépend du contexte.

**Valeurs d’heure**

Lorsqu’un paramètre exprime une heure, trois significations distinctes sont possibles :

-   *Heure* de la chronologie : l’heure par rapport au début de la chronologie. Par exemple, un clip peut démarrer 2 secondes dans la chronologie, ou une transition peut se produire 15 secondes dans la chronologie. La chronologie détermine le projet rendu final. vous pouvez donc considérer l’heure de la chronologie comme « heure du projet ».
-   *Heure du média*: point dans un fichier source relatif au début du fichier, tel qu’il a été atteint lors de la lecture normale. Par exemple, si vous avez un fichier vidéo de 10 secondes, le point au milieu du fichier se produit à 5 secondes, exprimé sous la forme d’un temps de support.
-   *Heure parente*: heure relative à un objet dans la chronologie. Par exemple, si un objet démarre à 8 secondes sur la chronologie et contient un autre objet qui commence à 10 secondes sur la chronologie, l’objet enfant démarre à 2 secondes par rapport au parent. Les suivis virtuels commencent à une heure égale à zéro, par rapport à la chronologie. Ainsi, pour tout objet dans une piste virtuelle, l’heure parente est égale à l’heure de la chronologie.

L’heure du média s’applique uniquement aux objets sources. Chaque objet source a une heure de début de support et une heure d’arrêt de support. Supposons, par exemple, que vous avez un clip vidéo de 10 secondes et que vous ne souhaitez utiliser que 5 secondes à partir du milieu du clip, en ajustant les 2 premières secondes et les 3 dernières secondes à partir du clip. Si vous souhaitez que le clip apparaisse 20 secondes dans le projet (en supposant une vitesse de lecture normale), vous devez spécifier les heures de démarrage et d’arrêt suivantes.

-   Début du média : 2 secondes
-   Arrêt du support : 7 secondes
-   Début de la chronologie : 20 secondes
-   Arrêt de la chronologie : 25 secondes

    ![insertion d’un clip source sur une chronologie](images/des-time1.png)

**Fréquences d’images**

La fréquence d’images est la « vitesse » d’un flux multimédia, mesurée en images par seconde. Comme avec les valeurs d’heure, la signification d’une fréquence d’images dépend du contexte :

-   **Fréquence d’images de sortie :** Fréquence d’images du projet rendu final, définie par le groupe. Lorsque vous affichez le projet, chaque groupe devient un flux de média distinct avec sa propre fréquence d’images.
-   **Fréquence d’images source :** Fréquence d’images dans laquelle le fichier source a été initialement créé. La fréquence d’images créée ne doit pas nécessairement correspondre à la fréquence d’images de sortie du groupe. DES met automatiquement en exemple ou sous-échantillonner le fichier en fonction DES besoins. Pour la plupart des formats de média, DES peuvent déterminer la fréquence d’images en examinant le format. Une séquence DIB est une exception. vous devez spécifier la fréquence d’images d’une séquence DIB. (Pour plus d’informations, consultez [utilisation des sources](working-with-sources.md).)

**Vitesse de lecture :** Vitesse apparente d’un élément source lorsqu’il apparaît dans le projet. Par exemple, une vidéo de 10 secondes peut s’ajuster à 5 secondes sur la chronologie. Par conséquent, la vitesse du clip augmente d’un facteur de 2, comme illustré dans le diagramme suivant.

![exécution d’une source plus rapide](images/des-time2.png)

(Avec une source audio, le pas se décale également.) La formule suivante détermine la vitesse de lecture d’un élément source :

-   Taux de lecture = (Media Stop – Start Media Start)/(chronologie Stop – Timeline Start)

Notez que chacun de ces trois tarifs est indépendant des autres :

-   Vous pouvez accélérer ou ralentir un clip en ajustant les temps de support. Cela n’affecte pas la fréquence d’images de la sortie finale.
-   Vous pouvez augmenter ou diminuer la fréquence d’images de sortie sans affecter la vitesse de lecture d’un fichier.
-   Vous pouvez mélanger, au sein du même groupe, des fichiers sources qui ont des fréquences d’images créées différentes, et les comporteront un échantillon ou sous-échantillonner chaque clip pour qu’il corresponde à la fréquence d’images du groupe.

Quand vous effectuez le rendu d’un projet, toutes les heures sont arrondies à la limite d’image la plus proche, comme déterminé par la fréquence d’images de groupe. Par exemple, supposons qu’un groupe vidéo a une fréquence d’images de 30 i/s. Chaque trame est d’environ 33 millisecondes (MS). Supposons que vous ajoutiez un élément source 1,68 seconde à la chronologie, en commençant à l’heure zéro. La source ne se termine pas exactement sur une limite de cadre, donc DES arrondit le temps d’arrêt à 1,6666 secondes (50 frames). Si vous recherchez 1,68 secondes dans le projet rendu, vous recherchez en fait au-delà de la fin de la source, le frame 51ème.

Toutefois, les ne remplacent pas l’heure d’arrêt de la source. Vous pouvez modifier ultérieurement la fréquence d’images du groupe ou déplacer la source vers un nouvel emplacement dans la chronologie où elle est arrondie différemment. Par conséquent, l’algorithme DES conserve l’heure d’arrêt d’origine et arrondit uniquement lorsque cela est nécessaire. Pour plus d’informations, consultez [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec les services d’édition DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



