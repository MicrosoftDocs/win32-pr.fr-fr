---
description: Windows prend en charge les formats pour compresser les bitmaps qui définissent leurs couleurs avec 8 ou 4 bits par pixel. La compression réduit le stockage de disque et de mémoire requis pour la bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compression de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462b41bffe207aecc82deece7e2090cfe6389635
ms.sourcegitcommit: 8eb9ae480cf2cb3524d83a1e7adcdaa875d625e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2021
ms.locfileid: "123096445"
---
# <a name="bitmap-compression"></a>Compression de bitmap

Windows prend en charge les formats pour compresser les bitmaps qui définissent leurs couleurs avec 8 ou 4 bits par pixel. La compression réduit le stockage de disque et de mémoire requis pour la bitmap.

Quand le membre de **compression** de la structure d’en-tête d’informations bitmap est bi \_ RLE8, un format de codage de longueur d’exécution (RLE) est utilisé pour compresser une image bitmap de 8 bits. Ce format peut être compressé en mode encodé ou absolu. Les deux modes peuvent se trouver n’importe où dans la même bitmap :

-   Le *mode encodé* se compose de deux octets : le premier octet spécifie le nombre de pixels consécutifs à dessiner à l’aide de l’index de couleur contenu dans le deuxième octet. En outre, le premier octet de la paire peut être défini à zéro pour indiquer un caractère d’échappement qui désigne la fin d’une ligne, la fin d’une bitmap ou un Delta, en fonction de la valeur du deuxième octet. L’interprétation de l’échappement dépend de la valeur du deuxième octet de la paire, qui peut être l’une des valeurs suivantes.



| Valeur | Signification                                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fin de ligne.                                                                                                                                           |
| 1     | Fin de bitmap.                                                                                                                                         |
| 2     | Set. Les 2 octets qui suivent l’échappement contiennent des valeurs non signées indiquant le décalage vers la droite et le haut du pixel suivant à partir de la position actuelle. |



 

-   En *mode absolu*, le premier octet est égal à zéro et le deuxième octet est une valeur comprise entre 03H et FFH. Le deuxième octet représente le nombre d’octets qui suivent, chacun contenant l’index de couleur d’un pixel unique. Lorsque le deuxième octet est inférieur ou égal à deux, l’échappement a la même signification que le mode encodé. En mode absolu, chaque exécution doit être complétée par des zéros pour se terminer sur une limite de mot de 16 bits.

L’exemple suivant montre les valeurs hexadécimales d’une bitmap 8 bits compressée :


```C++
[03 04] [05 06] [00 03 45 56 67 00] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



La bitmap se développe comme suit (les valeurs à deux chiffres représentent un index de couleur pour un pixel unique) :


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 up 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



Quand le membre de **compression** est bi \_ RLE4, l’image bitmap est compressée à l’aide d’un format d’encodage de longueur d’exécution pour une image bitmap de 4 bits, qui utilise également les modes codé et absolu :

-   En mode encodé, le premier octet de la paire contient le nombre de pixels à dessiner à l’aide des index de couleurs du deuxième octet. Le deuxième octet contient deux index de couleur, l’un dans ses 4 bits de poids fort et l’autre dans ses 4 bits de poids faible. Le premier des pixels est dessiné à l’aide de la couleur spécifiée par les bits de poids fort, le deuxième est dessiné à l’aide de la couleur dans les bits de poids faible, le troisième est dessiné à l’aide de la couleur des 4 bits d’ordre haut, et ainsi de suite, jusqu’à ce que tous les pixels spécifiés par le premier octet aient été dessinés.
-   En mode absolu, le premier octet est égal à zéro. Le deuxième octet contient le nombre d’index de couleur qui suivent. Les octets suivants contiennent des index de couleurs dans leurs 4 bits de poids fort et de poids faible, un index de couleur pour chaque pixel. En mode absolu, chaque exécution doit être alignée sur une limite de mot. La fin de ligne, la fin de bitmap et les séquences d’échappement Delta décrites pour BI \_ RLE8 s’appliquent également à la \_ compression RLE4 bi.

L’exemple suivant montre les valeurs hexadécimales d’une bitmap de 16 bits compressée :


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



La bitmap se développe comme suit (les valeurs à un seul chiffre représentent un index de couleur pour un pixel unique) :


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 up 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



