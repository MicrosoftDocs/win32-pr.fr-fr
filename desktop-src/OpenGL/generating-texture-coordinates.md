---
title: Génération de coordonnées de texture
description: Plutôt que de fournir explicitement des coordonnées de texture, OpenGL peut les générer en tant que fonction d’autres données de vertex à l’aide de glTexGen.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Pipeline de traitement OpenGL, coordonnées de texture
- coordonnées de texture OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e7b6bc2d1263fac046f2d3078e2bab9bf8a789cacb335137ba27443b12b89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082279"
---
# <a name="generating-texture-coordinates"></a>Génération de coordonnées de texture

Plutôt que de fournir explicitement des coordonnées de texture, OpenGL peut les générer en tant que fonction d’autres données de vertex à l’aide de [glTexGen \* ](gltexgen-functions.md). Une fois les coordonnées de texture spécifiées ou générées, elles sont transformées par la matrice de texture. Cette matrice est contrôlée avec les mêmes fonctions que celles utilisées pour les transformations de matrice (consultez [transformations de matrice](matrix-transformations.md)).

 

 




