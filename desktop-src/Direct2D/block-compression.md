---
title: Compression de blocs
description: Décrit le fonctionnement de la compression de bloc et comment l’utiliser dans WIC et Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8ee83911cc7be1ab6e611a735a7a5b3a7397c472b78e3192468d2e323ed0c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331741"
---
# <a name="block-compression"></a>Compression de blocs

à partir de Windows 8.1, Direct2D prend en charge plusieurs formats de pixel compressés en bloc. en outre, Windows 8.1 contient un nouveau codec DDS (Windows Imaging Component) pour permettre le chargement et le stockage d’images compressées de bloc dans le format de fichier DDS. La compression de bloc est une technique permettant de réduire la quantité de mémoire graphique consommée par le contenu de la bitmap. En utilisant la compression de bloc, votre application peut réduire la consommation de mémoire et les temps de chargement pour les mêmes images de résolution. Ou bien, votre application peut utiliser des images de résolution plus ou moins importantes tout en conservant le même encombrement mémoire GPU.

la compression de bloc a été utilisée par les applications Direct3D depuis longtemps, et avec Windows 8.1 est également disponible pour les développeurs d’applications standard et Direct2D.

Cette rubrique décrit le fonctionnement de la compression de bloc et comment l’utiliser dans WIC et Direct2D.

## <a name="about-block-compression"></a>À propos de la compression de bloc

La [compression de bloc](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) fait référence à une classe de techniques de compression pour réduire la taille des textures. Direct3D 11 prend en charge jusqu’à 7 formats BC différents en fonction du niveau de fonctionnalité. dans Windows 8.1 Direct2D introduit la prise en charge des formats BC1, BC2 et BC3 qui sont disponibles dans tous les niveaux de fonctionnalité.

### <a name="how-block-compression-works"></a>Fonctionnement de la compression de bloc

