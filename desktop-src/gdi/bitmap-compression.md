---
description: Windows prend en charge les formats pour la compression des bitmaps qui définissent leurs couleurs avec 8 ou 4 bits par pixel. La compression réduit le stockage de disque et de mémoire requis pour la bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compression de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114738"
---
# <a name="bitmap-compression"></a><span data-ttu-id="07131-104">Compression de bitmap</span><span class="sxs-lookup"><span data-stu-id="07131-104">Bitmap Compression</span></span>

<span data-ttu-id="07131-105">Windows prend en charge les formats pour la compression des bitmaps qui définissent leurs couleurs avec 8 ou 4 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="07131-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="07131-106">La compression réduit le stockage de disque et de mémoire requis pour la bitmap.</span><span class="sxs-lookup"><span data-stu-id="07131-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="07131-107">Quand le membre de **compression** de la structure d’en-tête d’informations bitmap est bi \_ RLE8, un format de codage de longueur d’exécution (RLE) est utilisé pour compresser une image bitmap de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="07131-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="07131-108">Ce format peut être compressé en mode encodé ou absolu.</span><span class="sxs-lookup"><span data-stu-id="07131-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="07131-109">Les deux modes peuvent se trouver n’importe où dans la même bitmap :</span><span class="sxs-lookup"><span data-stu-id="07131-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="07131-110">Le *mode encodé* se compose de deux octets : le premier octet spécifie le nombre de pixels consécutifs à dessiner à l’aide de l’index de couleur contenu dans le deuxième octet.</span><span class="sxs-lookup"><span data-stu-id="07131-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="07131-111">En outre, le premier octet de la paire peut être défini à zéro pour indiquer un caractère d’échappement qui désigne la fin d’une ligne, la fin d’une bitmap ou un Delta, en fonction de la valeur du deuxième octet.</span><span class="sxs-lookup"><span data-stu-id="07131-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="07131-112">L’interprétation de l’échappement dépend de la valeur du deuxième octet de la paire, qui peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="07131-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="07131-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="07131-113">Value</span></span> | <span data-ttu-id="07131-114">Signification</span><span class="sxs-lookup"><span data-stu-id="07131-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07131-115">0</span><span class="sxs-lookup"><span data-stu-id="07131-115">0</span></span>     | <span data-ttu-id="07131-116">Fin de ligne.</span><span class="sxs-lookup"><span data-stu-id="07131-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="07131-117">1</span><span class="sxs-lookup"><span data-stu-id="07131-117">1</span></span>     | <span data-ttu-id="07131-118">Fin de bitmap.</span><span class="sxs-lookup"><span data-stu-id="07131-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="07131-119">2</span><span class="sxs-lookup"><span data-stu-id="07131-119">2</span></span>     | <span data-ttu-id="07131-120">Set.</span><span class="sxs-lookup"><span data-stu-id="07131-120">Delta.</span></span> <span data-ttu-id="07131-121">Les 2 octets qui suivent l’échappement contiennent des valeurs non signées indiquant les décalages horizontal et vertical du pixel suivant à partir de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="07131-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="07131-122">En *mode absolu*, le premier octet est égal à zéro et le deuxième octet est une valeur comprise entre 03H et FFH.</span><span class="sxs-lookup"><span data-stu-id="07131-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="07131-123">Le deuxième octet représente le nombre d’octets qui suivent, chacun contenant l’index de couleur d’un pixel unique.</span><span class="sxs-lookup"><span data-stu-id="07131-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="07131-124">Lorsque le deuxième octet est inférieur ou égal à deux, l’échappement a la même signification que le mode encodé.</span><span class="sxs-lookup"><span data-stu-id="07131-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="07131-125">En mode absolu, chaque exécution doit être alignée sur une limite de mot.</span><span class="sxs-lookup"><span data-stu-id="07131-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="07131-126">L’exemple suivant montre les valeurs hexadécimales d’une bitmap 8 bits compressée :</span><span class="sxs-lookup"><span data-stu-id="07131-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="07131-127">La bitmap se développe comme suit (les valeurs à deux chiffres représentent un index de couleur pour un pixel unique) :</span><span class="sxs-lookup"><span data-stu-id="07131-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="07131-128">Quand le membre de **compression** est bi \_ RLE4, l’image bitmap est compressée à l’aide d’un format d’encodage de longueur d’exécution pour une image bitmap de 4 bits, qui utilise également les modes codé et absolu :</span><span class="sxs-lookup"><span data-stu-id="07131-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="07131-129">En mode encodé, le premier octet de la paire contient le nombre de pixels à dessiner à l’aide des index de couleurs du deuxième octet.</span><span class="sxs-lookup"><span data-stu-id="07131-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="07131-130">Le deuxième octet contient deux index de couleur, l’un dans ses 4 bits de poids fort et l’autre dans ses 4 bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="07131-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="07131-131">Le premier des pixels est dessiné à l’aide de la couleur spécifiée par les bits de poids fort, le deuxième est dessiné à l’aide de la couleur dans les bits de poids faible, le troisième est dessiné à l’aide de la couleur des 4 bits d’ordre haut, et ainsi de suite, jusqu’à ce que tous les pixels spécifiés par le premier octet aient été dessinés.</span><span class="sxs-lookup"><span data-stu-id="07131-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="07131-132">En mode absolu, le premier octet est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="07131-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="07131-133">Le deuxième octet contient le nombre d’index de couleur qui suivent.</span><span class="sxs-lookup"><span data-stu-id="07131-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="07131-134">Les octets suivants contiennent des index de couleurs dans leurs 4 bits de poids fort et de poids faible, un index de couleur pour chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="07131-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="07131-135">En mode absolu, chaque exécution doit être alignée sur une limite de mot.</span><span class="sxs-lookup"><span data-stu-id="07131-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="07131-136">La fin de ligne, la fin de bitmap et les séquences d’échappement Delta décrites pour BI \_ RLE8 s’appliquent également à la \_ compression RLE4 bi.</span><span class="sxs-lookup"><span data-stu-id="07131-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="07131-137">L’exemple suivant montre les valeurs hexadécimales d’une bitmap de 16 bits compressée :</span><span class="sxs-lookup"><span data-stu-id="07131-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="07131-138">La bitmap se développe comme suit (les valeurs à un seul chiffre représentent un index de couleur pour un pixel unique) :</span><span class="sxs-lookup"><span data-stu-id="07131-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



