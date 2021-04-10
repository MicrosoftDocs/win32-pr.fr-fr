---
description: Cette rubrique décrit deux concepts connexes, le rapport hauteur/largeur des images et les proportions en pixels.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Rapport hauteur/largeur des images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201858"
---
# <a name="picture-aspect-ratio"></a>Rapport hauteur/largeur des images

Cette rubrique décrit deux concepts connexes, le rapport hauteur/largeur des images et les proportions en pixels. Il décrit ensuite comment ces concepts sont exprimés en Microsoft Media Foundation à l’aide de types de médias.

-   [Rapport hauteur/largeur des images](#picture-aspect-ratio)
    -   [Cadre](#letterboxing)
    -   [Panoramique et numérisation](#pan-and-scan)
-   [Proportions de pixels](#pixel-aspect-ratio)
-   [Utilisation des proportions](#working-with-aspect-ratios)
-   [Exemples de code](#code-examples)
    -   [Recherche de la zone d’affichage](#finding-the-display-area)
    -   [Conversion entre les proportions de pixels](#converting-between-pixel-aspect-ratios)
    -   [Calcul de la zone de bandes](#calculating-the-letterbox-area)
-   [Rubriques connexes](#related-topics)

## <a name="picture-aspect-ratio"></a>Rapport hauteur/largeur des images

Les proportions d' *image* définissent la forme de l’image vidéo affichée. Les proportions d’image sont X :Y, où X :Y est le rapport entre la largeur de l’image et la hauteur de l’image. La plupart des normes vidéo utilisent le rapport hauteur/largeur des images 4:3 ou 16:9. Les proportions 16:9 sont généralement appelées *panoramiques*. Le film cinématographique utilise souvent des proportions 1:85:1 ou 1:66:1. Les proportions de l’image sont également appelées proportions d' *affichage* (Dar).

![Diagramme montrant les proportions 4:3 et 16:9](images/aspect-ratio01.png)

Parfois, l’image vidéo n’a pas la même forme que la zone d’affichage. Par exemple, une vidéo 4:3 peut être affichée sur un téléviseur grand écran (16 × 9). Dans une vidéo informatique, la vidéo peut être affichée à l’intérieur d’une fenêtre qui a une taille arbitraire. Dans ce cas, il existe trois façons d’ajuster l’image dans la zone d’affichage :

-   Étirer l’image le long d’un axe pour l’ajuster à la zone d’affichage.
-   Mettez l’image à l’échelle pour l’ajuster à la zone d’affichage tout en conservant les proportions d’image d’origine.
-   Rognez l’image.

L’étirement de l’image pour l’ajuster à la zone d’affichage est presque toujours incorrect, car elle ne conserve pas les proportions de l’image correctes.

### <a name="letterboxing"></a>Cadre

Le processus de mise à l’échelle d’une image grand écran pour l’adapter à un affichage 4:3 est appelé *cadre*, comme indiqué dans le diagramme suivant. Les zones de rectanglular résultantes en haut et en bas de l’image sont généralement remplies en noir, bien que d’autres couleurs puissent être utilisées.

![Diagramme montrant la bonne façon de les bandes](images/aspect-ratio02.png)

La casse inverse, avec la mise à l’échelle d’une image 4:3 pour l’adapter à un écran panoramique, est parfois appelée *pillarboxing*. Toutefois, *le terme de* la zone de données est également utilisé dans un sens général, pour signifier la mise à l’échelle d’une image vidéo pour l’adapter à une zone d’affichage donnée.

![Diagramme montrant pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Panoramique et numérisation

Le panoramique et l’analyse sont une technique par laquelle une image panoramique est rognée dans une zone rectangulaire de 4 × 3, pour être affichée sur un appareil d’affichage 4:3. L’image obtenue remplit l’intégralité de l’affichage, sans nécessiter de zones de bandes noires, mais les parties de l’image d’origine sont rognées de l’image. La zone rognée peut se déplacer d’un cadre à l’autres, comme la zone d’intérêt change. Le terme « panoramique » dans *panoramique et numérisation* fait référence à l’effet panoramique provoqué par le déplacement de la zone panoramique-et-numérisation.

![Diagramme montrant le panoramique et l’analyse](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Proportions de pixels

Les proportions en *pixels* (par) mesurent la forme d’un pixel.

Lorsqu’une image numérique est capturée, l’image est échantillonnée à la fois verticalement et horizontalement, ce qui se traduit par un tableau rectangulaire d’échantillons quantifiés, appelé *pixels* ou *pixels*. La forme de la grille d’échantillonnage détermine la forme des pixels de l’image numérisée.

Voici un exemple qui utilise des nombres réduits pour simplifier la mathématique. Supposons que l’image d’origine est carrée (autrement dit, les proportions de l’image sont 1:1); et supposons que la grille d’échantillonnage contient 12 éléments, organisés en une grille 4 × 3. La forme de chaque pixel résultant sera plus grande que la largeur. Plus précisément, la forme de chaque pixel sera 3 × 4. Les pixels qui ne sont pas des carrés sont appelés des *pixels non carrés*.

![Diagramme montrant une grille d’échantillonnage non carrée](images/aspect-ratio05.png)

Les proportions de pixels s’appliquent également au périphérique d’affichage. La forme physique du périphérique d’affichage et la résolution de pixel physique (en travers et en baisse) déterminent le pair du périphérique d’affichage. Les moniteurs d’ordinateur utilisent généralement des pixels carrés. Si l’image PAR et l’affichage PAR ne correspondent pas, l’image doit être mise à l’échelle dans une dimension, verticalement ou horizontalement, afin de s’afficher correctement. La formule suivante est associée à, à l’aspect des proportions (DAR) et à la taille de l’image en pixels :

*Dar* = (*largeur de l’image en pixels*  /  *hauteur de l’image en pixels*) × *par*

Notez que la largeur de l’image et la hauteur de l’image dans cette formule font référence à l’image en mémoire, et non à l’image affichée.

Voici un exemple concret : la vidéo analogique NTSC-M contient 480 lignes de numérisation dans la zone d’image active. ITU-R Rec. BT. 601 spécifie un taux d’échantillonnage horizontal de 704 pixels visibles par ligne, ce qui génère une image numérique avec 704 x 480 pixels. Les proportions de l’image prévues sont 4:3, ce qui donne un pas de 10:11.

-   DAR : 4:3
-   Largeur en pixels : 704
-   Hauteur en pixels : 480
-   PAR : 10/11

4/3 = (704/420) x (10/11)

Pour afficher correctement cette image sur un appareil d’affichage avec des pixels carrés, vous devez mettre à l’échelle la largeur par 10/11 ou la hauteur de 11/10.

## <a name="working-with-aspect-ratios"></a>Utilisation des proportions

La forme correcte d’une image vidéo est définie par le proportions en *pixels* (par) et la *zone d’affichage*.

-   Le pair définit la forme des pixels dans une image. Les pixels carrés ont un rapport hauteur/largeur de 1:1. Tout autre rapport hauteur/largeur décrit un pixel non carré. Par exemple, la télévision NTSC utilise une PAR 10:11. En supposant que vous présentiez la vidéo sur un moniteur d’ordinateur, l’affichage présente des pixels carrés (1:1 PAR). Le pair du contenu source est fourni dans l’attribut de proportions [**MF \_ Mt en \_ \_ \_ pixels**](mf-mt-pixel-aspect-ratio-attribute.md) sur le type de média.
-   La zone d’affichage est la région de l’image vidéo qui est destinée à être affichée. Deux zones d’affichage pertinentes peuvent être spécifiées dans le type de média :
    -   Ouverture pan-and-Scan. L’ouverture pan-and-Scan est une région 4 × 3 de vidéo qui doit être affichée en mode panoramique/numérisation. Il est utilisé pour afficher un contenu à grand écran sur un affichage 4 × 3 sans cadre. L’ouverture de la panoramisation et de l’analyse est indiquée dans l’attribut de l’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) et doit être utilisée uniquement lorsque l’attribut d’activation de l' [**\_ \_ \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-enabled-attribute.md) a la **valeur true**.
    -   Afficher l’ouverture. Cette ouverture est définie dans certaines normes vidéo. Tout ce qui se trouve en dehors de l’ouverture d’affichage est la région de suranalyse et ne doit pas être affiché. Par exemple, la télévision NTSC est de 720 × 480 pixels avec une ouverture d’affichage de 704 × 480. L’ouverture de l’affichage est indiquée dans l’attribut de l’ouverture de l’affichage de la version d' [**\_ \_ \_ \_ affichage minimale MF MT**](mf-mt-minimum-display-aperture-attribute.md) . S’il est présent, il doit être utilisé lorsque le mode pan-and-Scan a la **valeur false**.

Si le mode pan-and-can a la **valeur false** et qu’aucune ouverture n’est définie, la totalité de l’image vidéo doit être affichée. En fait, c’est le cas pour la plupart des contenus vidéo autres que la télévision et les vidéos DVD. Les proportions de l’image entière sont calculées en fonction de la largeur de la zone d’affichage (largeur de la *zone d’affichage*  /  ) × *par*.

## <a name="code-examples"></a>Exemples de code

### <a name="finding-the-display-area"></a>Recherche de la zone d’affichage

Le code suivant montre comment obtenir la zone d’affichage à partir du type de média.


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>Conversion entre les proportions de pixels

Le code suivant montre comment convertir un rectangle d’un proportions de pixels (PAR) en un autre, tout en conservant les proportions d’image.


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>Calcul de la zone de bandes

Le code suivant calcule la zone de bandes en fonction d’un rectangle source et d’un rectangle de destination. Il est supposé que les deux rectangles ont le même PAR.


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[**\_ouverture de \_ l' \_ affichage \_ de la version MF**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**\_ \_ analyse panoramique MF \_ MT \_ activée**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



