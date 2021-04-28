---
description: Définition des États DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Définition des États DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092697"
---
# <a name="setting-dxva-hd-states"></a>Définition des États DXVA-HD

Lors du traitement vidéo, l’appareil Microsoft DirectX Video Acceleration High Definition (DXVA-HD) conserve un état persistant d’une image à l’autre. Chaque État a une valeur par défaut documentée. Après avoir configuré l’appareil, définissez les États dont vous souhaitez modifier les valeurs par défaut. Avant de traiter chaque frame, mettez à jour tous les États qui doivent changer.

> [!Note]  
> Cette conception diffère de DXVA-VP. Dans DXVA-VP, l’application doit spécifier tous les paramètres VP avec chaque trame.

 

Les États des appareils se répartissent en deux catégories :

-   Les États de *flux* appliquent chaque flux d’entrée séparément. Vous pouvez appliquer des paramètres différents à chaque flux.
-   Les États de *blit* s’appliquent globalement à l’ensemble de la blit de traitement vidéo.

Les États de flux suivants sont définis.



| État du flux                                   | Description                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **\_État du flux DXVAHD \_ \_ D3DFORMAT**           | Format vidéo d’entrée.                                                                                             |
| **\_format de \_ Frame d’état de flux DXVAHD \_ \_**       | Entrelacement.                                                                                                    |
| **\_ \_ \_ espace colorimétrique d’entrée \_ de l’état du flux DXVAHD \_** | Espace colorimétrique d’entrée. Cet État spécifie la plage de couleurs RVB et la matrice de transfert YCbCr pour le flux d’entrée. |
| **taux de sortie de l' \_ État du flux DXVAHD \_ \_ \_**        | Fréquence d’images de sortie. Cet État contrôle la conversion de la fréquence des images.                                                   |
| **DXVAHD \_ de \_ source d’état de flux \_ \_**        | Rectangle source.                                                                                               |
| **\_Rect de \_ destination d’état de flux DXVAHD \_ \_**   | Rectangle de destination.                                                                                          |
| **\_État de flux DXVAHD \_ \_ alpha**               | Alpha planaire.                                                                                                   |
| **DXVAHD \_ \_ palette d’état de flux \_**             | Palette de couleurs. Cet État s’applique uniquement aux formats d’entrée en palette.                                             |
| **clé de luminance de l' \_ État du flux DXVAHD \_ \_ \_**           | Clé de luminance.                                                                                                       |
| **proportions de l' \_ État du flux DXVAHD \_ \_ \_**       | Proportions de pixels.                                                                                             |
| **\_Filtre d’état de flux DXVAHD \_ \_ \_ xxxx**        | Paramètres de filtre d’image. Le pilote peut prendre en charge la luminosité, le contraste et d’autres filtres d’image.                    |



 

Les États de Blit suivants sont définis :



| État blit                                   | Description                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **\_ \_ \_ Rect cible de l’État DXVAHD BLT \_**         | Rectangle cible.                                                            |
| **\_couleur d' \_ \_ arrière- \_ plan de l’État DXVAHD BLT**    | Couleur d’arrière-plan.                                                            |
| **\_espace de \_ \_ couleurs de \_ sortie \_ de l’état du BLT DXVAHD** | Espace colorimétrique de sortie.                                                          |
| **\_ \_ \_ remplissage alpha de l’État DXVAHD BLT \_**          | Mode de remplissage alpha.                                                             |
| **DXVAHD de l' \_ État du BLT \_ \_**         | La restriction. Cet État contrôle si l’appareil downsamples la sortie. |



 

Pour définir un état de flux, appelez la méthode [**IDXVAHD \_ VideoProcessor :: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) . Pour définir un État blit, appelez la méthode [**IDXVAHD \_ VideoProcessor :: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) . Dans ces deux méthodes, une valeur d’énumération spécifie l’État à définir. Les données d’État sont fournies à l’aide d’une structure de données spécifique à l’État, que l’application convertit en type **void \*** .

L’exemple de code suivant définit le format d’entrée et le rectangle de destination pour le flux 0 et définit la couleur d’arrière-plan sur noir.


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