Les formats compressés de bloc utilisent tous la même technique de base pour réduire l’espace consommé par les données de couleur. Cette section résume l’algorithme le plus simple, BC1. Pour obtenir une explication plus détaillée, consultez [bloquer la compression](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

Tout d’abord, l’image est divisée en blocs de 4 x 4 pixels. Chaque bloc est compressé séparément.

> [!Note]  
> Cela signifie que la largeur et la hauteur d’une image doivent chacune être un multiple de 4 pixels pour être compressés par blocs.

 

Cet exemple d’image montre un bloc de pixels 4x4 dans une image.

![un exemple d’image montre un bloc de pixels 4x4 dans une image.](images/dds1.png)

Ensuite, dans un bloc de 4 par 4, deux couleurs « référence » sont sélectionnées et sont encodées sous la forme de valeurs de 2 16 bits (5 bits rouges, 6 bits verts, 5 bits bleus). Le choix de ces couleurs affecte de manière significative la qualité de l’image et n’est pas trivial. Deux couleurs intermédiaires sont calculées en interpolant de manière linéaire entre les deux couleurs de référence dans l’espace de couleurs RVB. Cela produit un total de 4 couleurs possibles différentes ; une valeur d’index à deux bits est assignée à chaque couleur. Toutefois, Notez que seules les deux couleurs de point de terminaison doivent être stockées lorsque l’interpolation est fixe.

Dans cette figure, les couleurs 0 et 3 sont sélectionnées en tant que couleurs de « référence » pour le bloc, tandis que les couleurs 1 et 2 sont calculées à l’aide d’une interpolation linéaire.

![Diagramme qui montre le calcul de 4 valeurs de couleur pour représenter le bloc.](images/dds2.png)

Enfin, chaque pixel du bloc est mappé à l’une des quatre couleurs calculées précédemment, et chaque pixel est encodé à l’aide de la valeur d’index à deux bits.

La quantité totale de données utilisées pour représenter ces 16 pixels est la suivante :

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Cela aboutit à une densité moyenne de 4 bits par pixel. Pour comparaison, le format DXGI \_ courant \_ B8G8R8A8 \_ UNORM pixel consomme 32 bits par pixel.

Ce diagramme montre que chaque pixel est encodé sous la forme d’un index 2 bits. Le bloc entier est encodé en 64 bits.

![calcul de 4 valeurs de couleur pour représenter le bloc.](images/dds3.png)

Il existe des variantes pour prendre en charge les données alpha et le nombre variable de canaux de couleurs. BC6H et BC7 utilisent des algorithmes très différents afin de prendre en charge le contenu HDR (High dynamique Range) et d’augmenter la qualité de l’image, respectivement.

### <a name="directdraw-surface-dds-file-format"></a>Format de fichier de la surface DirectDraw (DDS)

Les données compressées de bloc sont généralement stockées dans des fichiers de [surface DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) . Vous connaissez peut-être les fichiers DDS si vous êtes un développeur Direct3D. Notez que Direct2D prend uniquement en charge certaines fonctionnalités DDS. Pour plus d’informations, consultez [spécifications DDS](#dds-requirements).

### <a name="advantages-of-block-compression"></a>Avantages de la compression par bloc

Les formats compressés de bloc diffèrent des formats de compression d’image d’industrie courants tels que JPEG dans la mesure où les formats BC sont pris en charge en mode natif par les GPU modernes. Cela signifie que vous pouvez charger directement une image compressée de bloc sur le GPU sans décodage ni décompression. Les formats BC consomment de 4 à 8 bits par pixel en moyenne ; par rapport à une image bitmap BGRA standard non compressée 32 par pixel, cela entraîne des économies de mémoire de 75% à 87,5%. En outre, étant donné qu’il n’y a pas d’étape de décodage, le temps nécessaire pour charger une image BC est considérablement réduit par rapport aux formats tels que JPEG.

### <a name="when-to-use-block-compression"></a>Quand utiliser la compression de bloc

Vous devez envisager d’utiliser des images compressées de bloc dans votre application au lieu d’autres formats tels que JPEG pour réduire la consommation de mémoire des bitmaps ou pour réduire le décodage et le temps de chargement.

Toutefois, la compression de bloc n’est pas appropriée dans tous les cas et nécessite des compromis. Tout d’abord, les algorithmes de compression de bloc sont perdus. La compression de bloc fonctionne bien avec le contenu de photographique naturel, mais elle peut introduire des artefacts visuels indésirables dans des images avec des limites nettes et à contraste élevé, telles que des captures d’écran générées par ordinateur. Vous devez vous assurer que les ressources de l’image compressée du bloc ont une qualité d’image acceptable avant de les utiliser.

Deuxièmement, les fichiers DDS compressés sont généralement consomment plus d’espace sur le disque que les images JPEG comparables. Cela augmentera ensuite la taille du package de votre application et les besoins en bande passante réseau.

## <a name="using-block-compression"></a>Utilisation de la compression de bloc

Cette section explique comment générer et utiliser des éléments multimédias compressés dans une application Direct2D.

### <a name="overview"></a>Vue d’ensemble

Bloquer les fichiers DDS compressés est un format optimisé pour le runtime, ce qui signifie qu’ils sont optimisés pour de bonnes performances au moment de l’exécution de l’application. Nous vous recommandons de continuer à utiliser votre pipeline de création et d’édition de ressources existantes, et de passer uniquement au format compressé de bloc lorsque vous les importez dans votre projet d’application, ou au moment de la génération.

### <a name="dds-requirements"></a>Configuration de DDS requise

Le format de fichier DDS a été conçu pour prendre en charge un large éventail de fonctionnalités utilisées dans Direct3D. Direct2D utilise uniquement un sous-ensemble de ces fonctionnalités. Par conséquent, lorsque vous créez des images DDS à utiliser avec Direct2D, vous devez garder à l’esprit les restrictions suivantes :

-   Seules les valeurs [**de \_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) suivantes sont autorisées :
    -   DXGI \_ format \_ BC1 \_ UNORM
    -   DXGI \_ format \_ BC2 \_ UNORM
    -   DXGI \_ format \_ BC3 \_ UNORM
-   Les données alpha prémultipliées doivent être utilisées. Cela comprend les fichiers DDS hérités utilisant des formats qui définissent explicitement les valeurs alpha prémultipliées (DXT1, DXT2, DXT4), ainsi que les fichiers DDS qui utilisent la \_ structure facilement d’en-tête DDS \_ avec les \_ \_ \_ \_ \_ \_ valeurs prémultipliées en mode Alpha DDS et DDS en mode Alpha.
-   Les dimensions X et Y doivent être des multiples de 4 pixels.
-   Les textures de volume, les cubemaps, les des mipmaps ou les tableaux de texture ne sont pas autorisés. Vous devez uniquement utiliser des images source à image unique.

### <a name="generating-block-compressed-assets"></a>Génération de ressources en bloc compressées

Il existe un large éventail d’outils de création de DDS disponibles pour créer ou convertir des fichiers DDS compressés par blocs. Remarque tous les outils ne prennent pas en charge la configuration requise pour l’utilisation de fichiers DDS avec Direct2D, comme détaillé dans la section précédente.

à partir de Visual Studio 2013, vous pouvez avoir des Visual Studio convertir des ressources visuelles existantes, telles que JPEG et PNG, au format compressé de bloc DDS approprié comme partie automatique de votre processus de génération. Pour ce faire, utilisez l’étape de génération personnalisée de la tâche de contenu d’image.

Pour plus d’informations sur la configuration de ce pour votre projet, consultez : [Comment : exporter une texture pour une utilisation avec des applications Direct2D ou Direct2D](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120)).

### <a name="direct2d-apis"></a>API Direct2D

Direct2D est mis à jour dans Windows 8.1 pour prendre en charge les formats de pixel suivants :

-   DXGI \_ format \_ BC1 \_ UNORM
-   DXGI \_ format \_ BC2 \_ UNORM
-   DXGI \_ format \_ BC3 \_ UNORM

Pour les formats précédents, vous devez utiliser l’alpha prémultiplié. En outre, ces formats ne sont valides que pour une utilisation en tant que source, et non comme cible. Par exemple, cela signifie que vous pouvez créer un bitmap Direct2D à l’aide de BC1, mais pas d’un contexte de périphérique.

les méthodes suivantes sont mises à jour dans Windows 8.1 pour prendre en charge les formats BC :

-   [**ID2D1DeviceContext :: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext :: CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext :: CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget :: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget :: CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1::GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Notez que [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) prend [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) en tant qu’interface ; toutefois, dans Windows 8.1 WIC ne prend pas en charge l’obtention de données de bloc compressées à partir de **IWICBitmapSource**, et il n’existe aucun format de pixel WIC correspondant au \_ format DXGI \_ BC1 \_ UNORM, etc. Au lieu de cela, **CreateBitmapFromWicBitmap** détermine si le **IWICBITMAPSOURCE** est un DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) valide et charge directement les données compressées du bloc. Vous pouvez soit spécifier explicitement le format de pixel dans le struct [**d2d1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) , soit autoriser Direct2D à déterminer automatiquement le format correct.

### <a name="windows-imaging-component-apis"></a>Windows API du composant de création d’images

le composant WIC (Windows Imaging Component) ajoute un nouveau codec DDS dans Windows 8.1. En outre, il ajoute de nouvelles interfaces qui prennent en charge l’accès aux données spécifiques à DDS, y compris les données de pixels compressées de bloc :

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Bloquer les formats de pixel WIC compressés

Il n’existe aucun nouveau format de pixel compressé de bloc WIC dans Windows 8.1. Au lieu de cela, si vous obtenez un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) à partir du décodeur DDS et appelez [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels), vous recevrez des pixels non compressés standard tels que WICPixelFormat32bppPBGRA. Vous pouvez utiliser [**IWICDdsFrameDecode :: CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) pour obtenir les données compressées de bloc brutes sous la forme d’une mémoire tampon à partir d’un fichier DDS.

