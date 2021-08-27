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
ms.openlocfilehash: e7cb7c3c06baa0a56f4c59b14744b73962fced369d56f00cbf887b9ae6d09e2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082459"
---
# <a name="execution-model"></a>Modèle d’exécution

Le modèle d’interprétation des commandes OpenGL est client/serveur. Le code d’application (le client) émet des commandes qui sont interprétées et traitées par OpenGL (le serveur). Le serveur peut s’exécuter ou non sur le même ordinateur que le client. Dans ce sens, OpenGL est transparent pour le réseau. Un serveur peut gérer plusieurs contextes OpenGL, chacun d’eux étant un État OpenGL encapsulé. Un client peut se connecter à l’un de ces contextes. Le protocole réseau requis peut être implémenté en augmentant un protocole existant (tel que celui du système de fenêtre X) ou en utilisant un protocole indépendant. Aucune commande OpenGL n’est fournie pour obtenir une entrée d’utilisateur.

Le système de fenêtre qui alloue des ressources trame contrôle finalement les effets des commandes OpenGL sur le trame. Le système de fenêtre :

-   Détermine les parties de l’trame OpenGL qui peuvent accéder à un moment donné.
-   Communique avec OpenGL sur la structure de ces parties.

Par conséquent, il n’existe aucune commande OpenGL pour configurer trame ou initialiser OpenGL. La configuration de la mémoire tampon de frame est effectuée en dehors d’OpenGL conjointement avec le système Windows. L’initialisation OpenGL a lieu lorsque le système de fenêtres alloue une fenêtre pour le rendu OpenGL.

 

 




