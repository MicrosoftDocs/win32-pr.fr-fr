---
description: La classe Metafile, qui hérite de la classe image, vous permet d’enregistrer une séquence de commandes de dessin.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Enregistrement des fichiers de sous-fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972151"
---
# <a name="recording-metafiles"></a><span data-ttu-id="03e37-103">Enregistrement des fichiers de sous-fichier</span><span class="sxs-lookup"><span data-stu-id="03e37-103">Recording Metafiles</span></span>

<span data-ttu-id="03e37-104">La classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , qui hérite de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , vous permet d’enregistrer une séquence de commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="03e37-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="03e37-105">Les commandes enregistrées peuvent être stockées dans la mémoire, enregistrées dans un fichier ou enregistrées dans un flux.</span><span class="sxs-lookup"><span data-stu-id="03e37-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="03e37-106">Les sous-fichiers peuvent contenir des graphiques vectoriels, des images raster et du texte.</span><span class="sxs-lookup"><span data-stu-id="03e37-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="03e37-107">L’exemple suivant crée un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="03e37-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="03e37-108">Le code utilise l’objet **Metafile** pour enregistrer une séquence de commandes Graphics, puis enregistre les commandes enregistrées dans un fichier nommé SampleMetafile. EMF.</span><span class="sxs-lookup"><span data-stu-id="03e37-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="03e37-109">Notez que le constructeur **Metafile** reçoit un handle de contexte de périphérique et que le constructeur [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) reçoit l’adresse de l’objet **Metafile** .</span><span class="sxs-lookup"><span data-stu-id="03e37-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="03e37-110">L’enregistrement s’arrête (et les commandes enregistrées sont enregistrées dans le fichier) lorsque l’objet **Graphics** est hors de portée.</span><span class="sxs-lookup"><span data-stu-id="03e37-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="03e37-111">Les deux dernières lignes de code affichent le métafichier en créant un nouvel objet **Graphics** et en passant l’adresse de l’objet **Metafile** à la méthode **DrawImage** de cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="03e37-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="03e37-112">Notez que le code utilise le même objet de **métafichier** pour enregistrer et afficher (Lire) le métafichier.</span><span class="sxs-lookup"><span data-stu-id="03e37-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


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
> <span data-ttu-id="03e37-113">Pour enregistrer un métafichier, vous devez construire un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="03e37-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="03e37-114">L’enregistrement du métafichier se termine lorsque cet objet **Graphics** est supprimé ou hors de portée.</span><span class="sxs-lookup"><span data-stu-id="03e37-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="03e37-115">Un métafichier contient son propre État Graphics, qui est défini par l’objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) utilisé pour enregistrer le métafichier.</span><span class="sxs-lookup"><span data-stu-id="03e37-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="03e37-116">Toutes les propriétés de l’objet **Graphics** (zone de découpage, transformation universelle, mode lissage et like) que vous définissez lors de l’enregistrement du métafichier sont stockées dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="03e37-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="03e37-117">Lorsque vous affichez le métafichier, le dessin est effectué en fonction de ces propriétés stockées.</span><span class="sxs-lookup"><span data-stu-id="03e37-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="03e37-118">Dans l’exemple suivant, supposons que le mode de lissage a été défini sur SmoothingModeNormal lors de l’enregistrement du métafichier.</span><span class="sxs-lookup"><span data-stu-id="03e37-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="03e37-119">Même si le mode de lissage de l’objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) utilisé pour la lecture est défini sur SmoothingModeHighQuality, le métafichier est lu en fonction du paramètre SmoothingModeNormal.</span><span class="sxs-lookup"><span data-stu-id="03e37-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="03e37-120">C’est le mode de lissage défini lors de l’enregistrement qui est important, pas le mode de lissage défini avant la lecture.</span><span class="sxs-lookup"><span data-stu-id="03e37-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



