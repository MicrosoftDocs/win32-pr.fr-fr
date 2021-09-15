---
title: Impression d’une image OpenGL
description: Vous pouvez imprimer les images OpenGL rendues dans les sous-fichiers améliorés.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL sur Windows, impression
- impression d’images OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311686"
---
# <a name="printing-an-opengl-image"></a>Impression d’une image OpenGL

Vous pouvez imprimer les images OpenGL rendues dans les sous-fichiers améliorés. Lorsque vous effectuez un rendu sur un appareil d’imprimante (HDC), celui-ci doit être sauvegardé par un spouleur de métafichiers. OpenGL utilise de la mémoire pour la profondeur, la couleur et d’autres mémoires tampons pour stocker la sortie graphique sur une imprimante. Étant donné que la résolution d’imprimante par défaut nécessite une quantité importante de mémoire pour stocker la sortie graphique, l’impression d’une image OpenGL peut nécessiter plus de mémoire que ce qui est disponible dans le système. Pour surmonter cette limitation, l’implémentation actuelle d’OpenGL imprime les graphiques OpenGL en bandes. Toutefois, cela augmente le temps nécessaire à l’impression des images OpenGL.

Avant d’imprimer une image OpenGL, vous devez appeler la fonction [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) pour terminer l’initialisation d’un contexte de périphérique d’impression (DC). Après avoir appelé **StartDoc**, vous pouvez créer des contextes de rendu (HGLRC) à rendre sur le périphérique d’impression. Si vous créez des contextes de rendu avant d’appeler **StartDoc**, il n’existe aucun moyen de déterminer si un métafichier est mis en file d’attente.

L’exemple de code suivant montre comment imprimer une image OpenGL :

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

Pour plus d’informations sur l’utilisation des métafichiers, consultez [opérations de métafichier améliorées](/windows/desktop/gdi/enhanced-metafile-operations).

 

 