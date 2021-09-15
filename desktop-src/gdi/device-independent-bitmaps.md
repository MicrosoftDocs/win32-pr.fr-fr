---
description: Une bitmap indépendante du périphérique (DIB, Device-Independent Bitmap) contient une table des couleurs.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Device-Independent des bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa35201a9a27c2d16a5a18b0125d25a3938890c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520068"
---
# <a name="device-independent-bitmaps"></a>Device-Independent des bitmaps

Une bitmap indépendante du périphérique (DIB, Device-Independent Bitmap) contient une *table des couleurs*. Une table des couleurs décrit comment les valeurs de pixel correspondent aux valeurs de couleur *RVB* , qui décrivent les couleurs produites en émettant de la lumière. Par conséquent, un DIB peut obtenir le schéma de couleurs approprié sur n’importe quel appareil. Un DIB contient les informations de couleur et de dimension suivantes :

-   Format de couleur de l’appareil sur lequel l’image rectangulaire a été créée.
-   Résolution de l’appareil sur lequel l’image rectangulaire a été créée.
-   Palette de l’appareil sur lequel l’image a été créée.
-   Tableau de bits qui mappe des triplets rouge, vert et bleu ( [**RVB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ) aux pixels de l’image rectangulaire.
-   Identificateur de compression de données qui indique le schéma de compression de données (le cas échéant) utilisé pour réduire la taille du tableau de bits.

Les informations de couleur et de dimension sont stockées dans une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , qui se compose d’une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) suivie de deux structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) ou plus. La structure **BITMAPINFOHEADER** spécifie les dimensions du rectangle de pixels, décrit la technologie de couleur de l’appareil et identifie les schémas de compression utilisés pour réduire la taille de l’image bitmap. Les structures **RGBQUAD** identifient les couleurs qui apparaissent dans le rectangle de pixels.

Il existe deux types de DIB :

-   DIB ascendant, dans lequel l’origine se trouve dans le coin inférieur gauche.
-   DIB descendant, dans lequel l’origine se trouve dans l’angle supérieur gauche.

Si la hauteur d’un DIB, comme indiqué par le membre **Height** de la structure d’en-tête d’informations bitmap, est une valeur positive, il s’agit d’un DIB ascendant ; Si la hauteur est une valeur négative, il s’agit d’un DIB descendant. Les DIB descendants ne peuvent pas être compressés.

Le format de couleur est spécifié en termes de nombre de plans de couleur et de bits de couleur. Le nombre de plans de couleur est toujours 1 ; le nombre de bits de couleur est 1 pour les images bitmap monochrome, 4 pour les bitmaps VGA et 8, 16, 24 ou 32 pour les bitmaps sur d’autres appareils couleur. Une application récupère le nombre de bits de couleur utilisés par un affichage (ou une imprimante) particulier en appelant la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant BITSPIXEL comme deuxième argument.

La résolution d’un périphérique d’affichage est spécifiée en pixels par mètre. Une application peut récupérer la résolution horizontale pour un affichage vidéo, ou imprimante, en suivant ce processus en trois étapes.

1.  Appelez la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant HORZRES comme deuxième argument.
2.  Appelez [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) une deuxième fois, en spécifiant HORZSIZE comme deuxième argument.
3.  Divise la première valeur de retour par la deuxième valeur de retour.

L’application peut récupérer la résolution verticale en utilisant le même processus en trois étapes avec des paramètres différents : VERTRES à la place de HORZRES et VERTSIZE à la place de HORZSIZE.

La palette est représentée par un tableau de structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) qui spécifient les composants d’intensité rouge, vert et bleu pour chaque couleur dans la palette de couleurs d’un périphérique d’affichage. Chaque index de couleurs du tableau de palette est mappé à un pixel spécifique dans la zone rectangulaire associée à l’image bitmap. La taille de ce tableau, en bits, est équivalente à la largeur du rectangle, en pixels, multipliée par la hauteur du rectangle, en pixels, multipliée par le nombre de bits de couleur de l’appareil. Une application peut récupérer la taille de la palette de l’appareil en appelant la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant NUMCOLORS comme deuxième argument.

Windows prend en charge la compression du tableau de palettes pour les dib 8-bpp et 4-bpp de bas en haut. Ces tableaux peuvent être compressés à l’aide du schéma d’encodage de longueur d’exécution (RLE). Le schéma RLE utilise des valeurs de 2 octets, le premier octet spécifiant le nombre de pixels consécutifs qui utilisent un index de couleurs et le deuxième octet spécifiant l’index. Pour plus d’informations sur la compression des bitmaps, consultez la description des structures [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)et [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .

Une application peut créer un DIB à partir d’un DDB en initialisant les structures requises et en appelant la fonction [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) . Pour déterminer si un appareil prend en charge cette fonction, appelez la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant RC \_ di \_ bitmap comme indicateur RasterCaps.

Une application qui doit copier une image bitmap peut utiliser [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) pour copier tous les pixels d’une image bitmap source vers une bitmap de destination, à l’exception de ces pixels qui correspondent à la couleur transparente.

Une application peut utiliser un DIB pour définir des pixels sur le périphérique d’affichage en appelant la fonction [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) . Pour déterminer si un appareil prend en charge la fonction **SetDIBitsToDevice** , appelez la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , en spécifiant RC \_ DIBTODEV comme indicateur RasterCaps. Spécifiez RC \_ STRETCHDIB comme indicateur RasterCaps pour déterminer si l’appareil prend en charge **StretchDIBits**.

Une application qui doit simplement afficher un DIB préexistant peut utiliser la fonction [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) . Par exemple, une application de feuille de calcul peut ouvrir des graphiques existants et les afficher dans une fenêtre à l’aide de la fonction **SetDIBitsToDevice** . Toutefois, pour redessiner à plusieurs reprises une bitmap dans une fenêtre, l’application doit utiliser la fonction [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) . Par exemple, une application multimédia qui combine des graphiques animés avec du son peut tirer parti de l’appel de la fonction **BitBlt** , car elle s’exécute plus rapidement que **SetDIBitsToDevice**.

 

 
