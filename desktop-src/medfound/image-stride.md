---
description: STRIDE d’image
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: STRIDE d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556983"
---
# <a name="image-stride"></a><span data-ttu-id="64584-103">STRIDE d’image</span><span class="sxs-lookup"><span data-stu-id="64584-103">Image Stride</span></span>

<span data-ttu-id="64584-104">Lorsqu’une image vidéo est stockée en mémoire, la mémoire tampon peut contenir des octets de remplissage supplémentaires après chaque ligne de pixels.</span><span class="sxs-lookup"><span data-stu-id="64584-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="64584-105">Les octets de remplissage affectent la manière dont l’image est stockée en mémoire, mais n’affectent pas le mode d’affichage de l’image.</span><span class="sxs-lookup"><span data-stu-id="64584-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="64584-106">Le *Stride* est le nombre d’octets d’une ligne de pixels en mémoire à la ligne suivante de pixels en mémoire.</span><span class="sxs-lookup"><span data-stu-id="64584-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="64584-107">STRIDE est *également appelé pas* à pas.</span><span class="sxs-lookup"><span data-stu-id="64584-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="64584-108">Si des octets de remplissage sont présents, le Stride est plus large que la largeur de l’image, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="64584-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![Diagramme montrant une image plus un remplissage.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="64584-110">Deux mémoires tampons contenant des images vidéo avec des dimensions égales peuvent avoir deux Strides différents.</span><span class="sxs-lookup"><span data-stu-id="64584-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="64584-111">Si vous traitez une image vidéo, vous devez prendre en compte le Stride.</span><span class="sxs-lookup"><span data-stu-id="64584-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="64584-112">De plus, il existe deux façons d’organiser une image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="64584-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="64584-113">Dans une image de *haut en haut* , la ligne supérieure des pixels de l’image apparaît en premier dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="64584-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="64584-114">Dans une image *ascendante* , la dernière ligne de pixels apparaît en premier dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="64584-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="64584-115">L’illustration suivante montre la différence entre une image de haut en bas et une image de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="64584-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![Diagramme montrant les images de haut en bas et de bas en haut.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="64584-117">Une image de bas en haut a un Stride négatif, car Stride est défini comme le nombre d’octets nécessaires pour descendre d’une ligne de pixels, par rapport à l’image affichée.</span><span class="sxs-lookup"><span data-stu-id="64584-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="64584-118">Les images YUV doivent toujours être de haut en haut et toute image contenue dans une surface Direct3D doit être de haut en haut.</span><span class="sxs-lookup"><span data-stu-id="64584-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="64584-119">Les images RVB dans la mémoire système sont généralement de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="64584-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="64584-120">En particulier, les transformations vidéo doivent gérer les mémoires tampons avec des Strides incompatibles, car la mémoire tampon d’entrée ne correspond peut-être pas à la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="64584-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="64584-121">Supposons, par exemple, que vous souhaitiez convertir une image source et écrire le résultat dans une image de destination.</span><span class="sxs-lookup"><span data-stu-id="64584-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="64584-122">Supposons que les deux images aient la même largeur et la même hauteur, mais n’ont peut-être pas le même format de pixel ou le même Stride d’image.</span><span class="sxs-lookup"><span data-stu-id="64584-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="64584-123">L’exemple de code suivant illustre une approche généralisée pour l’écriture de ce genre de fonction.</span><span class="sxs-lookup"><span data-stu-id="64584-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="64584-124">Il ne s’agit pas d’un exemple complet, car il résume un grand nombre des détails spécifiques.</span><span class="sxs-lookup"><span data-stu-id="64584-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



<span data-ttu-id="64584-125">Cette fonction accepte six paramètres :</span><span class="sxs-lookup"><span data-stu-id="64584-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="64584-126">Pointeur vers le début de la ligne de numérisation 0 dans l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="64584-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="64584-127">STRIDE de l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="64584-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="64584-128">Pointeur vers le début de la ligne de numérisation 0 dans l’image source.</span><span class="sxs-lookup"><span data-stu-id="64584-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="64584-129">STRIDE de l’image source.</span><span class="sxs-lookup"><span data-stu-id="64584-129">The stride of the source image.</span></span>
-   <span data-ttu-id="64584-130">Largeur de l’image en pixels.</span><span class="sxs-lookup"><span data-stu-id="64584-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="64584-131">Hauteur de l’image en pixels.</span><span class="sxs-lookup"><span data-stu-id="64584-131">The height of the image in pixels.</span></span>

