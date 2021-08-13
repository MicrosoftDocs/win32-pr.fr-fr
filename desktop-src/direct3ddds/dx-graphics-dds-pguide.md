---
title: Guide de programmation pour DDS
description: Direct3D implémente le format de fichier DDS pour le stockage des textures non compressées ou compressées (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc1f8b9b84c2dc1f9236c79c320ae75848834ef2183db55b189f6b9d340d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796719"
---
# <a name="programming-guide-for-dds"></a>Guide de programmation pour DDS

Direct3D implémente le format de fichier DDS pour le stockage des textures non compressées ou compressées (DXTn). Le format de fichier implémente plusieurs types légèrement différents conçus pour le stockage de différents types de données, et prend en charge les textures à couche unique, les textures avec des mipmaps, les cartes de cube, les cartes de volume et les tableaux de texture (dans Direct3D 10/11). Cette section décrit la disposition d’un fichier DDS.

Pour obtenir de l’aide sur la création d’une texture dans Direct3D 11, consultez [Comment : créer une texture](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create). Pour obtenir de l’aide dans Direct3D 9, consultez [prise en charge de la texture dans D3DX (Direct3D 9)](/windows/desktop/direct3d9/texture-support-in-d3dx).

-   [Disposition du fichier DDS](#dds-file-layout)
-   [Variantes DDS](#dds-variants)
-   [Utilisation de tableaux de texture dans Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Formats de ressource de fichier DDS courants et contenu d’en-tête associé](#common-dds-file-resource-formats-and-associated-header-content)
-   [Rubriques connexes](#related-topics)

## <a name="dds-file-layout"></a>Disposition du fichier DDS

Un fichier DDS est un fichier binaire qui contient les informations suivantes :

-   Un DWORD (nombre magique) contenant la valeur codée des quatre caractères "DDS " (0x20534444).

-   Une description des données du fichier.

    Les données sont décrites avec une description d’en-tête à l’aide de l' [**\_ en-tête DDS**](dds-header.md); le format de pixel est défini à l’aide de [**DDS \_ PIXELFORMAT**](dds-pixelformat.md). Notez que l' **\_ en-tête DDS** et les structures **DDS \_ PIXELFORMAT** remplacent les structures DDSURFACEDESC2, DDSCAPS2 et DDPIXELFORMAT DirectDraw 7 déconseillées. **DDS \_ L’en-tête** est l’équivalent binaire de DDSURFACEDESC2 et DDSCAPS2. **DDS \_ PIXELFORMAT** est l’équivalent binaire de DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Si le DDS \_ PIXELFORMAT dwFlags est défini sur DDPF \_ FourCC et que dwFourCC est défini sur « facilement », une structure de [**\_ \_ DXT10 d’en-tête DDS**](dds-header-dxt10.md) supplémentaire sera présente pour prendre en charge les tableaux de texture ou les formats de dxgi qui ne peuvent pas être exprimés sous forme de format de pixel RVB comme les formats à virgule flottante, les formats sRVB, etc. Lorsque la structure DXT10 de l' **\_ en-tête \_ DDS** est présente, la description de la totalité des données se présente comme suit.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   Pointeur vers un tableau d’octets qui contient les principales données de surface.
    ```
    BYTE bdata[]
    ```

    

-   Pointeur vers un tableau d’octets qui contient les surfaces restantes telles que niveaux de mipmap, faces dans un plan de cube, profondeurs dans une texture de volume. Suivez ces liens pour plus d’informations sur le schéma du fichier DDS pour une [texture](dds-file-layout-for-textures.md), un [mappage de cube](dds-file-layout-for-cubic-environment-maps.md) ou une [texture de volume](dds-file-layout-for-volume-textures.md).

    ```
    BYTE bdata2[]
    ```

    

Pour une prise en charge du matériel large, nous vous recommandons d’utiliser le [**\_ format dxgi \_ R8G8B8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format \_ R8G8B8A8 \_ ronfler**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format B8G8R8A8 \_ \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), DXGI format R16G16 [**\_ \_ \_ ronfler**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi format R8G8 \_ \_ \_ ronfler**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format \_ R8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)BC1 UNORM, DXGI format BC1 UNORM [**\_ \_ \_ \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi format BC2 \_ \_ \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi \_ format BC2 UNORM \_ \_ \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**dxgi format BC3 \_ \_ \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)ou [**dxgi format BC3 UNORM \_ \_ \_ \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format.

Pour plus d’informations sur les formats de texture compressés, consultez [compression de bloc de texture dans Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) et [compression de bloc (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

La bibliothèque D3DX (par exemple, D3DX11. lib) et d’autres bibliothèques similaires fournissent de manière non fiable ou incohérente la valeur de pas dans le membre **dwPitchOrLinearSize** de la structure d' [**\_ en-tête DDS**](dds-header.md) . Par conséquent, lorsque vous lisez et écrivez dans des fichiers DDS, nous vous recommandons de calculer la tonalité de l’une des manières suivantes pour les formats indiqués :

-   Pour les formats compressés par blocs, calculez le pas comme suit :

    taille de bloc Max (1, ((largeur + 3)/4)) \*

    La taille du bloc est de 8 octets pour les formats DXT1, BC1 et textures BC4, et de 16 octets pour les autres formats compressés par blocs.

-   Pour \_ les formats R8G8 B8G8, G8R8 \_ G8B8, Legacy UYVY-compressés et YUY2 hérités, calculez l’espacement comme suit :

    ((largeur + 1)  >> 1) \* 4

-   Pour les autres formats, calculez l’espacement comme suit :

    (largeur \* en bits par pixel + 7)/8

    Vous divisez par 8 pour l’alignement d’octets.

> [!Note]  
> La valeur de l’espacement que vous calculez n’est pas toujours égale au pas que le Runtime fournit, qui est alignée sur DWORD dans certaines situations et alignée sur l’octet dans d’autres situations. Par conséquent, nous vous recommandons de copier une ligne de numérisation à un moment plutôt que d’essayer de copier l’image entière en une seule copie.

 

## <a name="dds-variants"></a>Variantes DDS

Il existe de nombreux outils qui créent et consomment des fichiers DDS, mais ils peuvent varier en fonction des détails de ce dont ils ont besoin dans l’en-tête. Les enregistreurs doivent remplir les en-têtes aussi complètement que possible et les lecteurs doivent vérifier les valeurs minimales pour obtenir une compatibilité maximale. Pour valider un fichier DDS, un lecteur doit s’assurer que le fichier comporte au moins 128 octets pour s’adapter à la valeur magique et à l’en-tête de base, que la valeur Magic est 0x20534444 (« DDS »), que la taille de l' \_ en-tête DDS est égale à 124 et que la \_ taille d’en-tête de l’en-tête est 32. Si le DDS \_ PIXELFORMAT dwFlags est défini sur DDPF \_ FourCC et que dwFourCC est défini sur « facilement », la taille totale du fichier doit être d’au moins 148 octets.

Des variantes courantes sont utilisées lorsque le format de pixel est défini sur un code DDPF \_ FourCC où dwFourCC est défini sur une valeur d’énumération de format D3DFORMAT ou dxgi \_ . Il n’existe aucun moyen de savoir si une valeur d’énumération est un format D3DFORMAT ou DXGI. \_ il est donc vivement recommandé d’utiliser à la place l’en-tête de l’extension « facilement » et du \_ DXT10 d’en-tête DDS \_ pour stocker le dxgiFormat lorsque l’PIXELFORMAT de base \_ ne peut pas exprimer le format.

L’PIXELFORMAT standard \_ de DDS doit être préférable à la compatibilité maximale pour stocker les données RVB non compressées et les données DXT1-5, car tous les outils DDS ne prennent pas en charge l’extension facilement.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Utilisation de tableaux de texture dans Direct3D 10/11

Les nouvelles structures DDS ([**\_ en-tête DDS**](dds-header.md) et [**\_ \_ DXT10 en-tête DDS**](dds-header-dxt10.md)) dans Direct3D 10/11 étendent le format de fichier DDS pour prendre en charge un tableau de textures, qui est un nouveau type de ressource dans Direct3D 10/11. Voici un exemple de code qui montre comment accéder aux différents niveaux de mipmap dans un tableau de textures, à l’aide des nouveaux en-têtes.


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Formats de ressource de fichier DDS courants et contenu d’en-tête associé



| Format de ressource                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| DXGI \_ format \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | DDS \_ RVBA      | 32            | vert       | 0xff00     | 0xff0000   | 0xff000000 |
| DXGI \_ format \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RVBA      | 32            | 0xffff     | 0xffff0000 |            |            |
| \*\*<br/> DXGI \_ format \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | DDS \_ RVBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| DXGI \_ format \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RVB       | 32            | 0xffff     | 0xffff0000 |            |            |
| DXGI \_ format \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | DDS \_ RVBA      | 16            | 0x7c00     | 0x3e0      | 0x1F       | 0x8000     |
| DXGI \_ format \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RVB       | 16            | 0xf800     | 0x7e0      | 0x1F       |            |
| DXGI \_ a8 \_ UNORM<br/> D3DFMT \_ a8<br/>                                           | DDS \_ alpha     | 8             |            |            |            | vert       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | DDS \_ RVBA      | 32            | 0xff0000   | 0xff00     | vert       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RVB       | 32            | 0xff0000   | 0xff00     | vert       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RVB       | 32            | vert       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | DDS \_ RVBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RVB       | 24            | 0xff0000   | 0xff00     | vert       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RVB       | 16            | 0x7c00     | 0x3e0      | 0x1F       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | DDS \_ RVBA      | 16            | 0xf00      | 0xf0       | 0xF        | 0xF000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RVB       | 16            | 0xf00      | 0xf0       | 0xF        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | DDS \_ RVBA      | 16            | 0xe0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | LUMINANCE de DDS \_ | 16            | vert       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | LUMINANCE de DDS \_ | 16            | 0xffff     |            |            |            |
| D3DFMT \_ N8<br/>                                                                      | LUMINANCE de DDS \_ | 8             | vert       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | LUMINANCE de DDS \_ | 8             | 0xF        |            |            | 0xf0       |



 



| Format de ressource                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| DXGI \_ format \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | FourCC de DDS \_ | DXT1   |
| DXGI \_ format \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | FourCC de DDS \_ | "DXT3"   |
| DXGI \_ format \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | FourCC de DDS \_ | DXT5   |
| \*<br/> DXGI \_ format \_ textures BC4 \_ UNORM<br/>                                           | FourCC de DDS \_ | "BC4U"   |
| \*<br/> \_Format dxgi \_ textures BC4 \_ ronfler<br/>                                           | FourCC de DDS \_ | "BC4S"   |
| \*<br/> DXGI \_ format \_ BC5 \_ UNORM<br/>                                           | FourCC de DDS \_ | "ATI2"   |
| \*<br/> \_Format dxgi \_ BC5 \_ ronfler<br/>                                           | FourCC de DDS \_ | "BC5S"   |
| DXGI \_ format \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | FourCC de DDS \_ | "RGBG"   |
| DXGI \_ format \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | FourCC de DDS \_ | "GRGB"   |
| \*<br/> DXGI \_ format \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | FourCC de DDS \_ | 36       |
| \*<br/> \_Format dxgi \_ R16G16B16A16 \_ ronfler<br/> D3DFMT \_ Q16W16V16U16<br/>  | FourCC de DDS \_ | 110      |
| \*<br/> DXGI \_ format \_ R16 \_ float<br/> D3DFMT \_ R16F<br/>                   | FourCC de DDS \_ | 111      |
| \*<br/> DXGI \_ format \_ R16G16 \_ float<br/> D3DFMT \_ G16R16F<br/>             | FourCC de DDS \_ | 112      |
| \*<br/> DXGI \_ format \_ R16G16B16A16 \_ float<br/> D3DFMT \_ A16B16G16R16F<br/> | FourCC de DDS \_ | 113      |
| \*<br/> DXGI \_ format \_ R32 \_ float<br/> D3DFMT \_ R32F<br/>                   | FourCC de DDS \_ | 114      |
| \*<br/> DXGI \_ format \_ R32G32 \_ float<br/> D3DFMT \_ G32R32F<br/>             | FourCC de DDS \_ | 115      |
| \*<br/> DXGI \_ format \_ R32G32B32A32 \_ float<br/> D3DFMT \_ A32B32G32R32F<br/> | FourCC de DDS \_ | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | FourCC de DDS \_ | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | FourCC de DDS \_ | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | FourCC de DDS \_ | UYVY   |
| D3DFMT \_ YUY2<br/>                                                                     | FourCC de DDS \_ | YUY2   |
| D3DFMT \_ CxV8U8<br/>                                                                   | FourCC de DDS \_ | 117      |
| Tout format DXGI                                                                             | FourCC de DDS \_ | FACILEMENT   |



 

\* = Un lecteur DDS robuste doit être en mesure de gérer ces codes de format hérités. Toutefois, un tel lecteur DDS doit préférer utiliser l’extension d’en-tête « facilement » lors de l’écriture de ces codes de format pour éviter toute ambiguïté.

\*\* = En raison de problèmes de longue durée dans les implémentations courantes des lecteurs et Writers DDS, la méthode la plus fiable pour écrire des données de type 10:10:10:2 consiste à utiliser l’extension d’en-tête « facilement » avec le code de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) « 24 » (autrement dit, le \_ format dxgi \_ R10G10B10A2 \_ valeur UNORM). Les \_ données de D3DFMT A2R10G10B10 doivent être converties en données de type 10:10:10:2 avant d’être écrites sous la forme d’un fichier de format dxgi \_ \_ R10G10B10A2 \_ UNORM format DDS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DDS](dx-graphics-dds.md)
</dt> </dl>

 

