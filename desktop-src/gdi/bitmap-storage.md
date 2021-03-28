---
description: Les bitmaps doivent être enregistrées dans un fichier qui utilise le format de fichier bitmap établi et attribuer un nom avec l’extension. bmp à trois caractères.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Stockage bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114730"
---
# <a name="bitmap-storage"></a><span data-ttu-id="58238-103">Stockage bitmap</span><span class="sxs-lookup"><span data-stu-id="58238-103">Bitmap Storage</span></span>

<span data-ttu-id="58238-104">Les bitmaps doivent être enregistrées dans un fichier qui utilise le format de fichier bitmap établi et attribuer un nom avec l’extension. bmp à trois caractères.</span><span class="sxs-lookup"><span data-stu-id="58238-104">Bitmaps should be saved in a file that uses the established bitmap file format and assigned a name with the three-character .bmp extension.</span></span> <span data-ttu-id="58238-105">Le format de fichier bitmap établi se compose d’une structure [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) suivie d’une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .</span><span class="sxs-lookup"><span data-stu-id="58238-105">The established bitmap file format consists of a [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure followed by a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure.</span></span> <span data-ttu-id="58238-106">Un tableau de structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (également appelé table de couleurs) suit la structure d’en-tête d’informations bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-106">An array of [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures (also called a color table) follows the bitmap information header structure.</span></span> <span data-ttu-id="58238-107">La table de couleurs est suivie d’un deuxième tableau d’index dans la table des couleurs (les données de la bitmap réelle).</span><span class="sxs-lookup"><span data-stu-id="58238-107">The color table is followed by a second array of indexes into the color table (the actual bitmap data).</span></span>

<span data-ttu-id="58238-108">Le format de fichier bitmap est indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="58238-108">The bitmap file format is shown in the following illustration.</span></span>

![diagramme du format de fichier bitmap, montrant le tableau bitmapfileheader, BITMAPINFOHEADER, rgbquad et le tableau d’index de couleurs](images/csbmp-02.png)

<span data-ttu-id="58238-110">Les membres de la structure [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) identifient le fichier ; Spécifiez la taille du fichier, en octets ; et spécifiez le décalage du premier octet dans l’en-tête jusqu’au premier octet des données bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-110">The members of the [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) structure identify the file; specify the size of the file, in bytes; and specify the offset from the first byte in the header to the first byte of bitmap data.</span></span> <span data-ttu-id="58238-111">Les membres de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) spécifient la largeur et la hauteur de la bitmap, en pixels ; le format de couleur (nombre de plans de couleur et de bits de couleur par pixel) du périphérique d’affichage sur lequel le bitmap a été créé ; Si les données bitmap ont été compressées avant le stockage et le type de compression utilisé ; nombre d’octets de données bitmap ; résolution du périphérique d’affichage sur lequel le bitmap a été créé ; et le nombre de couleurs représentées dans les données.</span><span class="sxs-lookup"><span data-stu-id="58238-111">The members of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header), or [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structure specify the width and height of the bitmap, in pixels; the color format (count of color planes and color bits-per-pixel) of the display device on which the bitmap was created; whether the bitmap data was compressed before storage and the type of compression used; the number of bytes of bitmap data; the resolution of the display device on which the bitmap was created; and the number of colors represented in the data.</span></span> <span data-ttu-id="58238-112">Les structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) spécifient les valeurs d’intensité RVB pour chacune des couleurs de la palette de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="58238-112">The [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures specify the RGB intensity values for each of the colors in the device's palette.</span></span>

<span data-ttu-id="58238-113">Le tableau d’index de couleurs associe une couleur, sous la forme d’un index à une structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , à chaque pixel d’une bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-113">The color-index array associates a color, in the form of an index to an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, with each pixel in a bitmap.</span></span> <span data-ttu-id="58238-114">Ainsi, le nombre de bits dans le tableau d’index de couleurs est égal au nombre de pixels multiplié par le nombre de bits nécessaires pour indexer les structures **RGBQUAD** .</span><span class="sxs-lookup"><span data-stu-id="58238-114">Thus, the number of bits in the color-index array equals the number of pixels times the number of bits needed to index the **RGBQUAD** structures.</span></span> <span data-ttu-id="58238-115">Par exemple, une image bitmap de noir et blanc de 1 et 2 a un tableau d’index de couleurs de 8 \* 8 \* 1 = 64 bits, car un bit est nécessaire pour indexer deux couleurs.</span><span class="sxs-lookup"><span data-stu-id="58238-115">For example, an 8x8 black-and-white bitmap has a color-index array of 8 \* 8 \* 1 = 64 bits, because one bit is needed to index two colors.</span></span> <span data-ttu-id="58238-116">La Redbrick.bmp, mentionnée dans [à propos des bitmaps](about-bitmaps.md), est une bitmap 32x32 avec 16 couleurs ; son tableau d’index de couleurs est 32 \* 32 \* 4 = 4096 bits, car quatre couleurs d’index 16 bits.</span><span class="sxs-lookup"><span data-stu-id="58238-116">The Redbrick.bmp, mentioned in [About Bitmaps](about-bitmaps.md), is a 32x32 bitmap with 16 colors; its color-index array is 32 \* 32 \* 4 = 4096 bits because four bits index 16 colors.</span></span>

<span data-ttu-id="58238-117">Pour créer un tableau d’index de couleurs pour une image bitmap de haut en haut, commencez à la ligne supérieure de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-117">To create a color-index array for a top-down bitmap, start at the top line in the bitmap.</span></span> <span data-ttu-id="58238-118">L’index du [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) pour la couleur du pixel le plus à gauche est les *n* premiers bits dans le tableau d’index de couleurs (où *n* est le nombre de bits nécessaires pour indiquer toutes les structures **RGBQUAD** ).</span><span class="sxs-lookup"><span data-stu-id="58238-118">The index of the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) for the color of the left-most pixel is the first *n* bits in the color-index array (where *n* is the number of bits needed to indicate all of the **RGBQUAD** structures).</span></span> <span data-ttu-id="58238-119">La couleur du pixel suivant à droite est les *n* bits suivants dans le tableau, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="58238-119">The color of the next pixel to the right is the next *n* bits in the array, and so forth.</span></span> <span data-ttu-id="58238-120">Une fois que vous avez atteint le pixel le plus à droite dans la ligne, continuez avec le pixel le plus à gauche dans la ligne ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="58238-120">After you reach the right-most pixel in the line, continue with the left-most pixel in the line below.</span></span> <span data-ttu-id="58238-121">Continuez jusqu’à ce que vous ayez terminé avec l’intégralité de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-121">Continue until you finish with the entire bitmap.</span></span> <span data-ttu-id="58238-122">S’il s’agit d’une image bitmap ascendante, commencez par la ligne du bas de l’image bitmap au lieu de la ligne supérieure, en allant de gauche à droite et passez à la ligne supérieure de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-122">If it is a bottom-up bitmap, start at the bottom line of the bitmap instead of the top line, still going from left to right, and continue to the top line of the bitmap.</span></span>

<span data-ttu-id="58238-123">La sortie hexadécimale suivante affiche le contenu du fichier Redbrick.bmp.</span><span class="sxs-lookup"><span data-stu-id="58238-123">The following hexadecimal output shows the contents of the file Redbrick.bmp.</span></span>


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



<span data-ttu-id="58238-124">Le tableau suivant montre les octets de données associés aux structures dans un fichier bitmap.</span><span class="sxs-lookup"><span data-stu-id="58238-124">The following table shows the data bytes associated with the structures in a bitmap file.</span></span>



| <span data-ttu-id="58238-125">Structure</span><span class="sxs-lookup"><span data-stu-id="58238-125">Structure</span></span>                                    | <span data-ttu-id="58238-126">Octets correspondants</span><span class="sxs-lookup"><span data-stu-id="58238-126">Corresponding bytes</span></span> |
|----------------------------------------------|---------------------|
| [<span data-ttu-id="58238-127">**BITMAPFILEHEADER**</span><span class="sxs-lookup"><span data-stu-id="58238-127">**BITMAPFILEHEADER**</span></span>](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | <span data-ttu-id="58238-128">0x00 0x0D</span><span class="sxs-lookup"><span data-stu-id="58238-128">0x00 0x0D</span></span>           |
| <span data-ttu-id="58238-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58238-129">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))</span></span> | <span data-ttu-id="58238-130">0x0E 0x35</span><span class="sxs-lookup"><span data-stu-id="58238-130">0x0E 0x35</span></span>           |
| <span data-ttu-id="58238-131">Tableau [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)</span><span class="sxs-lookup"><span data-stu-id="58238-131">[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) array</span></span>             | <span data-ttu-id="58238-132">0x36 0x75</span><span class="sxs-lookup"><span data-stu-id="58238-132">0x36 0x75</span></span>           |
| <span data-ttu-id="58238-133">Tableau d’index de couleurs</span><span class="sxs-lookup"><span data-stu-id="58238-133">Color-index array</span></span>                            | <span data-ttu-id="58238-134">0x76 0x275</span><span class="sxs-lookup"><span data-stu-id="58238-134">0x76 0x275</span></span>          |



 

 

 