<span data-ttu-id="64584-132">L’idée générale est de traiter une ligne à la fois, en effectuant une itération sur chaque pixel de la ligne.</span><span class="sxs-lookup"><span data-stu-id="64584-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="64584-133">Supposons que le type \_ de pixel source \_ et le \_ type de pixel de dest \_ sont des structures représentant la disposition des pixels pour les images source et de destination, respectivement.</span><span class="sxs-lookup"><span data-stu-id="64584-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="64584-134">(Par exemple, RGB 32 bits utilise la structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) .</span><span class="sxs-lookup"><span data-stu-id="64584-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="64584-135">Tous les formats de pixel n’ont pas une structure prédéfinie.) Le cast du pointeur de tableau vers le type de structure vous permet d’accéder aux composants RGB ou YUV de chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="64584-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="64584-136">Au début de chaque ligne, la fonction stocke un pointeur vers la ligne.</span><span class="sxs-lookup"><span data-stu-id="64584-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="64584-137">À la fin de la ligne, il incrémente le pointeur de la largeur de l’image Stride, qui avance le pointeur vers la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="64584-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="64584-138">Cet exemple appelle une fonction hypothétique nommée TransformPixelValue pour chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="64584-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="64584-139">Il peut s’agir de n’importe quelle fonction qui calcule un pixel cible à partir d’un pixel source.</span><span class="sxs-lookup"><span data-stu-id="64584-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="64584-140">Bien entendu, les détails exacts dépendent de la tâche particulière.</span><span class="sxs-lookup"><span data-stu-id="64584-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="64584-141">Par exemple, si vous avez un format YUV planaire, vous devez accéder aux plans Chroma indépendamment du plan de luminance ; avec la vidéo entrelacée, vous devrez peut-être traiter les champs séparément. et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="64584-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="64584-142">Pour obtenir un exemple plus concret, le code suivant convertit une image RGB 32 bits en image AYUV.</span><span class="sxs-lookup"><span data-stu-id="64584-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="64584-143">Les pixels RVB sont accessibles à l’aide d’une structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , et les pixels AYUV sont accessibles à l’aide d’une structure de structure [**\_ AYUVSample8 DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .</span><span class="sxs-lookup"><span data-stu-id="64584-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



<span data-ttu-id="64584-144">L’exemple suivant convertit une image RGB 32 bits en image YV12.</span><span class="sxs-lookup"><span data-stu-id="64584-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="64584-145">Cet exemple montre comment gérer un format YUV planaire.</span><span class="sxs-lookup"><span data-stu-id="64584-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="64584-146">(YV12 est un format Planar 4:2:0.) Dans cet exemple, la fonction conserve trois pointeurs distincts pour les trois plans dans l’image cible.</span><span class="sxs-lookup"><span data-stu-id="64584-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="64584-147">Toutefois, l’approche de base est la même que l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="64584-147">However, the basic approach is the same as the previous example.</span></span>


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



<span data-ttu-id="64584-148">Dans tous ces exemples, il est supposé que l’application a déjà déterminé le Stride de l’image.</span><span class="sxs-lookup"><span data-stu-id="64584-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="64584-149">Vous pouvez parfois recevoir ces informations à partir de la mémoire tampon du média.</span><span class="sxs-lookup"><span data-stu-id="64584-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="64584-150">Dans le cas contraire, vous devez le calculer en fonction du format vidéo.</span><span class="sxs-lookup"><span data-stu-id="64584-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="64584-151">Pour plus d’informations sur le calcul de l’image Stride et l’utilisation des mémoires tampons de média pour la vidéo, consultez [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="64584-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64584-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64584-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64584-153">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="64584-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="64584-154">Types de médias</span><span class="sxs-lookup"><span data-stu-id="64584-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
