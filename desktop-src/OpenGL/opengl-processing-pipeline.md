---
title: Pipeline de traitement OpenGL
description: Pipeline de traitement OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline de traitement
- pipeline de traitement OpenGL
- pipeline OpenGL
- framebuffers, pipeline de traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b52568de344404e9bddbedbacc40beda064b09d3e3af96c2657f670e677c32a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936862"
---
# <a name="opengl-processing-pipeline"></a>Pipeline de traitement OpenGL

De nombreuses fonctions OpenGL sont utilisées spécifiquement pour dessiner des objets tels que des points, des lignes, des polygones et des bitmaps. Certaines fonctions contrôlent la façon dont une partie de ce dessin se produit (par exemple, celles qui permettent l’anticrénelage ou la texturation). D’autres fonctions sont spécifiquement concernées par la manipulation de trame. Les rubriques de cette section décrivent comment toutes les fonctions OpenGL fonctionnent ensemble pour créer le pipeline de traitement OpenGL. Cette section examine également de plus près les étapes dans lesquelles les données sont réellement traitées et associe ces étapes aux fonctions OpenGL.

Le diagramme suivant détaille le pipeline de traitement OpenGL. Pour la plupart du pipeline, vous pouvez voir trois flèches verticales entre les principales étapes. Ces flèches représentent des vertex et les deux types de données principaux qui peuvent être associés à des vertex : des valeurs de couleur et des coordonnées de texture. Notez également que les vertex sont assemblés en primitives, puis en fragments et enfin en pixels dans le trame. Cette progression est traitée plus en détail dans les [vertex](vertices.md), les [primitives](primitives.md), les [fragments](fragments.md)et les [pixels](pixels.md).

![Diagramme montrant le pipeline de traitement OpenGL.](images/proc01.png)

 

 




