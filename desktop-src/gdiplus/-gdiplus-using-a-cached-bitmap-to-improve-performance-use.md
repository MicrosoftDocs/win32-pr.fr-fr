---
description: Les objets image et Bitmap stockent les images dans un format indépendant du périphérique.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Utilisation d’une image bitmap mise en cache pour améliorer les performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991309"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a><span data-ttu-id="61817-103">Utilisation d’une image bitmap mise en cache pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="61817-103">Using a Cached Bitmap to Improve Performance</span></span>

<span data-ttu-id="61817-104">Les objets [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) stockent les images dans un format indépendant du périphérique.</span><span class="sxs-lookup"><span data-stu-id="61817-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) objects store images in a device-independent format.</span></span> <span data-ttu-id="61817-105">Un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) stocke une image au format du périphérique d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="61817-105">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object stores an image in the format of the current display device.</span></span> <span data-ttu-id="61817-106">Le rendu d’une image stockée dans un objet **CachedBitmap** est rapide, car aucun temps de traitement n’est consacré à la conversion de l’image au format requis par le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="61817-106">Rendering an image stored in a **CachedBitmap** object is fast because no processing time is spent converting the image to the format required by the display device.</span></span>

<span data-ttu-id="61817-107">L’exemple suivant crée un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) et un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) à partir du fichier Texture.jpg.</span><span class="sxs-lookup"><span data-stu-id="61817-107">The following example creates a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object and a [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object from the file Texture.jpg.</span></span> <span data-ttu-id="61817-108">Les **bitmaps** et les **CachedBitmap** sont tous dessinés 30 000 fois.</span><span class="sxs-lookup"><span data-stu-id="61817-108">The **Bitmap** and the **CachedBitmap** are each drawn 30,000 times.</span></span> <span data-ttu-id="61817-109">Si vous exécutez le code, vous verrez que les images **CachedBitmap** sont dessinées beaucoup plus rapidement que les images **bitmap** .</span><span class="sxs-lookup"><span data-stu-id="61817-109">If you run the code, you will see that the **CachedBitmap** images are drawn substantially faster than the **Bitmap** images.</span></span>


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> <span data-ttu-id="61817-110">Un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) correspond au format du périphérique d’affichage au moment de la construction de l’objet **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="61817-110">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object matches the format of the display device at the time the **CachedBitmap** object was constructed.</span></span> <span data-ttu-id="61817-111">Si l’utilisateur de votre programme modifie les paramètres d’affichage, votre code doit construire un nouvel objet **CachedBitmap** .</span><span class="sxs-lookup"><span data-stu-id="61817-111">If the user of your program changes the display settings, your code should construct a new **CachedBitmap** object.</span></span> <span data-ttu-id="61817-112">La méthode **DrawImage** échoue si vous la transmettez à un objet **CachedBitmap** qui a été créé avant une modification dans le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="61817-112">The **DrawImage** method will fail if you pass it a **CachedBitmap** object that was created prior to a change in the display format.</span></span>

 

 

 



