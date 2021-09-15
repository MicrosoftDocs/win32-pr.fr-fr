---
description: 'les services de Windows GDI+ appartiennent aux trois grandes catégories suivantes :'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Les trois parties de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521500"
---
# <a name="the-three-parts-of-gdi"></a>Les trois parties de GDI+

les services de Windows GDI+ appartiennent aux trois grandes catégories suivantes :

-   [2D (graphismes vectoriels)](#2-d-vector-graphics)
-   [Images](#imaging)
-   [Typographie](#typography)

## <a name="2-d-vector-graphics"></a>2D (graphismes vectoriels)

Les graphiques vectoriels impliquent le dessin de primitives (telles que des lignes, des courbes et des figures) qui sont spécifiées par des ensembles de points sur un système de coordonnées. Par exemple, une ligne droite peut être spécifiée par ses deux points de terminaison, et un rectangle peut être spécifié par un point indiquant l’emplacement de son coin supérieur gauche et une paire de nombres indiquant sa largeur et sa hauteur. Un chemin d’accès simple peut être spécifié par un tableau de points à connecter par des lignes droites. Une spline de Bézier est une courbe sophistiquée spécifiée par quatre points de contrôle.

GDI+ fournit des classes qui stockent des informations sur les primitives elles-mêmes, les classes qui stockent des informations sur la façon dont les primitives sont dessinées, et les classes qui effectuent réellement le dessin. Par exemple, la classe **Rect** stocke l’emplacement et la taille d’un rectangle ; la classe **Pen** stocke les informations sur la couleur de ligne, la largeur de ligne et le style de ligne. et la classe **Graphics** possède des méthodes pour dessiner des lignes, des rectangles, des chemins d’accès et d’autres figures. Il existe également plusieurs classes de **pinceau** qui stockent des informations sur la façon dont les figures et les tracés fermés doivent être remplis de couleurs ou de modèles.

## <a name="imaging"></a>Images

Certains genres d’images sont difficiles ou impossibles à afficher avec les techniques des graphiques vectoriels. Par exemple, les images sur les boutons de la barre d’outils et les images qui s’affichent sous forme d’icônes sont difficiles à spécifier en tant que collections de lignes et de courbes. Une photographie numérique haute résolution d’un stade de baseball surchargé serait encore plus difficile à créer avec des techniques vectorielles. Les images de ce type sont stockées sous forme de bitmaps, des tableaux de nombres qui représentent les couleurs des points individuels sur l’écran. les structures de données qui stockent des informations sur les bitmaps ont tendance à être plus complexes que celles requises pour les graphiques vectoriels. par conséquent, il existe plusieurs classes GDI+ dédiées à cet effet. **CachedBitmap** est un exemple de cette classe qui est utilisée pour stocker une bitmap en mémoire pour un accès rapide et un affichage.

## <a name="typography"></a>Typographie

La typographie s’intéresse à l’affichage de texte dans diverses polices, tailles et styles. GDI+ fournit un niveau impressionnant de prise en charge pour cette tâche complexe. l’une des nouvelles fonctionnalités de GDI+ est l’anticrénelage de sous-pixels, qui donne au texte rendu sur un écran LCD une apparence plus lisse.

 

 



