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
# <a name="image-stride"></a>STRIDE d’image

Lorsqu’une image vidéo est stockée en mémoire, la mémoire tampon peut contenir des octets de remplissage supplémentaires après chaque ligne de pixels. Les octets de remplissage affectent la manière dont l’image est stockée en mémoire, mais n’affectent pas le mode d’affichage de l’image.

Le *Stride* est le nombre d’octets d’une ligne de pixels en mémoire à la ligne suivante de pixels en mémoire. STRIDE est *également appelé pas* à pas. Si des octets de remplissage sont présents, le Stride est plus large que la largeur de l’image, comme indiqué dans l’illustration suivante.

![Diagramme montrant une image plus un remplissage.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Deux mémoires tampons contenant des images vidéo avec des dimensions égales peuvent avoir deux Strides différents. Si vous traitez une image vidéo, vous devez prendre en compte le Stride.

De plus, il existe deux façons d’organiser une image en mémoire. Dans une image de *haut en haut* , la ligne supérieure des pixels de l’image apparaît en premier dans la mémoire. Dans une image *ascendante* , la dernière ligne de pixels apparaît en premier dans la mémoire. L’illustration suivante montre la différence entre une image de haut en bas et une image de bas en haut.

![Diagramme montrant les images de haut en bas et de bas en haut.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Une image de bas en haut a un Stride négatif, car Stride est défini comme le nombre d’octets nécessaires pour descendre d’une ligne de pixels, par rapport à l’image affichée. Les images YUV doivent toujours être de haut en haut et toute image contenue dans une surface Direct3D doit être de haut en haut. Les images RVB dans la mémoire système sont généralement de bas en haut.

En particulier, les transformations vidéo doivent gérer les mémoires tampons avec des Strides incompatibles, car la mémoire tampon d’entrée ne correspond peut-être pas à la mémoire tampon de sortie. Supposons, par exemple, que vous souhaitiez convertir une image source et écrire le résultat dans une image de destination. Supposons que les deux images aient la même largeur et la même hauteur, mais n’ont peut-être pas le même format de pixel ou le même Stride d’image.

L’exemple de code suivant illustre une approche généralisée pour l’écriture de ce genre de fonction. Il ne s’agit pas d’un exemple complet, car il résume un grand nombre des détails spécifiques.


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



Cette fonction accepte six paramètres :

-   Pointeur vers le début de la ligne de numérisation 0 dans l’image de destination.
-   STRIDE de l’image de destination.
-   Pointeur vers le début de la ligne de numérisation 0 dans l’image source.
-   STRIDE de l’image source.
-   Largeur de l’image en pixels.
-   Hauteur de l’image en pixels.

L’idée générale est de traiter une ligne à la fois, en effectuant une itération sur chaque pixel de la ligne. Supposons que le type \_ de pixel source \_ et le \_ type de pixel de dest \_ sont des structures représentant la disposition des pixels pour les images source et de destination, respectivement. (Par exemple, RGB 32 bits utilise la structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . Tous les formats de pixel n’ont pas une structure prédéfinie.) Le cast du pointeur de tableau vers le type de structure vous permet d’accéder aux composants RGB ou YUV de chaque pixel. Au début de chaque ligne, la fonction stocke un pointeur vers la ligne. À la fin de la ligne, il incrémente le pointeur de la largeur de l’image Stride, qui avance le pointeur vers la ligne suivante.

Cet exemple appelle une fonction hypothétique nommée TransformPixelValue pour chaque pixel. Il peut s’agir de n’importe quelle fonction qui calcule un pixel cible à partir d’un pixel source. Bien entendu, les détails exacts dépendent de la tâche particulière. Par exemple, si vous avez un format YUV planaire, vous devez accéder aux plans Chroma indépendamment du plan de luminance ; avec la vidéo entrelacée, vous devrez peut-être traiter les champs séparément. et ainsi de suite.

Pour obtenir un exemple plus concret, le code suivant convertit une image RGB 32 bits en image AYUV. Les pixels RVB sont accessibles à l’aide d’une structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , et les pixels AYUV sont accessibles à l’aide d’une structure de structure [**\_ AYUVSample8 DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .


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



L’exemple suivant convertit une image RGB 32 bits en image YV12. Cet exemple montre comment gérer un format YUV planaire. (YV12 est un format Planar 4:2:0.) Dans cet exemple, la fonction conserve trois pointeurs distincts pour les trois plans dans l’image cible. Toutefois, l’approche de base est la même que l’exemple précédent.


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



Dans tous ces exemples, il est supposé que l’application a déjà déterminé le Stride de l’image. Vous pouvez parfois recevoir ces informations à partir de la mémoire tampon du média. Dans le cas contraire, vous devez le calculer en fonction du format vidéo. Pour plus d’informations sur le calcul de l’image Stride et l’utilisation des mémoires tampons de média pour la vidéo, consultez [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 
