---
title: Données d’entrée
description: Le pipeline OpenGL vous oblige à entrer plusieurs types de données
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline de traitement OpenGL, données d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a588e60991ad068653890659e236f8a7a96e62cad524b13ea72bfd38fb5bba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937426"
---
# <a name="input-data"></a>Données d’entrée

Le pipeline OpenGL vous oblige à entrer plusieurs types de données :

-   **Vertex**. Les vertex décrivent la forme de l’objet géométrique souhaité. Pour spécifier des vertex, utilisez les fonctions [ * _ *glVertex \** _](glvertex-functions.md) conjointement avec [_ *glBegin* *](glbegin.md) et [**glEnd**](glend.md) pour créer un point, une ligne ou un polygone. Vous pouvez également utiliser [**glRect**](glrect-functions.md) pour décrire un rectangle entier à un moment donné.
-   **Indicateur de périphérie**. Par défaut, tous les bords des polygones sont des bords limites. Utilisez [**glEdgeFlag \***](gledgeflag-functions.md) pour définir explicitement l’indicateur de périphérie.
-   **Position de la trame actuelle**. Spécifié avec [**glRasterPos \***](glrasterpos-functions.md), la position raster actuelle est utilisée pour déterminer les coordonnées raster pour les opérations de dessin de pixel et de bitmap.
-   **Normal actuel**. Un vecteur normal associé à un vertex particulier détermine la façon dont une surface au niveau de ce vertex est orientée dans l’espace tridimensionnel. Cela affecte à son tour la quantité de lumière reçue par un vertex particulier. Utilisez [**glNormal \***](glnormal-functions.md) pour spécifier un vecteur normal.
-   **Couleur actuelle**. La couleur d’un vertex, ainsi que les conditions d’éclairage, déterminent la couleur finale et allumée. La couleur est spécifiée avec [ * *glColor \** _](glcolor-functions.md) if en mode RVBA, ou avec [_ *glIndex \** *](glindex-functions.md) en mode d’index des couleurs.
-   **Coordonnées de texture actuelles**. Spécifié avec [**glTexCoord \***](gltexcoord-functions.md), les coordonnées de texture déterminent l’emplacement dans une carte de texture à associer à un vertex d’un objet.

> [!Note]  
> Quand **glVertex \* *_ est appelé, le vertex obtenu hérite de l’indicateur de bord actuel, de la couleur normale, de la couleur et des coordonnées de texture. Par conséquent, _* glEdgeFlag \* *_,* _ glNormal \* *_,* _ glColor \* *_ et _* glTexCoord \* *_ doivent être appelés avant _* glVertex \***, s’ils doivent affecter le vertex résultant.

 

 

 




