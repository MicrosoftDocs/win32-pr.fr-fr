---
title: Traitement de la vidéo
description: Traitement de la vidéo
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- plug-ins Lecteur Windows Media, DSP de vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, traitement vidéo
- Plug-ins DSP, traitement vidéo
- plug-ins vidéo DSP, traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea168199270cfe8029b7b9303a7745db2c255f4268252a5bd80472a73c6f2f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334022"
---
# <a name="processing-the-video"></a>Traitement de la vidéo

Les détails du traitement des vidéos varient pour chaque format. Cela n’entre pas dans le cadre de cette documentation pour fournir ces informations. Dans un sens général, l’objectif du plug-in est de modifier les données de couleur dans la mémoire tampon d’entrée, puis de copier les données dans la mémoire tampon de sortie.

L’exemple de plug-in traite deux types de formats vidéo : YUV et RVB.

Pour la vidéo YUV, les informations de couleur rouge et bleue sont encodées dans les valeurs V et V et le niveau de luminance est représenté par la valeur Y. la valeur verte est encodée et peut être récupérée à l’aide d’un algorithme. L’exemple de plug-in change simplement les valeurs vous-même et V pour affecter le niveau de couleur. Chaque octet U ou V a une valeur comprise entre zéro et 255. Le plug-in ajuste d’abord chaque valeur pour qu’elle soit représentée par une plage comprise entre-128 et 127, puis met à l’échelle la valeur en fonction du facteur d’échelle fourni. Enfin, le code réajuste la valeur pour la plage de zéro à 255 d’origine et copie les données dans la mémoire tampon de sortie. L’exemple de code suivant traite la vidéo UYVY. Dans ce format, chaque octet est une valeur U ou Y.


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



Pour la vidéo RVB, les informations de couleur et de luminance sont encodées sous forme de valeurs séparées de rouge, de vert et de bleu. L’exemple de plug-in calcule la moyenne des trois valeurs pour déterminer la valeur du gris, puis ajuste chaque valeur de couleur à l’aide du facteur d’échelle fourni. Une fois encore, les valeurs doivent être normalisées pour la plage-128 à 127 avant la mise à l’échelle. Le code suivant de Process32Bit illustre le processus pour RGB32 :


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



Pour plus d’informations sur les formats vidéo, consultez le [site Web du FourCC](../directshow/fourcc-codes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in de DSP vidéo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 