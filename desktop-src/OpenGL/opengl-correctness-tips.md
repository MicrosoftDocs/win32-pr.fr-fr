---
title: Conseils d’exactitude OpenGL
description: Conseils d’exactitude OpenGL
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, conseils d’exactitude
- OpenGL, meilleures pratiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379804"
---
# <a name="opengl-correctness-tips"></a>Conseils d’exactitude OpenGL

Suivez ces instructions pour créer des applications OpenGL qui fonctionnent comme vous le souhaitez :

-   Supposons que le comportement d’erreur dans la partie d’une implémentation OpenGL peut changer dans une version ultérieure de OpenGL. La sémantique des erreurs OpenGL peut changer dans les révisions ultérieures.
-   Utilisez la matrice de projection pour réduire toutes les géométries à un seul plan. Si la matrice modelview est utilisée, les fonctionnalités OpenGL qui fonctionnent en coordonnées oculaires (telles que les plans d’éclairage et de découpage défini par l’application) peuvent échouer.
-   N’apportez pas de modifications importantes à une matrice unique. Par exemple, n’animez pas une rotation en appelant continuellement [**glRotate**](glrotate.md) avec un angle incrémentiel. Utilisez plutôt [**glLoadIdentity**](glloadidentity.md) pour initialiser la matrice donnée pour chaque frame, puis appelez **glRotate** avec l’angle complet souhaité pour ce frame.
-   Attendez-vous à ce que plusieurs passes dans une base de données de rendu génèrent les mêmes fragments de pixel uniquement si ce comportement est garanti par les règles d’invariance établies pour une implémentation OpenGL conforme. Dans le cas contraire, plusieurs passes peuvent générer des ensembles différents de fragments.
-   Ne vous attendez pas à ce que les erreurs soient signalées lors de la définition d’une liste d’affichage. Les commandes d’une liste d’affichage génèrent des erreurs uniquement lorsque la liste est exécutée.
-   Pour optimiser le fonctionnement de la mémoire tampon de profondeur, placez le plan near frustum le plus éloigné possible du point de vue.
-   Appelez [**glFlush**](glflush.md) pour forcer l’exécution de toutes les commandes OpenGL précédentes. Ne comptez pas sur [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ou [**glIsEnabled**](glisenabled.md) pour vider le flux de rendu. Les commandes de requête vident la plus grande partie du flux nécessaire pour retourner des données valides, mais ne terminent pas nécessairement toutes les commandes de rendu en attente.
-   Désactivez le tramage lors du rendu des images préfondues (par exemple, quand [**glCopyPixels**](glcopypixels.md) est appelé).
-   Utilisez la plage complète de la mémoire tampon d’accumulation. Par exemple, si vous accumulez quatre images, mettez-les à l’échelle chaque mois au fur et à mesure qu’elles sont accumulées.
-   Pour obtenir une pixellisation exacte à deux dimensions, spécifiez avec soin la projection orthographique et les vertex des primitives à pixelliser. Spécifiez la projection orthographique avec des coordonnées entières, comme indiqué dans l’exemple suivant.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    La *largeur* et la *hauteur* des paramètres sont les dimensions de la fenêtre d’affichage. À partir de cette matrice de projection, placez les positions de polygones et d’images de pixels aux coordonnées entières pour pixelliser de manière prévisible. Par exemple, [glRecti](glrect-functions.md)(0, 0, 1, 1) remplit de manière fiable le pixel inférieur gauche de la fenêtre d’affichage, tandis que [glRasterPos2i](glrasterpos-functions.md)(0, 0) place de manière fiable une image non zoomée au pixel inférieur gauche de la fenêtre d’affichage. Toutefois, les vertex point, les sommets de ligne et les positions de bitmap doivent être placés à des emplacements demi-entiers. Par exemple, une ligne dessinée de (*x* (1), 0,5) à (*x* (2), 0,5) est rendue de manière fiable le long de la ligne inférieure des pixels dans la fenêtre d’affichage, et un point dessiné à (0,5, 0,5) remplit de manière fiable le même pixel que glRecti (0, 0, 1, 1).

    Une compromission optimale qui permet de spécifier toutes les primitives à des positions entières, tout en garantissant une pixellisation prévisible, consiste à traduire *x* et *y* par 0,375, comme illustré dans l’exemple de code suivant. Une telle traduction maintient les bords d’image de polygone et de pixel en toute sécurité à l’écart des centres de pixels, tout en déplaçant les sommets de ligne suffisamment près des centres de pixels.

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   Évitez d’utiliser des coordonnées de vertex *w* négatives et des coordonnées de texture *q* négatives. OpenGL peut ne pas découper de telles coordonnées correctement et peut faire des erreurs d’interpolation lors de la définition de primitives d’ombrage définies par ces coordonnées.

 

 




