---
title: Portage des opérations de pixels
description: Portage des opérations de pixels
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Portage de l’IRIS dans le GL, pixels
- Portage à partir de IRIS GL, pixels
- portage vers OpenGL à partir de IRIS GL, pixels
- Portage OpenGL à partir de IRIS GL, pixels
- pixels, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc67a4c9224dbe6544c60cb205f8a192517af7f3ab16ba64134b4d55d1c8676f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132378"
---
# <a name="porting-pixel-operations"></a>Portage des opérations de pixels

Lors du Portage de code impliquant des opérations de pixels, gardez les points suivants à l’esprit :

-   Les opérations de pixels logiques ne sont pas appliquées aux tampons de couleurs RVBA. Pour plus d’informations, consultez [**glLogicOp**](gllogicop.md).
-   En général, IRIS GL utilise le format ABGR pour les pixels, tandis que OpenGL utilise RVBA. Vous pouvez modifier le format avec [**glPixelStore**](glpixelstore-functions.md).
-   Lors du Portage des fonctions **lrectwrite** , veillez à noter l’endroit où **lrectwrite** écrit (par exemple, il peut écrire dans le tampon de profondeur).

OpenGL offre une plus grande flexibilité en matière d’opérations de pixels. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour les opérations de pixels et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                                   | Fonction OpenGL                                                                           | Signification                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**, **rectread**,**readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Lit un bloc de pixels à partir du trame.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Écrit un bloc de pixels dans le trame.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Copie les pixels dans le trame.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Spécifie les facteurs de zoom de pixel pour **glDrawPixels** et **glCopyPixels**. |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Spécifie la position raster pour les opérations de pixel.                         |
| **readsource**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Sélectionne une source de mémoire tampon de couleur pour les pixels.                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Définit les modes de stockage en pixels. Définissez les modes de transfert de pixels.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Spécifie une opération logique pour les écritures de pixels.                         |
|                                                    | [**glEnable**](glenable.md) (GL \_ Logic \_ op)                                            | Active les opérations de logiques de pixels.                                        |



 

Pour obtenir la liste complète des opérations logiques possibles, consultez [**glLogicOp**](gllogicop.md).

Cet exemple de code IRIS GL illustre une écriture de pixels classique :

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

Le code précédent ressemble à celui-ci lorsqu’il est traduit en OpenGL :

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





