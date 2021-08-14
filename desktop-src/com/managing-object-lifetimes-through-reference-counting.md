---
title: Gestion des durées de vie des objets via le décompte de références
description: Gestion des durées de vie des objets via le décompte de références
ms.assetid: 7f9da5a9-0435-431c-8f90-56e2e489c431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f2c75352eef5680eb9a4d8367f76f88c19138dd834b71068740bee18f2315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310559"
---
# <a name="managing-object-lifetimes-through-reference-counting"></a>Gestion des durées de vie des objets via le décompte de références

Dans les systèmes d’objets traditionnels, le cycle de vie des objets, c’est-à-dire les problèmes liés à la création et à la suppression d’objets, est géré implicitement par le langage (ou le temps d’exécution du langage) ou explicitement par les programmeurs d’applications.

Dans un système évolutif et décentralisé constitué de composants réutilisés, il n’est plus vrai qu’un client, voire n’importe quel programmeur, « sache » toujours comment gérer la durée de vie d’un composant. Pour un client doté des privilèges de sécurité appropriés, il est toujours relativement facile de créer des objets via une requête simple, mais la suppression d’objets est une autre question. Il n’est pas toujours évident de préciser quand un objet n’est plus nécessaire et doit être supprimé. (Les lecteurs familiers avec les environnements de programmation récupérés par le garbage collector, tels que Java, peuvent être désaccords ; Toutefois, les objets Java ne s’étendent pas aux limites de l’ordinateur ou même du processus, et par conséquent, le garbage collection est limité aux objets qui résident dans un espace de processus unique. En outre, Java force l’utilisation d’un langage de programmation unique.) Même lorsque le client d’origine est terminé avec l’objet, il ne peut pas simplement arrêter l’objet, car d’autres clients ou clients peuvent toujours y avoir une référence.

Une façon de s’assurer qu’un objet n’est plus nécessaire est de dépendre entièrement d’un canal de communication sous-jacent pour informer le système lorsque toutes les connexions à un objet inter-processus ou inter-canaux ont disparu. Toutefois, les schémas qui utilisent cette méthode sont inacceptables pour plusieurs raisons. L’un des problèmes est qu’elle peut nécessiter une différence majeure entre le modèle de programmation inter-processus/réseau croisé et le modèle de programmation à processus unique. Dans le modèle de programmation inter-processus/réseau croisé, le système de communication fournit les hooks nécessaires à la gestion de la durée de vie des objets, tandis que dans le modèle de programmation à processus unique, les objets sont connectés directement sans canal de communication intermédiaire. Un autre problème est que ce schéma peut également entraîner une couche de logiciels fournis par le système qui interférerait avec les performances des composants dans le cas du processus in-process. En outre, un mécanisme basé sur la surveillance explicite n’aurait pas tendance à se mettre à l’échelle vers plusieurs milliers ou millions d’objets.

COM offre une approche évolutive et distribuée de cet ensemble de problèmes. Les clients disent à un objet lorsqu’ils l’utilisent et lorsqu’ils sont terminés, et les objets se suppriment lorsqu’ils ne sont plus nécessaires. Cette approche impose que tous les objets comptent des références à elles-mêmes. Des langages de programmation tels que Java, qui ont par nature leurs propres schémas de gestion de la durée de vie, comme garbage collection, peuvent utiliser le comptage de références de COM pour implémenter et utiliser les objets COM en interne, ce qui permet au programmeur d’éviter tout traitement.

Tout comme une application doit libérer de la mémoire qu’elle a allouée une fois que la mémoire n’est plus utilisée, un client d’un objet est chargé de libérer ses références à l’objet lorsque cet objet n’est plus nécessaire. Dans un système orienté objet, le client ne peut le faire qu’en donnant à l’objet une instruction de libération proprement dite.

Il est important qu’un objet soit libéré lorsqu’il n’est plus utilisé. La difficulté consiste à déterminer quand il est approprié de désallouer un objet. Cela est facile avec des variables automatiques (celles allouées sur la pile). elles ne peuvent pas être utilisées en dehors du bloc dans lequel elles sont déclarées, de sorte que le compilateur les libère lorsque la fin du bloc est atteinte. Pour les objets COM, qui sont alloués dynamiquement, il revient aux clients d’un objet de décider quand ils n’ont plus besoin d’utiliser l’objet, en particulier les objets locaux ou distants qui peuvent être utilisés par plusieurs clients en même temps. L’objet doit attendre la fin de l’exécution de tous les clients avant de se libérer. Étant donné que les objets COM sont manipulés via des pointeurs d’interface et peuvent être utilisés par des objets dans des processus différents ou sur d’autres ordinateurs, le système ne peut pas effectuer le suivi des clients d’un objet.

La méthode du COM pour déterminer quand il est approprié de libérer un objet est le décompte de références manuel. Chaque objet gère un nombre de références qui effectue le suivi du nombre de clients connectés, c’est-à-dire le nombre de pointeurs qui existent pour l’une de ses interfaces dans un client quelconque.

Pour plus d'informations, voir les rubriques suivantes :

-   [Implémentation du décompte de références](implementing-reference-counting.md)
-   [Règles pour la gestion des nombres de références](rules-for-managing-reference-counts.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation et implémentation de IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




