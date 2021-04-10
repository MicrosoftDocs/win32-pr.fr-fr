---
title: Traitement de la vidéo
description: Traitement de la vidéo
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Plug-ins du lecteur Windows Media, DSP vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, traitement vidéo
- Plug-ins DSP, traitement vidéo
- plug-ins vidéo DSP, traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031422"
---
# <a name="processing-the-video"></a><span data-ttu-id="fe842-108">Traitement de la vidéo</span><span class="sxs-lookup"><span data-stu-id="fe842-108">Processing the Video</span></span>

<span data-ttu-id="fe842-109">Les détails du traitement des vidéos varient pour chaque format. Cela n’entre pas dans le cadre de cette documentation pour fournir ces informations.</span><span class="sxs-lookup"><span data-stu-id="fe842-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="fe842-110">Dans un sens général, l’objectif du plug-in est de modifier les données de couleur dans la mémoire tampon d’entrée, puis de copier les données dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="fe842-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="fe842-111">L’exemple de plug-in traite deux types de formats vidéo : YUV et RVB.</span><span class="sxs-lookup"><span data-stu-id="fe842-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="fe842-112">Pour la vidéo YUV, les informations de couleur rouge et bleue sont encodées dans les valeurs V et V et le niveau de luminance est représenté par la valeur Y. la valeur verte est encodée et peut être récupérée à l’aide d’un algorithme.</span><span class="sxs-lookup"><span data-stu-id="fe842-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="fe842-113">L’exemple de plug-in change simplement les valeurs vous-même et V pour affecter le niveau de couleur.</span><span class="sxs-lookup"><span data-stu-id="fe842-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="fe842-114">Chaque octet U ou V a une valeur comprise entre zéro et 255.</span><span class="sxs-lookup"><span data-stu-id="fe842-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="fe842-115">Le plug-in ajuste d’abord chaque valeur pour qu’elle soit représentée par une plage comprise entre-128 et 127, puis met à l’échelle la valeur en fonction du facteur d’échelle fourni.</span><span class="sxs-lookup"><span data-stu-id="fe842-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="fe842-116">Enfin, le code réajuste la valeur pour la plage de zéro à 255 d’origine et copie les données dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="fe842-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="fe842-117">L’exemple de code suivant traite la vidéo UYVY.</span><span class="sxs-lookup"><span data-stu-id="fe842-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="fe842-118">Dans ce format, chaque octet est une valeur U ou Y.</span><span class="sxs-lookup"><span data-stu-id="fe842-118">In this format, every other byte is a U or Y value.</span></span>


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="fe842-119">Pour la vidéo RVB, les informations de couleur et de luminance sont encodées sous forme de valeurs séparées de rouge, de vert et de bleu.</span><span class="sxs-lookup"><span data-stu-id="fe842-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="fe842-120">L’exemple de plug-in calcule la moyenne des trois valeurs pour déterminer la valeur du gris, puis ajuste chaque valeur de couleur à l’aide du facteur d’échelle fourni.</span><span class="sxs-lookup"><span data-stu-id="fe842-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="fe842-121">Une fois encore, les valeurs doivent être normalisées pour la plage-128 à 127 avant la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="fe842-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="fe842-122">Le code suivant de Process32Bit illustre le processus pour RGB32 :</span><span class="sxs-lookup"><span data-stu-id="fe842-122">The following code from Process32Bit shows the process for RGB32:</span></span>


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="fe842-123">Pour plus d’informations sur les formats vidéo, consultez le [site Web du FourCC](../directshow/fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fe842-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe842-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe842-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe842-125">**Implémentation d’un plug-in de DSP vidéo**</span><span class="sxs-lookup"><span data-stu-id="fe842-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 