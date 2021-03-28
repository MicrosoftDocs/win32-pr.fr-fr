---
description: Pour modifier une image stockée dans un métafichier amélioré, une application doit effectuer les tâches décrites dans la procédure suivante.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Modification d’un métafichier amélioré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114667"
---
# <a name="editing-an-enhanced-metafile"></a>Modification d’un métafichier amélioré

Pour modifier une image stockée dans un métafichier amélioré, une application doit effectuer les tâches décrites dans la procédure suivante.

**Pour modifier une image stockée dans un métafichier amélioré**

1.  Utilisez le test de positionnement pour capturer les coordonnées du curseur et récupérer la position de l’objet (trait, arc, Rectangle, ellipse, polygone ou forme irrégulière) que l’utilisateur souhaite modifier.
2.  Convertissez ces coordonnées en unités logiques (ou universelles).
3.  Appelez la fonction [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) et examinez chaque enregistrement de métafichier.
4.  Détermine si un enregistrement donné correspond à une fonction de dessin GDI.
5.  Si c’est le cas, déterminez si les coordonnées stockées dans l’enregistrement correspondent à la ligne, à l’arc, à l’ellipse ou à tout autre élément graphique qui croise les coordonnées spécifiées par l’utilisateur.
6.  Lors de la recherche de l’enregistrement correspondant à la sortie que l’utilisateur souhaite modifier, effacez l’objet sur l’écran qui correspond à l’enregistrement d’origine.
7.  Supprimez l’enregistrement correspondant du métafichier, en enregistrant un pointeur vers son emplacement.
8.  Permet à l’utilisateur de redessiner ou de remplacer l’objet.
9.  Convertissez les fonctions GDI utilisées pour dessiner le nouvel objet en un ou plusieurs enregistrements de métafichier amélioré.
10. Stockez ces enregistrements dans le métafichier amélioré.

 

 



