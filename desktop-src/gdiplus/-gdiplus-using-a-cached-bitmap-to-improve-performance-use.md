---
description: Les objets image et Bitmap stockent les images dans un format indépendant du périphérique.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Utilisation d’une image bitmap mise en cache pour améliorer les performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ffee17a2c8d564a38235cc83d204eacc9b4edf2e8070cb5971d55f1f991169f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036327"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Utilisation d’une image bitmap mise en cache pour améliorer les performances

Les objets [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) stockent les images dans un format indépendant du périphérique. Un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) stocke une image au format du périphérique d’affichage actuel. Le rendu d’une image stockée dans un objet **CachedBitmap** est rapide, car aucun temps de traitement n’est consacré à la conversion de l’image au format requis par le périphérique d’affichage.

L’exemple suivant crée un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) et un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) à partir du fichier Texture.jpg. Les **bitmaps** et les **CachedBitmap** sont tous dessinés 30 000 fois. Si vous exécutez le code, vous verrez que les images **CachedBitmap** sont dessinées beaucoup plus rapidement que les images **bitmap** .


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
> Un objet [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) correspond au format du périphérique d’affichage au moment de la construction de l’objet **CachedBitmap** . Si l’utilisateur de votre programme modifie les paramètres d’affichage, votre code doit construire un nouvel objet **CachedBitmap** . La méthode **DrawImage** échoue si vous la transmettez à un objet **CachedBitmap** qui a été créé avant une modification dans le format d’affichage.

 

 

 



