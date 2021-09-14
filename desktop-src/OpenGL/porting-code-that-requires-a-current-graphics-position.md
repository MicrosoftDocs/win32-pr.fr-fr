---
title: Code de port qui a besoin d’une position graphique actuelle
description: OpenGL ne conserve pas la position graphique actuelle. Les fonctions de l’IRIS du GL qui dépendent de la position graphique actuelle, telles que déplacer, dessiner et RMV, n’ont pas d’équivalents dans OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Portage de l’IRIS dans le GL, position graphique actuelle
- Portage à partir de IRIS GL, position graphique actuelle
- portage vers OpenGL à partir de IRIS GL, position graphique actuelle
- Portage OpenGL depuis IRIS GL, position graphique actuelle
- position graphique actuelle
- positions raster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119157"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Code de port qui a besoin d’une position graphique actuelle

OpenGL ne conserve pas la position graphique actuelle. Les fonctions de l’IRIS du GL qui dépendent de la position graphique actuelle, telles que **déplacer**, **dessiner** et **RMV**, n’ont pas d’équivalents dans OpenGL.

Les anciennes versions de IRIS GL comprenaient des commandes de dessin reposant sur la position graphique actuelle, bien que leur utilisation soit déconseillée. Vous devrez réécrire votre code si vous vous reposez sur la position graphique actuelle de quelque manière que ce soit, ou si vous utilisez l’une des routines suivantes :

-   **dessiner** et **déplacer**
-   **PMV**, **PDR** et **PCLOS**
-   **RDR**, **RMV**, **rpdr** et **rpmv**
-   **getgpos**

OpenGL présente un concept de position raster qui correspond à la position actuelle du caractère de l’IRIS du GL. Pour plus d’informations sur le positionnement de la trame, consultez [Portage d’opérations de pixels](porting-pixel-operations.md).

Cette rubrique contient des informations sur les éléments suivants.

-   [Portage de l’écran et des commandes de vidage de la mémoire tampon](porting-screen-and-buffer-clearing-commands.md)
-   [Fonctions de transformation et de matrice de Portage](porting-matrix-and-transformation-functions.md)
-   [Portage du code en mode MSINGLE](porting-msingle-mode-code.md)
-   [Portage de fonctions qui obtiennent des matrices et des transformations](porting-functions-that-get-matrices-and-transformations.md)
-   [Portage des Viewports, Screenmasks et Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Portage des plans de découpage](porting-clipping-planes.md)

 

 




