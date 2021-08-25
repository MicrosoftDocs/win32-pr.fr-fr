---
title: Formats de pixel et modes alpha pris en charge
description: Décrit les formats de pixel et les modes alpha pris en charge par chaque type de cible de rendu.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D, formats de pixel
- Direct2D, modes alpha
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d5b260741cae6aebb447a11692f03dad6e35498a19f33221aa77ac8a8507144a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917159"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formats de pixel et modes alpha pris en charge

Cette rubrique décrit les formats de pixel et les modes alpha pris en charge par les différentes parties de Direct2D, y compris chaque type de cible de rendu, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)et [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource). Elle contient les sections suivantes.

-   [Formats YUV pris en charge pour la source d’image DXGI](#supported-yuv-formats-for-dxgi-image-source)
-   [Spécification d’un format de pixel pour une cible de rendu](#specifying-a-pixel-format-for-a-render-target)
-   [Formats pris en charge pour ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Formats pris en charge pour ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Formats pris en charge pour la cible de rendu compatible](#supported-formats-for-compatible-render-target)
-   [Formats pris en charge pour la cible de rendu de surface DXGI](#supported-formats-for-dxgi-surface-render-target)
-   [Formats pris en charge pour la cible de rendu bitmap WIC](#supported-formats-for-wic-bitmap-render-target)
-   [Formats pris en charge pour ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Spécification d’un format de pixel pour un ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Formats WIC pris en charge](#supported-wic-formats)
-   [Utilisation d’un format non pris en charge](#using-an-unsupported-format)
-   [À propos des modes alpha](#about-alpha-modes)
    -   [À propos des modes alpha prémultipliés et droits](#about-premultiplied-and-straight-alpha-modes)
    -   [Différences entre les caractères alpha de droite et prémultipliés](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Mode Alpha pour les cibles de rendu](#alpha-mode-for-render-targets)
    -   [ClearType et les modes alpha](#cleartype-and-alpha-modes)
-   [Rubriques connexes](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Formats YUV pris en charge pour la source d’image DXGI

Un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) est un fournisseur abstrait de pixels. Il peut être instancié à partir d’un WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) ou [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) prend en charge le même ensemble de formats de pixel et de modes alpha que [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

En plus de ce qui précède, un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) instancié à partir de [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) prend également en charge certains formats de pixel YUV, y compris les données planaires divisées en plusieurs surfaces. Pour plus d’informations sur la configuration requise pour chaque format de pixel, consultez [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) .



| Format                    |
|---------------------------|
| DXGI \_ format \_ AYUV        |
| DXGI \_ format \_ NV12        |
| DXGI \_ format \_ YUY2        |
| DXGI \_ format \_ P208        |
| DXGI \_ format \_ V208        |
| DXGI \_ format \_ V408        |
| \_Format dxgi \_ R8 \_ UNORM   |
| DXGI \_ format \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Spécification d’un format de pixel pour une cible de rendu

Lorsque vous créez une cible de rendu, vous devez spécifier son format de pixel. Pour spécifier le format de pixel, vous utilisez une structure de [**\_ \_ format de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) pour définir le membre **PixelFormat** d’une structure de [**Propriétés de \_ cible de rendu \_ \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) . Ensuite, vous transmettez cette structure à la méthode Create appropriée, telle que [**ID2D1Factory :: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

La structure du [**\_ \_ format de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) a deux champs :

-   **format**, une valeur de [ \_ format dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) qui décrit la taille et la disposition des canaux dans chaque pixel, et
-   **alpha**, valeur [**du \_ \_ mode Alpha d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) qui décrit la façon dont les informations alpha sont interprétées.

L’exemple suivant crée une structure de [**\_ \_ format de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) et l’utilise pour spécifier le format de pixel et le mode Alpha d’un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



Les différentes cibles de rendu prennent en charge des combinaisons différentes de format et de mode Alpha. Les sections suivantes répertorient le format et les combinaisons alpha pris en charge par chaque cible de rendu.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Formats pris en charge pour ID2D1HwndRenderTarget

Les formats pris en charge pour un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) varient selon qu’il s’affiche à l’aide de matériel ou de logiciel, ou si Direct2D gère le mode de rendu automatiquement par défaut.

> [!Note]  
> Nous vous recommandons d’utiliser le format [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) comme format de pixel pour de meilleures performances. Cela s’avère particulièrement utile pour les cibles de rendu logicielles. Les cibles au format BGRA sont plus performantes que les formats RVBA.

 

Lorsque vous créez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), vous utilisez la structure de propriétés de la [**\_ cible de rendu \_ \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) pour spécifier les options de rendu. Les options incluent le format de pixel, comme indiqué dans la section précédente. Le champ type de cette structure vous permet de spécifier si la cible de rendu est rendue sur le matériel ou les logiciels, ou si Direct2D doit déterminer automatiquement le mode de rendu.

Pour permettre à Direct2D de déterminer si la cible de rendu utilise le rendu matériel ou logiciel, utilisez le paramètre [**\_ \_ \_ \_ par défaut du type de cible de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .

Le tableau suivant répertorie les formats pris en charge pour les objets [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) créés à l’aide du paramètre [**\_ \_ \_ \_ par défaut du type de cible de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .



| Format                        | Mode Alpha                       |
|-------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ ignore        |
| \_format dxgi \_ inconnu         | \_Mode Alpha \_ d2d1 \_ inconnu       |



 

Pour forcer une cible de rendu à utiliser le rendu matériel, utilisez le paramètre [**matériel du type de \_ cible de rendu \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . Le tableau suivant répertorie les formats pris en charge pour les objets [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) qui utilisent explicitement le rendu matériel.



| Format                        | Mode Alpha                       |
|-------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | \_Mode Alpha \_ d2d1 \_ inconnu       |
| DXGI \_ format \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ R8G8B8A8 \_ UNORM | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ ignore        |
| \_format dxgi \_ inconnu         | \_Mode Alpha \_ d2d1 \_ inconnu       |



 

Pour forcer une cible de rendu à utiliser le rendu logiciel, utilisez le paramètre [**logiciel du type de \_ cible de rendu \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . Le tableau suivant répertorie les formats pris en charge pour les objets [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) qui utilisent explicitement le rendu logiciel.



| Format                        | Mode Alpha                       |
|-------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ ignore        |
| \_format dxgi \_ inconnu         | \_Mode Alpha \_ d2d1 \_ inconnu       |



 

Que le [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) soit ou non une accélération matérielle, le [format \_ dxgi \_ inconnu](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) utilise le [format \_ dxgi \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) par défaut et le mode Alpha [**\_ \_ \_ Unknown du mode d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) utilise le **mode Alpha d2d1 \_ \_ \_ ignore** par défaut.

## <a name="supported-formats-for-id2d1devicecontext"></a>Formats pris en charge pour ID2D1DeviceContext

à partir de Windows 8 le [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) tire parti de plus de formats de [**haute couleur Direct3D**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) tels que :

-   DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ R16G16B16A16 \_ UNORM
-   DXGI \_ format \_ R16G16B16A16 \_ float
-   DXGI \_ format \_ R32G32B32A32 \_ float

Utilisez la méthode [**ID2D1DeviceContext :: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) pour voir si un format fonctionne sur un contexte de périphérique particulier. Ces formats peuvent également fonctionner sur un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).

ces formats s’ajoutent aux formats pris en charge par l’interface [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dans Windows 7. Pour plus d’informations [, consultez contextes d’appareils et](devices-and-device-contexts.md) de périphériques.

## <a name="supported-formats-for-compatible-render-target"></a>Formats pris en charge pour la cible de rendu compatible

Une cible de rendu compatible (un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) créé par l’une des méthodes [**ID2D1RenderTarget :: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) hérite des formats et des modes alpha pris en charge de la cible de rendu qui l’a créée. Une cible de rendu compatible prend également en charge les combinaisons de format et de mode Alpha suivantes, indépendamment de ce que son parent prend en charge.



| Format                  | Mode Alpha                       |
|-------------------------|----------------------------------|
| \_Format dxgi \_ a8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_Format dxgi \_ a8 \_ UNORM | \_Mode d2d1 \_ alpha \_ simple      |
| \_format dxgi \_ inconnu   | \_Mode Alpha \_ d2d1 \_ inconnu       |



 

Le [format \_ \_ inconnu au format dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) utilise le format de cible de rendu parent par défaut et le mode Alpha [**d2d1 \_ \_ \_ inconnu en mode**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha utilise le mode Alpha **d2d1 \_ \_ \_ prémultiplié** par défaut.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formats pris en charge pour la cible de rendu de surface DXGI

Une cible de rendu DXGI est un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) créé par l’une des méthodes [**ID2D1Factory :: CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) . Il prend en charge les combinaisons de format et de mode Alpha suivantes.



| Format                        | Mode Alpha                       |
|-------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| \_Format dxgi \_ a8 \_ UNORM       | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_Format dxgi \_ a8 \_ UNORM       | \_Mode d2d1 \_ alpha \_ simple      |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ ignore        |



 

> [!Note]  
> Le format doit correspondre au format de la surface DXGI sur laquelle la cible de rendu de la surface DXGI dessine.

 

Le [format \_ \_ inconnu au format dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) utilise le format de surface DXGI par défaut. N’utilisez pas le mode Alpha [**d2d1 \_ \_ \_ inconnu en mode Alpha**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) avec une cible de rendu de surface DXGI. Elle n’a pas de valeur par défaut et entraîne l’échec de la création de la cible de rendu de la surface DXGI.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formats pris en charge pour la cible de rendu bitmap WIC

Une cible de rendu de bitmap WIC est un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) créé par l’une des méthodes [**ID2D1Factory :: CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) . Il prend en charge les combinaisons de format et de mode Alpha suivantes.



| Format                        | Mode Alpha                       |
|-------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_Format dxgi \_ a8 \_ UNORM       | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_Format dxgi \_ a8 \_ UNORM       | \_Mode d2d1 \_ alpha \_ simple      |
| \_Format dxgi \_ a8 \_ UNORM       | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_format dxgi \_ inconnu         | D2D1 \_ \_ mode Alpha \_ ignore        |
| \_format dxgi \_ inconnu         | \_Mode Alpha \_ d2d1 \_ inconnu       |



 

Le format de pixel de la cible de bitmap WIC doit correspondre au format de pixel de la bitmap WIC.

Le [format \_ \_ inconnu au format dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) utilise le format de bitmap WIC par défaut et le mode Alpha [**d2d1 \_ \_ \_ inconnu en mode Alpha**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) utilise par défaut le mode Alpha bitmap WIC.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formats pris en charge pour ID2D1DCRenderTarget

Un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) prend en charge les combinaisons de format et de mode Alpha suivantes.



| Format                        | Mode Alpha                       |
|-------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore        |



 

N’utilisez pas le [format \_ dxgi \_ inconnu](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ou le mode [**alpha \_ \_ \_ inconnu d2d1 en mode Alpha**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) avec un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Elle n’a pas de valeur par défaut et entraîne l’échec de la création de **ID2D1DCRenderTarget** .

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Spécification d’un format de pixel pour un ID2D1Bitmap

En règle générale, les objets [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) prennent en charge les formats et modes alpha suivants (avec certaines restrictions, décrites dans les paragraphes qui suivent).



| Format                                                      | Mode Alpha                       |
|-------------------------------------------------------------|----------------------------------|
| DXGI \_ format \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ format \_ B8G8R8A8 \_ UNORM                               | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_Format dxgi \_ a8 \_ UNORM                                     | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_Format dxgi \_ a8 \_ UNORM                                     | \_Mode d2d1 \_ alpha \_ simple      |
| \_Format dxgi \_ a8 \_ UNORM                                     | \_Mode Alpha \_ d2d1 \_ inconnu       |
| \_format dxgi \_ inconnu                                       | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| \_format dxgi \_ inconnu                                       | D2D1 \_ \_ mode Alpha \_ ignore        |
| \_format dxgi \_ inconnu                                       | \_Mode Alpha \_ d2d1 \_ inconnu       |
| DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement) | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | \_Mode Alpha \_ d2d1 \_ inconnu       |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | \_Mode Alpha \_ d2d1 \_ inconnu       |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | D2D1 \_ \_ mode Alpha \_ prémultiplié |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | D2D1 \_ \_ mode Alpha \_ ignore        |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (Windows 8.1 et versions ultérieures, uniquement)      | \_Mode Alpha \_ d2d1 \_ inconnu       |



 

Quand vous utilisez la méthode [**ID2D1RenderTarget :: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) , vous utilisez le champ **PixelFormat** d’une structure de [**\_ \_ Propriétés de bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) pour spécifier le format de pixel de la nouvelle cible de rendu. Il doit correspondre au format de pixel de la source [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) .

Quand vous utilisez la méthode [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) , vous utilisez le champ **PixelFormat** d’une structure de [**\_ \_ Propriétés de bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (au lieu du membre **PixelFormat** d’une structure de propriétés de la [**\_ \_ cible de \_ rendu d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) ) pour spécifier le format de pixel de la nouvelle cible de rendu. Il doit correspondre au format de pixel de la source de bitmap WIC.

> [!Note]  
> Pour plus d’informations sur la prise en charge des formats de pixel Compressed Block (BCn), consultez [Block compression](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formats WIC pris en charge

Lorsque vous utilisez la méthode [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) pour créer une image bitmap à partir d’une bitmap WIC, ou lorsque vous utilisez la méthode [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) avec un [**IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock), la source WIC doit être dans un format pris en charge par Direct2D.



| Format WIC                     | Format DXGI correspondant     | Mode Alpha correspondant                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | \_Format dxgi \_ a8 \_ UNORM       | \_Mode d2d1 \_ alpha \_ direct ou d2d1 \_ en mode Alpha \_ \_ prémultiplié |
| GUID \_ WICPixelFormat32bppPRGBA | DXGI \_ format \_ R8G8B8A8 \_ UNORM | D2D1 \_ mode \_ alpha \_ prémultiplié ou d2d1 \_ en mode \_ alpha \_ ignore   |
| GUID \_ WICPixelFormat32bppBGR   | DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ ignore                                       |
| GUID \_ WICPixelFormat32bppPBGRA | DXGI \_ format \_ B8G8R8A8 \_ UNORM | D2D1 \_ \_ mode Alpha \_ prémultiplié                                |



 

Pour obtenir un exemple qui montre comment convertir une bitmap WIC en un format pris en charge, consultez [Comment charger une image bitmap à partir d’un fichier](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Utilisation d’un format non pris en charge

L’utilisation d’une combinaison autre que les formats de pixel et les modes alpha répertoriés dans les tableaux précédents produit un [**\_ format de \_ pixel \_ non pris en charge par D2DERR**](direct2d-error-codes.md) ou une erreur **E \_ INVALIDARG** .

## <a name="about-alpha-modes"></a>À propos des modes alpha

### <a name="about-premultiplied-and-straight-alpha-modes"></a>À propos des modes alpha prémultipliés et droits

L’énumération du [**\_ \_ mode Alpha d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indique si le canal alpha utilise des caractères alpha prémultipliés, des caractères alpha droits ou s’ils doivent être ignorés et considérés comme opaques. Avec l’alpha direct, le canal alpha indique une valeur qui correspond à la transparence d’une couleur.

Les couleurs sont toujours traitées comme des caractères alpha rectilignes par les commandes et les pinceaux de dessin Direct2D, quel que soit le format de destination.

Avec l’alpha prémultiplié, chaque canal de couleur est mis à l’échelle en fonction de la valeur alpha. En règle générale, aucune valeur de canal de couleur n’est supérieure à la valeur de canal alpha. Si une valeur de canal de couleur dans un format prémultiplié est supérieure au canal alpha, la mathématique de fusion de source standard crée une fusion additive.

La valeur du canal alpha lui-même est la même dans les valeurs alpha et prémultipliées.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Différences entre les caractères alpha de droite et prémultipliés

Lors de la description d’une couleur RVBA à l’aide de l’alpha direct, la valeur alpha de la couleur est stockée dans le canal alpha. Par exemple, pour décrire une couleur rouge qui est opaque à 60%, utilisez les valeurs suivantes : (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). La valeur 255 indique la couleur rouge complète et 153 (ce qui correspond à 60% de 255) indique que la couleur doit avoir une opacité de 60%.

Quand vous décrivez une couleur RVBA à l’aide de l’alpha prémultiplié, chaque couleur est multipliée par la valeur alpha : (255 \* 0,6, 0 \* 0,6, 0 \* 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Quel que soit le mode Alpha de la cible de rendu, les valeurs [**\_ \_ F de couleur d2d1**](d2d1-color-f.md) sont toujours interprétées comme des valeurs alpha directes. Par exemple, lorsque vous spécifiez la couleur d’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) à utiliser avec une cible de rendu qui utilise le mode Alpha prémultiplié, spécifiez la couleur comme vous le feriez si la cible de rendu utilisait une alpha simple. Lorsque vous peignez avec le pinceau, Direct2D convertit la couleur au format de destination pour vous.

### <a name="alpha-mode-for-render-targets"></a>Mode Alpha pour les cibles de rendu

Quel que soit le paramètre de mode alpha, le contenu d’une cible de rendu prend en charge la transparence. Par exemple, si vous dessinez un rectangle rouge partiellement transparent avec une cible de rendu avec un mode Alpha [**d2d1 \_ alpha \_ mode \_ ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), le rectangle apparaît en rose (si l’arrière-plan est blanc).

Si vous dessinez un rectangle rouge partiellement transparent lorsque le mode Alpha [**est \_ \_ \_ prémultiplié par d2d1 alpha**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), le rectangle apparaît en rose (en supposant que l’arrière-plan est blanc) et vous pouvez le voir jusqu’à ce qui se trouve derrière la cible de rendu. Cela est utile lorsque vous utilisez un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pour effectuer le rendu dans une fenêtre transparente ou lorsque vous utilisez une cible de rendu compatible (un rendu ciblé créé par la méthode [**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) pour créer une bitmap qui prend en charge la transparence.

### <a name="cleartype-and-alpha-modes"></a>ClearType et les modes alpha

Si vous spécifiez un mode Alpha autre que le [**\_ mode d2d1 alpha \_ \_ ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) pour une cible de rendu, le mode d’anticrénelage de texte passe automatiquement du [**\_ \_ \_ mode antialias du texte d2d1 CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) à **d2d1 \_ mode anticrénelage de texte \_ \_ en nuances de gris**. (Lorsque vous spécifiez un mode Alpha **du \_ mode Alpha d2d1 \_ \_ inconnu**, Direct2D définit le alpha pour vous, selon le type de la cible de rendu.)

Vous pouvez utiliser la méthode [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) pour rétablir le mode antialias du texte [**d2d1 \_ \_ \_ CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode), mais le rendu du texte CLEARTYPE sur une surface transparente peut générer des résultats imprévisibles. Si vous souhaitez afficher du texte ClearType sur une cible de rendu transparente, nous vous recommandons d’utiliser l’une des deux techniques suivantes.

-   Utilisez la méthode [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) pour découper la cible de rendu dans la zone où le texte sera rendu, puis appelez la méthode [**Clear**](id2d1rendertarget-clear.md) et spécifiez une couleur opaque, puis Restituez votre texte.
-   Utilisez [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) pour dessiner un rectangle opaque derrière la zone dans laquelle le texte sera rendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_Format de pixel d2d1 \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**\_Mode Alpha \_ d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[\_format dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 