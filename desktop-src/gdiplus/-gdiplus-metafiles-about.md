---
description: Windows GDI+ fournit la classe Metafile pour vous permettre d’enregistrer et d’afficher des métafichiers.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Fichiers de fichier (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318338"
---
# <a name="metafiles-gdi"></a>Fichiers de fichier (GDI+)

Windows GDI+ fournit la classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) pour vous permettre d’enregistrer et d’afficher des métafichiers. Un métafichier, également appelé image vectorielle, est une image qui est stockée sous la forme d’une séquence de commandes et de paramètres de dessin. Les commandes et les paramètres enregistrés dans un objet **Metafile** peuvent être stockés dans la mémoire ou enregistrés dans un fichier ou un flux.

GDI+ peut afficher les sous-fichiers qui ont été stockés dans les formats suivants :

-   Windows Metafile Format (WMF)
-   métafichier amélioré (EMF)
-   EMF +

GDI+ peut enregistrer les fichiers de métafichier dans les formats EMF et EMF +, mais pas au format WMF.

EMF + est une extension du EMF qui permet le stockage des enregistrements GDI+. Il existe deux variantes du format EMF + : EMF + uniquement et EMF + double. Les fichiers EMF + only contiennent uniquement des enregistrements GDI+. Ces sous-fichiers peuvent être affichés par GDI+ mais pas par Windows Graphics Device Interface (GDI). Les métafichiers EMF + double contiennent des enregistrements GDI+ et GDI. Chaque enregistrement GDI+ dans un métafichier EMF + double est associé à un autre enregistrement GDI. Ces sous-fichiers peuvent être affichés par GDI+ ou GDI.

L’exemple suivant enregistre un paramètre et une commande de dessin dans un fichier disque. Notez que l’exemple crée un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et que le constructeur de l’objet **Graphics** reçoit l’adresse d’un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) comme argument.


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



Comme le montre l’exemple précédent, la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est la clé d’enregistrement des instructions et des paramètres dans un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Tout appel passé à une méthode d’un objet **Graphics** peut être enregistré dans un objet **Metafile** . De même, vous pouvez définir n’importe quelle propriété d’un objet **Graphics** et enregistrer ce paramètre dans un objet **Metafile** . L’enregistrement se termine lorsque l’objet **Graphics** est supprimé ou est hors de portée.

L’exemple suivant affiche le métafichier créé dans l’exemple précédent. Le métafichier est affiché avec son coin supérieur gauche à l’adresse (100, 100).


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



L’exemple suivant enregistre plusieurs paramètres de propriété (région de découpage, transformation universelle et mode de lissage) dans un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Ensuite, le code enregistre plusieurs instructions de dessin. Les instructions et les paramètres sont enregistrés dans un fichier sur disque.


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



L’exemple suivant affiche l’image de métafichier créée dans l’exemple précédent.


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



L’illustration suivante montre la sortie du code précédent. Notez l’anticrénelage, la zone de découpage elliptique et la rotation à 30 degrés.

![capture d’écran d’une fenêtre qui contient une Ellipse remplie de lignes d’origine à un point en dehors de l’ellipse](images/aboutgdip05-art00.png)

 

 



