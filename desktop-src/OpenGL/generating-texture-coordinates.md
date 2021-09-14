---
title: Génération de coordonnées de texture
description: Plutôt que de fournir explicitement des coordonnées de texture, OpenGL peut les générer en tant que fonction d’autres données de vertex à l’aide de glTexGen.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Pipeline de traitement OpenGL, coordonnées de texture
- coordonnées de texture OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096658"
---
# <a name="generating-texture-coordinates"></a>Génération de coordonnées de texture

Plutôt que de fournir explicitement des coordonnées de texture, OpenGL peut les générer en tant que fonction d’autres données de vertex à l’aide de [glTexGen \* ](gltexgen-functions.md). Une fois les coordonnées de texture spécifiées ou générées, elles sont transformées par la matrice de texture. Cette matrice est contrôlée avec les mêmes fonctions que celles utilisées pour les transformations de matrice (consultez [transformations de matrice](matrix-transformations.md)).

 

 




