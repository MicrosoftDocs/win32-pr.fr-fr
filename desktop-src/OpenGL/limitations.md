---
title: Limites
description: Limites
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL sur Windows, limitations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121318"
---
# <a name="limitations"></a>Limites

L’implémentation générique présente les limitations suivantes :

-   Impression.

    Vous pouvez imprimer une image OpenGL directement sur une imprimante en utilisant uniquement des fichiers. Pour plus d’informations, consultez [impression d’une image OpenGL](printing-an-opengl-image.md).

-   Les graphiques OpenGL et GDI ne peuvent pas être mélangés dans une fenêtre à double mémoire tampon.

    Une application peut directement dessiner des graphiques OpenGL et des graphiques GDI dans une fenêtre à une seule mise en mémoire tampon, mais pas dans une fenêtre à deux mémoires tampons.

-   Il n’y a pas de palettes de couleurs matérielles par fenêtre.

    Windows dispose d’une palette de couleurs matérielles système unique, qui s’applique à l’ensemble de l’écran. Une fenêtre OpenGL ne peut pas avoir sa propre palette matérielle, mais elle peut avoir sa propre palette logique. Pour ce faire, il doit devenir une application prenant en charge la palette. pour plus d’informations, consultez [Modes de couleurs OpenGL et gestion des palettes de Windows](opengl-color-modes-and-windows-palette-management.md).

-   Il n’existe aucune prise en charge directe pour le presse-papiers, l’échange dynamique de données (DDE) ou OLE.

    une fenêtre avec des graphiques OpenGL ne prend pas directement en charge ces fonctionnalités de Windows. Toutefois, il existe des solutions de contournement pour l’utilisation du presse-papiers. Pour plus d’informations, consultez [copie d’une image OpenGL dans le presse-papiers](copying-an-opengl-image-to-the-clipboard.md).

-   La bibliothèque de classes ininventor 2,0 C++ n’est pas incluse.

    La bibliothèque de classes d’inventaire, basée sur OpenGL, fournit des constructions de niveau supérieur pour la programmation de graphiques 3D. Elle n’est pas incluse dans la version actuelle de l’implémentation de OpenGL par Microsoft pour Windows.

-   Il n’existe aucune prise en charge des fonctionnalités de format de pixel suivantes : les images stéréoscopiques, les bitplanes alpha et les tampons auxiliaires.

    Toutefois, il existe une prise en charge de plusieurs mémoires tampons auxiliaires, notamment : tampon stencil, tampon d’accumulation, mémoire tampon d’arrière-plan (double mise en mémoire tampon), mémoire tampon plan Underlay et mémoire tampon de plan de profondeur (axe z).

 

 




