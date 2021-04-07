---
title: Effets graphiques
description: Liste des fonctionnalités qui doivent être désactivées lors de l’exécution en tant que session à distance dans un environnement de Services Bureau à distance.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f850b8bac5d084419b1f15c2e0efe619da5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940007"
---
# <a name="graphic-effects"></a>Effets graphiques

Un serveur de Services Bureau à distance s’appuie sur le réseau pour transmettre toutes les entrées et sorties à ses terminaux clients. Par conséquent, les applications qui effectuent une utilisation excessive des effets graphiques peuvent affecter les performances de tous les clients Services Bureau à distance en ralentissant le réseau. En outre, la vitesse de transmission plus lente sur un réseau peut entraîner l’affichage de ces effets spéciaux moins attrayants que dans un environnement vidéo local.

En particulier, les applications doivent désactiver ou réduire l’utilisation des fonctionnalités suivantes lors de l’exécution dans un environnement Services Bureau à distance en tant que session à distance :

-   Écrans de démarrage : informations graphiques relatives au produit ou à la société affichées au démarrage d’une application. La transmission d’un écran de démarrage à un client Connexion Bureau à distance (RDC) utilise une bande passante réseau supplémentaire et force l’utilisateur à attendre avant d’accéder à l’application.
-   Les animations, qui consomment le temps processeur et la bande passante réseau.
-   Entrée ou sortie directe à l’écran. Si vous avez besoin de lire des bits à partir de l’écran, maintenez une copie hors écran distincte de la mémoire tampon vidéo. De même, si vous devez effectuer une sortie d’écran élaborée, par exemple, en superposant plusieurs images pour arriver sur un écran composite final, effectuez cette opération dans une mémoire tampon hors écran, puis envoyez les résultats à la mémoire tampon vidéo réelle.

Pour plus d’informations sur la détection des sessions à distance, consultez [détection de l’environnement de services Bureau à distance](detecting-the-terminal-services-environment.md).

Utilisez la bibliothèque MFC (Microsoft Foundation Class), le cas échéant, dans la mesure du possible. MFC contient une longue liste de classes essayées et vraies pour effectuer une grande variété de tâches. La plupart de ces classes fonctionnent bien dans un environnement de Services Bureau à distance, généralement bien mieux que les solutions remaniées. Un bon exemple est la classe qui fournit le texte d’aide contextuelle : le texte d’aide qui s’affiche à l’écran lorsque le pointeur de la souris se trouve au-dessus d’un bouton ou d’un élément de menu. Si une application utilise l’implémentation MFC pour fournir cette fonctionnalité, elle fonctionnera raisonnablement bien sur le système de bureau. Toutefois, si l’application implémente cette fonctionnalité à l’aide de boîtes de dialogue ou d’une autre approche, le résultat final peut ne pas fonctionner aussi bien dans un environnement Services Bureau à distance.

 

 