### <a name="multi-frame-dds-access"></a>Accès DDS multi-Frame

Le format de fichier DDS permet de stocker plusieurs images associées dans un seul fichier. Par exemple, un fichier DDS peut contenir un carte cubique, une texture de volume ou un tableau de textures, qui peuvent tous être mipmapped. Dans Direct3D, ces différentes images sont exposées en tant que sous-ressources. Dans WIC, plusieurs images sont exposées en tant que frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) et [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).

WIC prend uniquement en charge la notion d’un tableau unidimensionnel de frames, tandis que DDS prend en charge trois dimensions indépendantes (même si seulement deux peuvent être utilisées dans un fichier). WIC fournit des méthodes pratiques pour faciliter le mappage entre une sous-ressource DDS et une trame WIC. Pour le décodage, [**IWICDdsDecoder :: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) vous permet de spécifier l’index de tableau, le niveau MIP et l’index de tranche de la sous-ressource, puis renvoie le frame WIC correct.

Pour l’encodage, [**IWICDdsEncoder :: CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) calcule l’index de tableau résultant, le niveau MIP et l’index de découpage lorsque vous créez un nouveau Frame. Vous devez d’abord appeler [**IWICDdsEncoder :: SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) pour définir les paramètres de fichier spécifiques au DDS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide pratique pour exporter une texture pour l’utiliser avec des applications Javascript ou Direct2D](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Référence pour DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Compression de bloc](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 