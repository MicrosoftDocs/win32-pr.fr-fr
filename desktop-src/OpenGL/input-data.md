---
title: Données d’entrée
description: Le pipeline OpenGL vous oblige à entrer plusieurs types de données
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline de traitement OpenGL, données d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509380"
---
# <a name="input-data"></a>Données d’entrée

Le pipeline OpenGL vous oblige à entrer plusieurs types de données :

-   **Vertex**. Les vertex décrivent la forme de l’objet géométrique souhaité. Pour spécifier des vertex, utilisez les fonctions [**\* glVertex**](glvertex-functions.md) conjointement à [**glBegin**](glbegin.md) et [**glEnd**](glend.md) pour créer un point, une ligne ou un polygone. Vous pouvez également utiliser [**glRect**](glrect-functions.md) pour décrire un rectangle entier à un moment donné.
-   **Indicateur de périphérie**. Par défaut, tous les bords des polygones sont des bords limites. Utilisez [**glEdgeFlag \***](gledgeflag-functions.md) pour définir explicitement l’indicateur de périphérie.
-   **Position de la trame actuelle**. Spécifié avec [**glRasterPos \***](glrasterpos-functions.md), la position raster actuelle est utilisée pour déterminer les coordonnées raster pour les opérations de dessin de pixel et de bitmap.
-   **Normal actuel**. Un vecteur normal associé à un vertex particulier détermine la façon dont une surface au niveau de ce vertex est orientée dans l’espace tridimensionnel. Cela affecte à son tour la quantité de lumière reçue par un vertex particulier. Utilisez [**glNormal \***](glnormal-functions.md) pour spécifier un vecteur normal.
-   **Couleur actuelle**. La couleur d’un vertex, ainsi que les conditions d’éclairage, déterminent la couleur finale et allumée. La couleur est spécifiée [**avec \* glColor**](glcolor-functions.md) en mode RVBA, ou avec [**glIndex \***](glindex-functions.md) si en mode d’index des couleurs.
-   **Coordonnées de texture actuelles**. Spécifié avec [**glTexCoord \***](gltexcoord-functions.md), les coordonnées de texture déterminent l’emplacement dans une carte de texture à associer à un vertex d’un objet.

> [!Note]  
> Quand **glVertex \*** est appelé, le vertex obtenu hérite de l’indicateur de bord actuel, de la couleur normale, de la couleur et des coordonnées de texture. Par conséquent **, \* glEdgeFlag**, **glNormal \***, **\* glColor** et **glTexCoord \*** doivent être appelés avant **glVertex \***, s’ils doivent affecter le vertex résultant.

 

 

 




