---
description: Définit les différents types de formats de surface.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762109"
---
# <a name="d3dformat"></a>D3DFORMAT

Définit les différents types de formats de surface.

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a>Notes

Il existe plusieurs types de formats :

-   [Formats d’affichage ou de mémoire tampon](#backbuffer-or-display-formats)
-   [Formats de mémoire tampon](#buffer-formats)
-   [Formats de texture compressés DXTn](#dxtn-compressed-texture-formats)
-   [Formats à virgule flottante](#floating-point-formats)
-   [Formats FOURCC](#fourcc-formats)
-   [Formats IEEE](#ieee-formats)
-   [Formats mixtes](#mixed-formats)
-   [Formats signés](#signed-formats)
-   [Formats non signés](#unsigned-formats)
-   [Autres](#other)

Tous les formats sont répertoriés de gauche à droite, le bit le plus significatif au bit le moins significatif. Par exemple, **D3DFORMAT \_ ARGB** est classé du canal de bits A (alpha) le plus significatif au canal de bits le moins significatif B (bleu). Lors du parcours des données de surface, les données sont stockées en mémoire à partir du bit le moins significatif au bit le plus significatif, ce qui signifie que l’ordre des canaux en mémoire est du bit le moins significatif (bleu) au bit le plus significatif (alpha).

La valeur par défaut pour les formats qui contiennent des canaux non définis (G16R16, A8, etc.) est 1. La seule exception est le format A8, qui est initialisé à 000 pour les trois canaux de couleur.

L’ordre des bits est tout d’abord l’octet le plus significatif, donc D3DFMT \_ A8L8 indique que l’octet de poids fort de ce format de 2 octets est alpha. **D3DFMT \_ D16** indique une valeur entière de 16 bits et une surface verrouillable par l’application.

Les formats de pixel ont été choisis pour activer l’expression des formats d’extension définis par le fournisseur de matériel, ainsi que pour inclure la méthode FOURCC bien établie. L’ensemble de formats compris par le runtime Direct3D est défini par D3DFORMAT.

Notez que les formats sont fournis par des fournisseurs de matériel indépendants (IHV) et que de nombreux codes FOURCC ne sont pas répertoriés. Les formats de cette énumération sont uniques dans le sens où ils sont approuvés par le runtime, ce qui signifie que le rastériseur de référence fonctionnera sur tous ces types. Les formats fournis par IHV seront pris en charge par chaque IHV carte par carte.

### <a name="backbuffer-or-display-formats"></a>Formats d’affichage ou de mémoire tampon

Ces formats sont les seuls formats valides pour une mémoire tampon d’arrière-plan ou un affichage.



| Format      | Mémoire tampon d’arrière-plan | Afficher                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (mode plein écran uniquement) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Formats de mémoire tampon

Les mémoires tampons de profondeur, de stencil, de vertex et d’index ont chacune des formats uniques.



| Indicateurs de mémoire tampon               | Valeur | Format                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ verrouillable**  | 70    | profondeur de bits de la mémoire tampon z 16 bits.                                                                                                                    |
| **D3DFMT \_ d32**            | 71    | profondeur en bits de la mémoire tampon z 32 bits.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | profondeur de bits de la mémoire tampon z 16 bits où 15 bits sont réservés pour le canal de profondeur et 1 bit est réservé pour le canal du stencil.                     |
| **D3DFMT \_ D24S8**          | 75    | profondeur en bits de la mémoire tampon z 32 bits utilisant 24 bits pour le canal de profondeur et 8 bits pour le canal du stencil.                                             |
| **D3DFMT \_ D24X8**          | 77    | profondeur en bits de la mémoire tampon z 32 bits utilisant 24 bits pour le canal de profondeur.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | profondeur en bits de la mémoire tampon z 32 bits utilisant 24 bits pour le canal de profondeur et 4 bits pour le canal du stencil.                                             |
| **D3DFMT \_ D32F \_ verrouillable** | 82    | Format verrouillable dans lequel la valeur de profondeur est représentée sous la forme d’un nombre à virgule flottante IEEE Standard.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Format non verrouillable qui contient 24 bits de profondeur (dans un format à virgule flottante de 24 bits-20E4) et 8 bits de stencil.                        |
| **D3DFMT \_ d32 \_ verrouillable**  | 84    | Mémoire tampon de profondeur 32 bits verrouillable. **Différences entre Direct3D 9 et Direct3D 9Ex :** Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/>  |
| **D3DFMT \_ S8 \_ verrouillable**   | 85 %    | Mémoire tampon de stencil de 8 bits verrouillable. **Différences entre Direct3D 9 et Direct3D 9Ex :** Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/> |
| **D3DFMT \_ D16**            | 80    | profondeur de bits de la mémoire tampon z 16 bits.                                                                                                                    |
| **D3DFMT \_ VERTEXDATA**     | 100   | Décrit une surface de mémoire tampon de vertex.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | profondeur de bit de la mémoire tampon d’index 16 bits.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | profondeur de bit de la mémoire tampon d’index 32 bits.                                                                                                                |



 

Tous les formats de stencil de profondeur, à l’exception de D3DFMT \_ D16 \_ verrouillables, indiquent un ordre de bit particulier par pixel et le pilote est autorisé à consommer plus que le nombre indiqué de canaux par profondeur (mais pas de canal de stencil).

### <a name="dxtn-compressed-texture-formats"></a>Formats de texture compressés DXTn

Ces indicateurs sont utilisés pour les textures compressées :



| Indicateurs de texture compressée DXTn | Valeur                          | Format                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | MAKEFOURCC ('D', 'X', 'T', ' 1 ') | Format de texture de compression DXT1 |
| **D3DFMT \_ DXT2**              | MAKEFOURCC ('D', 'X', 'T', ' 2 ') | Format de texture de compression DXT2 |
| **D3DFMT \_ DXT3**              | MAKEFOURCC ('D', 'X', 'T', ' 3 ') | Format de texture de compression DXT3 |
| **D3DFMT \_ DXT4**              | MAKEFOURCC ('D', 'X', 'T', ' 4 ') | Format de texture de compression DXT4 |
| **D3DFMT \_ DXT5**              | MAKEFOURCC ('D', 'X', 'T', ' 5 ') | Format de texture de compression DXT5 |



 

Le runtime ne permet pas à une application de créer une surface à l’aide d’un format DXTn, sauf si les dimensions de la surface sont des multiples de 4. Cela s’applique aux surfaces brutes hors écran, aux cibles de rendu, aux textures 2D, aux textures de cube et aux textures de volume.

### <a name="floating-point-formats"></a>Formats de Floating-Point

Ces indicateurs sont utilisés pour les formats de surface à virgule flottante. Ces formats 16 bits par canal sont également appelés formats s10e5.



| Indicateurs à virgule flottante      | Valeur | Format                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | format à virgule flottante 16 bits utilisant 16 bits pour le canal rouge.                                   |
| **D3DFMT \_ G16R16F**       | 112   | format float 32 bits utilisant 16 bits pour le canal rouge et 16 bits pour le canal vert. |
| **D3DFMT \_ A16B16G16R16F** | 113   | format float 64 bits utilisant 16 bits pour chaque canal (alpha, bleu, vert, rouge).        |



 

### <a name="fourcc-formats"></a>Formats FOURCC

Les données au format FOURCC sont des données compressées.

### <a name="makefourcc"></a>MAKEFOURCC

Une macro pour générer des codes à quatre caractères est la suivante :

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Voici les formats FOURCC définis :



| Indicateurs FOURCC              | Valeur                          | Format                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTI2 \_ ARGB8** | MAKEFOURCC (« M », « E », « T », « 1 »)    | Texture multiélément (non compressée)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC (« G », « R », « G », « B ») | Format RVB condensé 16 bits analogue à YUY2 (Y0U0, Y1V0, Y2U2, etc.). Elle nécessite une paire de pixels afin de représenter correctement la valeur de couleur. Le premier pixel de la paire contient 8 bits de vert (dans les 8 bits de poids fort) et 8 bits de couleur rouge (dans les 8 bits de poids faible). Le deuxième pixel contient 8 bits de couleur verte (dans les 8 bits de poids fort) et 8 bits de bleu (dans les 8 bits de poids faible). Ensemble, les deux pixels partagent les composants rouge et bleu, tandis que chacun a un composant vert unique (G0R0, G1B0, G2R2, etc.). L’échantillonneur de texture ne normalise pas les couleurs lors de la recherche dans un nuanceur de pixels ; ils restent dans la plage de 0.0 f à 255.0 f. Cela est vrai pour tous les modèles de nuanceur de pixels programmables. Pour le nuanceur de pixels de fonction fixe, le matériel doit se normaliser à la plage 0. f en 1. f et le traiter essentiellement comme la texture YUY2. Le matériel qui expose ce format doit avoir le membre PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) défini sur une valeur capable de gérer cette plage. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC (« R », « G », « B », « G ») | Format RVB condensé 16 bits analogue à UYVY (U0Y0, V0Y1, U2Y2, etc.). Elle nécessite une paire de pixels afin de représenter correctement la valeur de couleur. Le premier pixel de la paire contient 8 bits de vert (dans les 8 bits de poids faible) et 8 bits de couleur rouge (dans les 8 bits de poids fort). Le deuxième pixel contient 8 bits de couleur verte (dans les 8 bits de poids faible) et 8 bits de bleu (dans les 8 bits de poids fort). Ensemble, les deux pixels partagent les composants rouge et bleu, tandis que chacun a un composant vert unique (R0G0, B0G1, R2G2, etc.). L’échantillonneur de texture ne normalise pas les couleurs lors de la recherche dans un nuanceur de pixels ; ils restent dans la plage de 0.0 f à 255.0 f. Cela est vrai pour tous les modèles de nuanceur de pixels programmables. Pour le nuanceur de pixels de fonction fixe, le matériel doit se normaliser à la plage 0. f en 1. f et le traiter essentiellement comme la texture YUY2. Le matériel qui expose ce format doit avoir un membre PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) défini sur une valeur capable de gérer cette plage.     |
| **D3DFMT \_ UYVY**          | MAKEFOURCC (« U », « Y », « V », « Y ») | Format UYVY (conformité PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ YUY2**          | MAKEFOURCC (« Y », « U », « Y », « 2 ») | Format YUY2 (conformité PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>Formats IEEE

Ces indicateurs sont utilisés pour les formats de surface à virgule flottante. Ces formats 32 bits par canal sont également appelés formats s23e8.



| Indicateurs à virgule flottante      | Valeur | Format                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | format float 32 bits utilisant 32 bits pour le canal rouge.                                   |
| **D3DFMT \_ G32R32F**       | 115   | format float 64 bits utilisant 32 bits pour le canal rouge et 32 bits pour le canal vert. |
| **D3DFMT \_ A32B32G32R32F** | 116   | format float 128 bits utilisant 32 bits pour chaque canal (alpha, bleu, vert, rouge).       |



 

### <a name="mixed-formats"></a>Formats mixtes

Les données dans des formats mixtes peuvent contenir une combinaison de données non signées et de données signées.



| Indicateurs de format mixte      | Valeur | Format                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | relief 16 bits-format de carte avec luminance utilisant 6 bits pour la luminance et 5 bits pour v et vous. |
| **D3DFMT \_ X8L8V8U8**    | 62    | 32 bits-format de carte avec luminance à l’aide de 8 bits pour chaque canal.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | format de carte de choc 32 bits utilisant 2 bits pour Alpha et 10 bits chacun pour w, v et vous.                |



 

### <a name="signed-formats"></a>Formats signés

Les données d’un format signé peuvent être à la fois positives et négatives. Les formats signés utilisent des combinaisons de données (U), (V), (W) et (Q).



| Indicateurs de format signé      | Valeur | Format                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | relief 16 bits : format de carte avec 8 bits chacun pour vous et vos données v.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | 32 bits-format de carte avec 8 bits pour chaque canal.                                                     |
| **D3DFMT \_ V16U16**       | 64    | format de la carte de choc 32 bits utilisant 16 bits pour chaque canal.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | format de carte de choc 64 bits utilisant 16 bits pour chaque composant.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | format de compression normale 16 bits. L’échantillon de texture calcule le canal C à partir de : C = sqrt (1-U ²-V ²). |



 

### <a name="unsigned-formats"></a>Formats non signés

Les données dans un format non signé doivent être positives. Les formats non signés utilisent des combinaisons des données (R) Ed, (G) reen, (B) Lü, (A) lpha, (L) uminance et (P) Alette. Les données de palette sont également appelées données d’index de couleurs, car les données sont utilisées pour indexer une palette de couleurs.



| Indicateurs de format non signés             | Valeur | Format                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | format de pixel RVB 24 bits avec 8 bits par canal.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | format de pixel ARVB 32 bits avec alpha, à l’aide de 8 bits par canal.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | format de pixel RVB 32 bits, où 8 bits sont réservés pour chaque couleur.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | format de pixel RVB 16 bits avec 5 bits pour le rouge, 6 bits pour le vert et 5 bits pour le bleu.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | format de pixel de 16 bits, où 5 bits sont réservés pour chaque couleur.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | format de pixel de 16 bits, où 5 bits sont réservés pour chaque couleur et 1 bit est réservé pour alpha.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | format de pixel ARVB 16 bits avec 4 bits pour chaque canal.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | format de texture RGB 8 bits utilisant 3 bits pour le rouge, 3 bits pour le vert et 2 bits pour le bleu.                                                                                     |
| **D3DFMT \_ a8**                    | 28    | alpha 8 bits uniquement.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | format de texture ARVB 16 bits avec 8 bits pour alpha, 3 bits pour les rouge et vert et 2 bits pour le bleu.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | format de pixel RVB 16 bits utilisant 4 bits pour chaque couleur.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | format de pixel 32 bits utilisant 10 bits pour chaque couleur et 2 bits pour alpha.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | format de pixel ARVB 32 bits avec alpha, à l’aide de 8 bits par canal.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | format de pixel RVB 32 bits, où 8 bits sont réservés pour chaque couleur.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | format de pixel 32 bits utilisant 16 bits chacun pour le vert et le rouge.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | format de pixel 32 bits utilisant 10 bits chacun pour le rouge, le vert et le bleu, et 2 bits pour alpha.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | format de pixel 64 bits utilisant 16 bits pour chaque composant.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | couleurs 8 bits indexées avec 8 bits d’alpha.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | couleurs 8 bits indexées.                                                                                                                                                      |
| **D3DFMT \_ N8**                    | 50    | luminance 8 bits uniquement.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | luminance de 16 bits uniquement.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16 bits utilisant 8 bits chacun pour Alpha et luminance.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8 bits utilisant 4 bits chacun pour Alpha et luminance.                                                                                                                          |
| **D3DFMT \_ a1**                    | 118   | monochrome 1 bit. **Différences entre Direct3D 9 et Direct3D 9Ex :** Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR \_ biais** | 119   | 2,8-point fixe biaisé. **Différences entre Direct3D 9 et Direct3D 9Ex :** Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/>                                      |
| **D3DFMT \_ BINARYBUFFER**          | 199   | Format binaire indiquant que les données n’ont pas de type inhérent. **Différences entre Direct3D 9 et Direct3D 9Ex :** Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/> |



 

### <a name="other"></a>Autres

Cet indicateur est utilisé pour les formats non définis.



| Autres indicateurs         | Valeur | Format                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ inconnu** | 0     | Le format de surface est inconnu |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




