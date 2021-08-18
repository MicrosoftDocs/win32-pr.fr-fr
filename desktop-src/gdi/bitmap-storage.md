---
description: Les bitmaps doivent être enregistrées dans un fichier qui utilise le format de fichier bitmap établi et attribuer un nom avec l’extension de .bmp à trois caractères.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Stockage Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83688f240899ded49227264b716d8c5d1fb609aa747fc358184a78ad18c8d17f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038207"
---
# <a name="bitmap-storage"></a>Stockage Bitmap

Les bitmaps doivent être enregistrées dans un fichier qui utilise le format de fichier bitmap établi et attribuer un nom avec l’extension de .bmp à trois caractères. Le format de fichier bitmap établi se compose d’une structure [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) suivie d’une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . Un tableau de structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (également appelé table de couleurs) suit la structure d’en-tête d’informations bitmap. La table de couleurs est suivie d’un deuxième tableau d’index dans la table des couleurs (les données de la bitmap réelle).

Le format de fichier bitmap est indiqué dans l’illustration suivante.

![diagramme du format de fichier bitmap, montrant le tableau bitmapfileheader, BITMAPINFOHEADER, rgbquad et le tableau d’index de couleurs](images/csbmp-02.png)

Les membres de la structure [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) identifient le fichier ; Spécifiez la taille du fichier, en octets ; et spécifiez le décalage du premier octet dans l’en-tête jusqu’au premier octet des données bitmap. Les membres de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) spécifient la largeur et la hauteur de la bitmap, en pixels ; le format de couleur (nombre de plans de couleur et de bits de couleur par pixel) du périphérique d’affichage sur lequel le bitmap a été créé ; Si les données bitmap ont été compressées avant le stockage et le type de compression utilisé ; nombre d’octets de données bitmap ; résolution du périphérique d’affichage sur lequel le bitmap a été créé ; et le nombre de couleurs représentées dans les données. Les structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) spécifient les valeurs d’intensité RVB pour chacune des couleurs de la palette de l’appareil.

Le tableau d’index de couleurs associe une couleur, sous la forme d’un index à une structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , à chaque pixel d’une bitmap. Ainsi, le nombre de bits dans le tableau d’index de couleurs est égal au nombre de pixels multiplié par le nombre de bits nécessaires pour indexer les structures **RGBQUAD** . Par exemple, une image bitmap de noir et blanc de 1 et 2 a un tableau d’index de couleurs de 8 \* 8 \* 1 = 64 bits, car un bit est nécessaire pour indexer deux couleurs. La Redbrick.bmp, mentionnée dans [à propos des bitmaps](about-bitmaps.md), est une bitmap 32x32 avec 16 couleurs ; son tableau d’index de couleurs est 32 \* 32 \* 4 = 4096 bits, car quatre couleurs d’index 16 bits.

Pour créer un tableau d’index de couleurs pour une image bitmap de haut en haut, commencez à la ligne supérieure de l’image bitmap. L’index du [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) pour la couleur du pixel le plus à gauche est les *n* premiers bits dans le tableau d’index de couleurs (où *n* est le nombre de bits nécessaires pour indiquer toutes les structures **RGBQUAD** ). La couleur du pixel suivant à droite est les *n* bits suivants dans le tableau, et ainsi de suite. Une fois que vous avez atteint le pixel le plus à droite dans la ligne, continuez avec le pixel le plus à gauche dans la ligne ci-dessous. Continuez jusqu’à ce que vous ayez terminé avec l’intégralité de l’image bitmap. S’il s’agit d’une image bitmap ascendante, commencez par la ligne du bas de l’image bitmap au lieu de la ligne supérieure, en allant de gauche à droite et passez à la ligne supérieure de l’image bitmap.

La sortie hexadécimale suivante affiche le contenu du fichier Redbrick.bmp.


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



Le tableau suivant montre les octets de données associés aux structures dans un fichier bitmap.



| Structure                                    | Octets correspondants |
|----------------------------------------------|---------------------|
| [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | 0x00 0x0D           |
| [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) | 0x0E 0x35           |
| Tableau [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)             | 0x36 0x75           |
| Tableau d’index de couleurs                            | 0x76 0x275          |



 

 

 
