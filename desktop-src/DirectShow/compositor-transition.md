---
description: Transition de compositeur
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transition de compositeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566262"
---
# <a name="compositor-transition"></a>Transition de compositeur

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La transition de compositeur composite composite un sous-rectangle du premier plan dans un rectangle désigné sur l’arrière-plan, sans modifier le reste de l’arrière-plan. Utilisez cette transition pour créer des effets de fractionnement ou d’image en image.

L’illustration suivante montre la transition de compositeur :

![transition de compositeur](images/trans-compositor.png)

ID de classe (CLSID) : {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

Nom de la variable CLSID : CLSID \_ DxtCompositor

Nom convivial : « DxtCompositor »

Propriétés



| Propriété   | Type | Default | Description                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Hauteur     | long | 0       | Hauteur, en pixels, du rectangle cible.                     |
| OffsetX    | long | 0       | Décalage horizontal du rectangle cible, en pixels.          |
| OffsetY    | long | 0       | Décalage vertical du rectangle cible, en pixels.            |
| SrcHeight  | long | 0       | Hauteur du sous-rectangle sur la source, en pixels.       |
| SrcOffsetX | long | 0       | Coordonnée x du sous-rectangle sur la source, en pixels. |
| SrcOffsetY | long | 0       | Coordonnée y du sous-rectangle sur la source, en pixels. |
| SrcWidth   | long | 0       | Largeur du sous-rectangle sur la source, en pixels.        |
| Largeur      | long | 0       | Largeur du rectangle cible, en pixels.                      |



 

Le diagramme suivant illustre ces propriétés :

![Propriétés de compositeur](images/compmeasure.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transitions et effets](transitions-and-effects.md)
</dt> </dl>

 

 



