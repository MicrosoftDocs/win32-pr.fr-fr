---
title: Rastérisation
description: La pixellisation est le processus par lequel une primitive est convertie en une image à deux dimensions.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Pipeline de traitement OpenGL, pixellisation
- pixellisation de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192f8fdd919c14be4bd47688abf911b363e13f2e8ca9606f1943eb2956378ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776879"
---
# <a name="rasterizing"></a>Rastérisation

La *pixellisation* est le processus par lequel une primitive est convertie en une image à deux dimensions. Chaque point de cette image contient des informations telles que les données de couleur, de profondeur et de texture. Un point et les informations qui lui sont associées sont appelés *fragments*. La position raster actuelle, telle qu’elle est spécifiée avec [**glRasterPos \***](glrasterpos-functions.md), est utilisée de différentes façons pendant cette étape pour dessiner des pixels et des bitmaps. Différents problèmes surviennent lors de la pixellisation des points, des segments de ligne et des polygones. En outre, les rectangles de pixels et les bitmaps doivent être pixellisés.

Avec OpenGL, vous contrôlez la pixellisation à l’aide des fonctions suivantes :

-   Primitives. Contrôlez la façon dont les primitives sont pixellisées à l’aide des fonctions qui déterminent les dimensions et les modèles stipple : [**glPointSize**](glpointsize.md), [**glLineWidth**](gllinewidth.md), [**glLineStipple**](gllinestipple.md)et [**glPolygonStipple**](glpolygonstipple.md). Contrôlez la façon dont les faces arrière et arrière des polygones sont pixellisées avec [**glCullFace**](glcullface.md), [**glFrontFace**](glfrontface.md)et [**glPolygonMode**](glpolygonmode.md).
-   Hauteur. Plusieurs fonctions contrôlent le stockage des pixels et les modes de transfert. La fonction [ * *glPixelStore \** _](glpixelstore-functions.md) contrôle l’encodage des pixels dans la mémoire du client, tandis que [_*glPixelTransfer \**_](glpixeltransfer.md) et [_*glPixelMap \**_](glpixelmap.md) contrôlent le mode de traitement des pixels avant leur placement dans le trame. Spécifiez un rectangle de pixels avec [_ *glDrawPixels* *](gldrawpixels.md); Contrôlez sa pixellisation avec [**glPixelZoom**](glpixelzoom.md).
-   Bitmaps. Les bitmaps sont des rectangles de zéros et ceux qui spécifient un modèle particulier de fragments à produire. Chacun de ces fragments a les mêmes données associées. La fonction [**glBitmap**](glbitmap.md) spécifie une image bitmap.
-   Mémoire de texture. Lorsque la texturation est activée, la texturation mappe une partie d’une image de texture spécifiée sur chaque primitive. Ce mappage est effectué à l’aide de la couleur de l’image de texture à l’emplacement indiqué par les coordonnées de texture d’un fragment pour modifier la couleur RVBA du fragment. Spécifiez une image de texture avec [**glTexImage2D**](glteximage2d.md) ou [**glTexImage1D**](glteximage1d.md). Les fonctions [ * *glTexParameter \** _](gltexparameter-functions.md) et [_ *\* glTexEnv* *](gltexenv-functions.md) contrôlent la façon dont les valeurs de texture sont interprétées et appliquées à un fragment.
-   Vont. Pour fusionner une couleur de brouillard avec la couleur de surtexturation d’un fragment pixellisé, utilisez un facteur de fusion qui dépend de la distance entre le Eyepoint et le fragment. Utilisez [**glFog \***](glfog.md) pour spécifier la couleur de brouillard et le facteur de fusion.

 

 




