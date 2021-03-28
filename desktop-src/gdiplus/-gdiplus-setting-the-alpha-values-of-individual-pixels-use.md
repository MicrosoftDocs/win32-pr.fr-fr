---
description: La rubrique utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images montre une méthode non destructrice permettant de modifier les valeurs alpha d’une image.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Définition des valeurs alpha de pixels individuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526073"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="05b9a-103">Définition des valeurs alpha de pixels individuels</span><span class="sxs-lookup"><span data-stu-id="05b9a-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="05b9a-104">La rubrique [utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) montre une méthode non destructrice permettant de modifier les valeurs alpha d’une image.</span><span class="sxs-lookup"><span data-stu-id="05b9a-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="05b9a-105">L’exemple de cette rubrique affiche une image semitransparently, mais les données de pixels de la bitmap ne sont pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="05b9a-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="05b9a-106">Les valeurs alpha sont modifiées uniquement pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="05b9a-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="05b9a-107">L’exemple suivant montre comment modifier les valeurs alpha de pixels individuels.</span><span class="sxs-lookup"><span data-stu-id="05b9a-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="05b9a-108">Le code de l’exemple modifie en fait les informations alpha dans un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="05b9a-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="05b9a-109">L’approche est beaucoup plus lente que l’utilisation d’une matrice de couleurs et d’un objet [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , mais elle vous permet de contrôler les pixels individuels dans l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="05b9a-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



<span data-ttu-id="05b9a-110">L’illustration suivante montre l’image résultante.</span><span class="sxs-lookup"><span data-stu-id="05b9a-110">The following illustration shows the resulting image.</span></span>

![Illustration montrant une image qui devient plus opaque de gauche à droite, sur un rectangle noir](images/image3.png)

<span data-ttu-id="05b9a-112">L’exemple de code précédent utilise des boucles imbriquées pour modifier la valeur alpha de chaque pixel de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="05b9a-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="05b9a-113">Pour chaque pixel, [**bitmap :: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) obtient la couleur existante, [**Color :: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crée une couleur temporaire qui contient la nouvelle valeur alpha, puis [**bitmap :: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) définit la nouvelle couleur.</span><span class="sxs-lookup"><span data-stu-id="05b9a-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="05b9a-114">La valeur alpha est définie en fonction de la colonne de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="05b9a-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="05b9a-115">Dans la première colonne, alpha a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="05b9a-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="05b9a-116">Dans la dernière colonne, alpha a la valeur 255.</span><span class="sxs-lookup"><span data-stu-id="05b9a-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="05b9a-117">Par conséquent, l’image résultante passe d’une transparence totale (sur le bord gauche) à une image entièrement opaque (sur le bord droit).</span><span class="sxs-lookup"><span data-stu-id="05b9a-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="05b9a-118">[**Bitmap :: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) et [**bitmap :: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) vous permettent de contrôler les valeurs de pixel individuelles.</span><span class="sxs-lookup"><span data-stu-id="05b9a-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="05b9a-119">Toutefois, l’utilisation de **bitmap :: GetPixel** et **bitmap :: SetPixel** n’est pas aussi rapide que l’utilisation de la classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) et de la structure [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="05b9a-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



