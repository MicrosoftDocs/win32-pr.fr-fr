---
description: La classe Metafile, qui hérite de la classe image, vous permet d’enregistrer une séquence de commandes de dessin.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Enregistrement des fichiers de sous-fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047cdce842a9b44096ebd0f866e1b1551a5f951e138557062dff5e8f8d54f3ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014779"
---
# <a name="recording-metafiles"></a>Enregistrement des fichiers de sous-fichier

La classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , qui hérite de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , vous permet d’enregistrer une séquence de commandes de dessin. Les commandes enregistrées peuvent être stockées dans la mémoire, enregistrées dans un fichier ou enregistrées dans un flux. Les sous-fichiers peuvent contenir des graphiques vectoriels, des images raster et du texte.

L’exemple suivant crée un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Le code utilise l’objet **Metafile** pour enregistrer une séquence de commandes Graphics, puis enregistre les commandes enregistrées dans un fichier nommé SampleMetafile. EMF. Notez que le constructeur **Metafile** reçoit un handle de contexte de périphérique et que le constructeur [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) reçoit l’adresse de l’objet **Metafile** . L’enregistrement s’arrête (et les commandes enregistrées sont enregistrées dans le fichier) lorsque l’objet **Graphics** est hors de portée. Les deux dernières lignes de code affichent le métafichier en créant un nouvel objet **Graphics** et en passant l’adresse de l’objet **Metafile** à la méthode **DrawImage** de cet objet **Graphics** . Notez que le code utilise le même objet de **métafichier** pour enregistrer et afficher (Lire) le métafichier.


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> Pour enregistrer un métafichier, vous devez construire un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . L’enregistrement du métafichier se termine lorsque cet objet **Graphics** est supprimé ou hors de portée.

 

Un métafichier contient son propre État Graphics, qui est défini par l’objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) utilisé pour enregistrer le métafichier. Toutes les propriétés de l’objet **Graphics** (zone de découpage, transformation universelle, mode lissage et like) que vous définissez lors de l’enregistrement du métafichier sont stockées dans le métafichier. Lorsque vous affichez le métafichier, le dessin est effectué en fonction de ces propriétés stockées.

Dans l’exemple suivant, supposons que le mode de lissage a été défini sur SmoothingModeNormal lors de l’enregistrement du métafichier. Même si le mode de lissage de l’objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) utilisé pour la lecture est défini sur SmoothingModeHighQuality, le métafichier est lu en fonction du paramètre SmoothingModeNormal. C’est le mode de lissage défini lors de l’enregistrement qui est important, pas le mode de lissage défini avant la lecture.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



