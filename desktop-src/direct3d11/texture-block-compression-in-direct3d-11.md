---
title: Compression de bloc de texture dans Direct3D 11
description: La prise en charge de la compression par bloc (BC) des textures a été étendue dans Direct3D 11 pour inclure les algorithmes BC6H et BC7.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f80a22c97c8a706a3825abfb4ac2b5133c1a9beb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101728"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Compression de bloc de texture dans Direct3D 11

La prise en charge de la compression par bloc (BC) des textures a été étendue dans Direct3D 11 pour inclure les algorithmes BC6H et BC7. BC6H prend en charge les données sources de plage haute dynamique, et BC7 fournit une compression de qualité supérieure à la moyenne avec moins d’artefacts pour les données sources RGB standard.

Pour plus d’informations sur la prise en charge des algorithmes de compression de bloc avant Direct3D 11, y compris la prise en charge des BC1 via les formats BC5, consultez [compression par bloc (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

**Remarque à propos des formats de fichiers :** Les formats de compression de texture BC6H et BC7 utilisent le format de fichier DDS pour stocker les données de texture compressées. Pour plus d’informations, consultez le [Guide de programmation de DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) pour plus d’informations.

## <a name="block-compression-formats-supported-in-direct3d-11"></a>Formats de compression de bloc pris en charge dans Direct3D 11



| Données sources                                  | Résolution de compression de données minimale requise                              | Format recommandé | Niveau de fonctionnalité minimal pris en charge |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Couleur à trois canaux avec canal alpha       | Trois canaux de couleur (5 bits : 6 bits : 5 bits), avec 0 ou 1 bit (s) d’alpha  | BC1                | Direct3D 9,1                    |
| Couleur à trois canaux avec canal alpha       | Trois canaux de couleur (5 bits : 6 bits : 5 bits), avec 4 bits d’alpha         | BC2                | Direct3D 9,1                    |
| Couleur à trois canaux avec canal alpha       | Trois canaux de couleur (5 bits : 6 bits : 5 bits) avec 8 bits d’alpha          | BC3                | Direct3D 9,1                    |
| Couleur à un canal                            | Un canal de couleur (8 bits)                                                | TEXTURES BC4                | Direct3D 10                     |
| Couleur à deux canaux                            | Deux canaux de couleur (8 bits : 8 bits)                                        | BC5                | Direct3D 10                     |
| Couleur de plage dynamique élevée (HDR) à trois canaux | Trois canaux de couleur (16 bits : 16 bits : 16 bits) dans la « moitié » virgule flottante\* | BC6H               | Direct3D 11                     |
| Couleur à trois canaux, canal alpha facultatif  | Trois canaux de couleur (4 à 7 bits par canal) avec 0 à 8 bits d’alpha  | BC7                | Direct3D 11                     |



 

\*La « moitié » virgule flottante est une valeur de 16 bits qui se compose d’un bit de signe facultatif, d’un exposant biaisé à 5 bits et d’une mantisse 10 ou 11 bits.

## <a name="bc1-bc2-and-b3-formats"></a>Formats BC1, BC2 et B3

Les formats BC1, BC2 et BC3 sont équivalents aux formats de compression de texture de DXTn Direct3D 9 et sont identiques aux formats Direct3D 10 BC1, BC2 et BC3 correspondants. La prise en charge de ces trois formats est requise par tous les niveaux de fonctionnalité ( \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 1, \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 2, \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 3, niveau de \_ fonctionnalité D3D \_ \_ 10 0, niveau de \_ \_ fonctionnalité D3D \_ \_ 10 \_ 1 et \_ niveau de fonctionnalité D3D \_ \_ 11 \_ 0).



| Format de compression de bloc | Format DXGI                                                                           | Format équivalent Direct3D 9                               | Octets par bloc de pixels 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI \_ format \_ BC1 \_ UNORM, DXGI \_ format \_ BC1 \_ UNORM \_ sRGB, DXGI \_ format \_ BC1 non \_ typé | D3DFMT \_ DXT1, FourCC = "DXT1"                                | 8                         |
| BC2                      | DXGI \_ format \_ BC2 \_ UNORM, DXGI \_ format \_ BC2 \_ UNORM \_ sRGB, DXGI \_ format \_ BC2 non \_ typé | D3DFMT \_ DXT2 \* , FourCC = "DXT2", D3DFMT \_ DXT3, FourCC = "DXT3" | 16                        |
| BC3                      | DXGI \_ format \_ BC3 \_ UNORM, DXGI \_ format \_ BC3 \_ UNORM \_ sRGB, DXGI \_ format \_ BC3 non \_ typé | D3DFMT \_ DXT4 \* , FourCC = "DXT4", D3DFMT \_ DXT5, FourCC = "DXT5" | 16                        |



 

\*Ces schémas de compression (DXT2 et DXT4) ne font aucune distinction entre les formats alpha prémultipliés Direct3D 9 et les formats alpha standard. Cette distinction doit être gérée par les nuanceurs programmables au moment du rendu.

## <a name="bc4-and-bc5-formats"></a>Formats textures BC4 et BC5



| Format de compression de bloc | Format DXGI                                                                     | Format équivalent Direct3D 9 | Octets par bloc de pixels 4x4 |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| TEXTURES BC4                      | DXGI \_ format \_ textures BC4 \_ UNORM, DXGI \_ format \_ textures BC4 \_ ronfler, DXGI \_ format \_ textures BC4 non \_ typé | FourCC = "ATI1"                | 8                         |
| BC5                      | DXGI \_ format \_ BC5 \_ UNORM, DXGI \_ format \_ BC5 \_ ronfler, DXGI \_ format \_ BC5 non \_ typé | FourCC = "ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>Format BC6H

Pour obtenir des informations plus détaillées sur ce format, consultez la documentation de [format BC6H](bc6h-format.md) .



| Format de compression de bloc | Format DXGI                                                                      | Format équivalent Direct3D 9 | Octets par bloc de pixels 4x4 |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | DXGI \_ format \_ BC6H \_ UF16, DXGI \_ format \_ BC6H \_ SF16, DXGI \_ format \_ BC6H non \_ typé | N/A                          | 16                        |



 

Le format BC6H peut sélectionner différents modes d’encodage pour chaque bloc de pixels 4x4. Un total de 14 modes d’encodage différents sont disponibles, chacun avec des compromis légèrement différents dans la qualité visuelle résultante de la texture affichée. Le choix des modes permet de décoder rapidement le matériel avec le niveau de qualité sélectionné ou adapté en fonction du contenu source, mais il augmente également considérablement la complexité de l’espace de recherche.

## <a name="bc7-format"></a>Format BC7

Pour obtenir des informations plus détaillées sur ce format, consultez la documentation de [format Bc7](bc7-format.md) .



| Format de compression de bloc | Format DXGI                                                                           | Format équivalent Direct3D 9 | Octets par bloc de pixels 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | DXGI \_ format \_ Bc7 \_ UNORM, DXGI \_ format \_ Bc7 \_ UNORM \_ sRGB, DXGI \_ format \_ Bc7 non \_ typé | N/A                          | 16                        |



 

Le format BC7 peut sélectionner différents modes d’encodage pour chaque bloc de pixels 4x4. Un total de 8 modes d’encodage différents sont disponibles, chacun avec des compromis légèrement différents dans la qualité visuelle résultante de la texture affichée. Le choix des modes permet de décoder rapidement le matériel avec le niveau de qualité sélectionné ou adapté en fonction du contenu source, mais il augmente également considérablement la complexité de l’espace de recherche.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                 | Description                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Format BC6H](bc6h-format.md)<br/>                             | Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.<br/> |
| [Format BC7](bc7-format.md)<br/>                               | Le format BC7 est un format de compression de texture utilisé pour la compression de haute qualité des données RVB et RVBA.<br/>                    |
| [Référence du mode de format BC7](bc7-format-mode-reference.md)<br/> | Cette documentation contient la liste des 8 modes de blocage et des allocations de bits pour les blocs de format de compression de texture BC7.<br/>    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compression par bloc (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Textures](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

