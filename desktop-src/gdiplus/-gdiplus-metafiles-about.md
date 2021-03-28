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
# <a name="metafiles-gdi"></a><span data-ttu-id="71741-103">Fichiers de fichier (GDI+)</span><span class="sxs-lookup"><span data-stu-id="71741-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="71741-104">Windows GDI+ fournit la classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) pour vous permettre d’enregistrer et d’afficher des métafichiers.</span><span class="sxs-lookup"><span data-stu-id="71741-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="71741-105">Un métafichier, également appelé image vectorielle, est une image qui est stockée sous la forme d’une séquence de commandes et de paramètres de dessin.</span><span class="sxs-lookup"><span data-stu-id="71741-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="71741-106">Les commandes et les paramètres enregistrés dans un objet **Metafile** peuvent être stockés dans la mémoire ou enregistrés dans un fichier ou un flux.</span><span class="sxs-lookup"><span data-stu-id="71741-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="71741-107">GDI+ peut afficher les sous-fichiers qui ont été stockés dans les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="71741-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="71741-108">Windows Metafile Format (WMF)</span><span class="sxs-lookup"><span data-stu-id="71741-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="71741-109">métafichier amélioré (EMF)</span><span class="sxs-lookup"><span data-stu-id="71741-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="71741-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="71741-110">EMF+</span></span>

<span data-ttu-id="71741-111">GDI+ peut enregistrer les fichiers de métafichier dans les formats EMF et EMF +, mais pas au format WMF.</span><span class="sxs-lookup"><span data-stu-id="71741-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="71741-112">EMF + est une extension du EMF qui permet le stockage des enregistrements GDI+.</span><span class="sxs-lookup"><span data-stu-id="71741-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="71741-113">Il existe deux variantes du format EMF + : EMF + uniquement et EMF + double.</span><span class="sxs-lookup"><span data-stu-id="71741-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="71741-114">Les fichiers EMF + only contiennent uniquement des enregistrements GDI+.</span><span class="sxs-lookup"><span data-stu-id="71741-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="71741-115">Ces sous-fichiers peuvent être affichés par GDI+ mais pas par Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="71741-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="71741-116">Les métafichiers EMF + double contiennent des enregistrements GDI+ et GDI.</span><span class="sxs-lookup"><span data-stu-id="71741-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="71741-117">Chaque enregistrement GDI+ dans un métafichier EMF + double est associé à un autre enregistrement GDI.</span><span class="sxs-lookup"><span data-stu-id="71741-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="71741-118">Ces sous-fichiers peuvent être affichés par GDI+ ou GDI.</span><span class="sxs-lookup"><span data-stu-id="71741-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="71741-119">L’exemple suivant enregistre un paramètre et une commande de dessin dans un fichier disque.</span><span class="sxs-lookup"><span data-stu-id="71741-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="71741-120">Notez que l’exemple crée un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et que le constructeur de l’objet **Graphics** reçoit l’adresse d’un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) comme argument.</span><span class="sxs-lookup"><span data-stu-id="71741-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


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



<span data-ttu-id="71741-121">Comme le montre l’exemple précédent, la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est la clé d’enregistrement des instructions et des paramètres dans un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="71741-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="71741-122">Tout appel passé à une méthode d’un objet **Graphics** peut être enregistré dans un objet **Metafile** .</span><span class="sxs-lookup"><span data-stu-id="71741-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="71741-123">De même, vous pouvez définir n’importe quelle propriété d’un objet **Graphics** et enregistrer ce paramètre dans un objet **Metafile** .</span><span class="sxs-lookup"><span data-stu-id="71741-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="71741-124">L’enregistrement se termine lorsque l’objet **Graphics** est supprimé ou est hors de portée.</span><span class="sxs-lookup"><span data-stu-id="71741-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="71741-125">L’exemple suivant affiche le métafichier créé dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="71741-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="71741-126">Le métafichier est affiché avec son coin supérieur gauche à l’adresse (100, 100).</span><span class="sxs-lookup"><span data-stu-id="71741-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="71741-127">L’exemple suivant enregistre plusieurs paramètres de propriété (région de découpage, transformation universelle et mode de lissage) dans un objet [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="71741-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="71741-128">Ensuite, le code enregistre plusieurs instructions de dessin.</span><span class="sxs-lookup"><span data-stu-id="71741-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="71741-129">Les instructions et les paramètres sont enregistrés dans un fichier sur disque.</span><span class="sxs-lookup"><span data-stu-id="71741-129">The instructions and settings are saved in a disk file.</span></span>


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



<span data-ttu-id="71741-130">L’exemple suivant affiche l’image de métafichier créée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="71741-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="71741-131">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="71741-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="71741-132">Notez l’anticrénelage, la zone de découpage elliptique et la rotation à 30 degrés.</span><span class="sxs-lookup"><span data-stu-id="71741-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![capture d’écran d’une fenêtre qui contient une Ellipse remplie de lignes d’origine à un point en dehors de l’ellipse](images/aboutgdip05-art00.png)

 

 



