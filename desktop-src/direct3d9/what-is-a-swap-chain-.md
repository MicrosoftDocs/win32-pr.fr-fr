---
description: Une chaîne de permutation est une collection de mémoires tampons utilisées pour afficher des frames à l’utilisateur.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: Qu’est-ce qu’une chaîne de permutation ? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8fc1fd2d313c70a680d9b276a3aabedc6d8cff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200693"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>Qu’est-ce qu’une chaîne de permutation ? (Direct3D 9)

Une chaîne de permutation est une collection de mémoires tampons utilisées pour afficher des frames à l’utilisateur. Chaque fois qu’une application présente un nouveau Frame à afficher, la première mémoire tampon de la chaîne de permutation remplace la mémoire tampon affichée. Ce processus est appelé échange ou basculement.

Une carte graphique contient un pointeur vers une surface qui représente l’image affichée sur le moniteur, appelée une mémoire tampon d’avant. À mesure que le moniteur est actualisé, la carte graphique envoie le contenu de la mémoire tampon d’entrée à l’analyse à afficher. Toutefois, cela provoque un problème lors du rendu de graphiques en temps réel. Le cœur du problème est que les taux d’actualisation du moniteur sont très lents par rapport au reste de l’ordinateur. La plage des taux d’actualisation courants est comprise entre 60 Hz (60 fois par seconde) et 100 Hz. Si votre application met à jour la mémoire tampon d’avant pendant que l’analyse se trouve au milieu d’une actualisation, l’image affichée sera coupée en moitié avec la moitié supérieure de l’affichage contenant l’ancienne image et la moitié inférieure contenant la nouvelle image. Ce problème est connu sous le terme de « destruction ».

Direct3D met en œuvre deux options pour éviter le déchirement :

-   Option permettant d’autoriser uniquement les mises à jour du moniteur sur l’opération de retraçage vertical (ou de synchronisation verticale). En règle générale, une analyse actualise son image en déplaçant un pin clair horizontalement, zigzagging en haut à gauche de l’écran et en se terminant en bas à droite. Lorsque la broche légère atteint la partie inférieure, le moniteur réétalonne le code confidentiel clair en le replaçant en haut à gauche, afin que le processus puisse recommencer. Ce réétalonnage est appelé synchronisation verticale. Au cours d’une synchronisation verticale, le moniteur ne dessine rien. par conséquent, toute mise à jour de la mémoire tampon d’avant ne sera pas visible tant que le moniteur n’aura pas redessiné. La synchronisation verticale est relativement lente ; Toutefois, il n’est pas assez lent d’afficher une scène complexe pendant l’attente. Ce qui est nécessaire pour éviter le déchirement et être en mesure d’afficher des scènes complexes est un processus appelé mise en mémoire tampon d’arrière-plan.
-   Une option pour utiliser une technique appelée mise en mémoire tampon d’arrière-plan. La mise en mémoire tampon d’arrière-plan est le processus qui consiste à dessiner une scène sur une surface hors écran, appelée mémoire tampon d’arrière-plan. Notez que toute surface autre que la mémoire tampon d’avant est appelée une surface hors écran, car elle n’est jamais affichée directement par le moniteur. En utilisant une mémoire tampon d’arrière-plan, une application a la liberté de restituer une scène chaque fois que le système est inactif (autrement dit, aucun message Windows n’est en attente) sans avoir à prendre en compte la fréquence d’actualisation du moniteur. La mise en mémoire tampon d’arrière-plan améliore la façon dont et quand déplacer la mémoire tampon d’arrière-plan vers la mémoire tampon d’arrière-plan.

Le processus de déplacement de la mémoire tampon d’arrière-plan vers la mémoire tampon d’arrière-plan est appelé retournement de surface. Étant donné que la carte graphique utilise simplement un pointeur vers une surface pour représenter la mémoire tampon d’entrée, une simple modification de pointeur suffit pour définir la mémoire tampon d’arrière-plan sur la mémoire tampon d’entrée. Quand une application demande à Direct3D de présenter la mémoire tampon d’arrière-plan au tampon d’avant, Direct3D « retourne » simplement les deux pointeurs de surface. Le résultat est que la mémoire tampon d’arrière-plan est désormais la nouvelle mémoire tampon d’origine, et l’ancienne mémoire tampon d’arrière-plan est la nouvelle mémoire tampon d’arrière-plan. Un retournement de surface est appelé chaque fois qu’une application demande au périphérique Direct3D de présenter la mémoire tampon d’arrière-plan ; Toutefois, Direct3D peut être configuré pour mettre les demandes en file d’attente jusqu’à ce qu’une synchronisation verticale se produise. Cette option est appelée « intervalle de présentation de l’appareil Direct3D ». Notez que les données de la nouvelle mémoire tampon d’arrière-plan peuvent ne pas être réutilisables, en fonction de la façon dont une application spécifie la manière dont Direct3D doit gérer le basculement de surface. Le retournement de surface est essentiel dans les logiciels multimédia, d’animation et de jeu ; elle est équivalente à la façon dont vous pouvez effectuer une animation avec un bloc de papier. Sur chaque page, l’artiste modifie légèrement les chiffres, de sorte que lorsque vous retournez rapidement entre les feuilles, le dessin apparaît animé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Retournement des surfaces (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



