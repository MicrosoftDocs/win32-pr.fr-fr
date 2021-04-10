---
title: Modèle d’exécution
description: Modèle d’exécution
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modèle d’exécution
- modèle d’exécution OpenGL
- OpenGL, modèle client/serveur
- modèle client/serveur OpenGL
- OpenGL, transparent pour le réseau
- framebuffers, modèle d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940225"
---
# <a name="execution-model"></a>Modèle d’exécution

Le modèle d’interprétation des commandes OpenGL est client/serveur. Le code d’application (le client) émet des commandes qui sont interprétées et traitées par OpenGL (le serveur). Le serveur peut s’exécuter ou non sur le même ordinateur que le client. Dans ce sens, OpenGL est transparent pour le réseau. Un serveur peut gérer plusieurs contextes OpenGL, chacun d’eux étant un État OpenGL encapsulé. Un client peut se connecter à l’un de ces contextes. Le protocole réseau requis peut être implémenté en augmentant un protocole existant (tel que celui du système de fenêtre X) ou en utilisant un protocole indépendant. Aucune commande OpenGL n’est fournie pour obtenir une entrée d’utilisateur.

Le système de fenêtre qui alloue des ressources trame contrôle finalement les effets des commandes OpenGL sur le trame. Le système de fenêtre :

-   Détermine les parties de l’trame OpenGL qui peuvent accéder à un moment donné.
-   Communique avec OpenGL sur la structure de ces parties.

Par conséquent, il n’existe aucune commande OpenGL pour configurer trame ou initialiser OpenGL. La configuration de la mémoire tampon de frame est effectuée en dehors d’OpenGL conjointement avec le système Windows. L’initialisation OpenGL a lieu lorsque le système de fenêtres alloue une fenêtre pour le rendu OpenGL.

 

 




