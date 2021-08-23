---
title: Opération OpenGL de base
description: Opération OpenGL de base
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, opérations de base
- OpenGL, traitement des données
- OpenGL, étapes de traitement
- OpenGL, afficher les listes
- afficher les listes OpenGL
- OpenGL, évaluateurs
- évaluateurs OpenGL
- OpenGL, opérations par vertex
- opérations par vertex OpenGL
- OpenGL, assembly primitif
- assembly primitif OpenGL
- OpenGL, pixellisation
- pixellisation OpenGL
- OpenGL, opérations par fragment
- opérations par fragment OpenGL
- framebuffers, opérations de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72f6abed7d06a93985b798e72efbf4d6ec0901e7ad9fb4614f5bf81590cefcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554713"
---
# <a name="basic-opengl-operation"></a>Opération OpenGL de base

Le diagramme suivant illustre comment OpenGL traite les données. Comme illustré, les commandes entrent à partir de la gauche et passent par un pipeline de traitement. Certaines commandes spécifient des objets géométriques à dessiner, tandis que d’autres contrôlent la façon dont les objets sont traités au cours des différentes étapes de traitement.

![Diagramme montrant les étapes du pipeline de traitement des données OpenGL.](images/basic01.png)

Les étapes de traitement de l’opération OpenGL de base sont les suivantes :

-   **Afficher la liste** Plutôt que de faire en sorte que toutes les commandes passent immédiatement par le pipeline, vous pouvez choisir de les accumuler dans une liste d’affichage pour les traiter ultérieurement.
-   **Évaluateur** L’étape de traitement de l’évaluateur offre un moyen efficace de calculer la géométrie des courbes et des surfaces en évaluant les commandes polynomiaux des valeurs d’entrée.
-   **Opérations par vertex et assembly primitif** OpenGL traite les primitivespoints géométriques, les segments de ligne et les polygonsall qui sont décrits par des vertex. Les vertex sont transformés et allumés, et les primitives sont ajustées à la fenêtre d’affichage en vue de la pixellisation.
-   **Pixellisation** L’étape de pixellisation produit une série d’adresses de tampons de trames et de valeurs associées à l’aide d’une description à deux dimensions d’un point, d’un segment de ligne ou d’un polygone. Chaque fragment produit est introduit dans la dernière étape, opérations par fragment.
-   **Opérations par fragment** Il s’agit des opérations finales effectuées sur les données avant qu’elles ne soient stockées sous la forme de pixels dans le trame.

    Les opérations par fragment incluent les mises à jour conditionnelles du trame en fonction des valeurs z entrantes et précédemment stockées (pour la mise en mémoire tampon z) et de la fusion des couleurs de pixels entrantes avec des couleurs stockées, ainsi que du masquage et d’autres opérations logiques sur les valeurs de pixel.

Les données peuvent être entrées sous la forme de pixels plutôt que de vertex. Les données sous la forme de pixels, telles que peuvent décrire une image à utiliser dans le mappage de texture, ignore la première étape de traitement décrite ci-dessus et est traitée en tant que pixels, dans l’étape des opérations de pixel. Opérations de pixel suivantes, les données de pixels sont :

-   Stocké en tant que mémoire de texture pour une utilisation à l’étape de pixellisation.
-   Pixellisé, avec les fragments résultants fusionnés dans le trame comme s’ils étaient générés à partir de données géométriques.

 

 




