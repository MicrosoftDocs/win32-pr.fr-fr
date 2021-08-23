---
title: Découpage (OpenGL)
description: Le découpage se produit en deux étapes
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline de traitement OpenGL, découpage
- découpage OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb518b9208b73dad2071531f6a30cdff6cab2ec5dcbe937fa3e66fea8bb0a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289039"
---
# <a name="clipping-opengl"></a>Découpage (OpenGL)

Le découpage se produit en deux étapes :

1.  **Affichez le volume clippingApplication de découpage spécifique.** Immédiatement après l’assemblage des primitives, elles sont découpées en coordonnées oculaires, si nécessaire, pour tous les plans de découpage que vous avez définis avec [**glClipPlane**](glclipplane.md). (OpenGL requiert la prise en charge d’au moins six plans de découpage spécifiques à l’application.)
2.  Les primitives sont transformées par la matrice de projection en coordonnées de clip et découpées par le volume de la vue correspondante. Cette matrice peut être contrôlée par les fonctions de transformation de matrice (consultez [transformations de matrice](matrix-transformations.md)), mais elle est généralement spécifiée par [**glFrustum**](glfrustum.md) ou [**glOrtho**](glortho.md).

Les points, les segments de ligne et les polygones sont gérés différemment lors du découpage :

-   Les points sont conservés dans leur état d’origine (s’ils sont à l’intérieur du volume du clip) ou ignorés (s’ils sont en dehors du volume du clip).
-   Si des parties de segments de ligne ou de polygones se trouvent en dehors du volume du clip, de nouveaux vertex sont générés au niveau des points de séquence.
-   Pour les polygones, il peut être nécessaire de construire un bord entier entre les nouveaux vertex générés au niveau des points de séquence.
-   Pour les segments de ligne et les polygones qui sont découpés, les informations d’indicateur de périphérie, de couleur et de texture sont affectées à tous les nouveaux vertex.

 

 




