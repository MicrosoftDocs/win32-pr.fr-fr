---
title: Sous-types de média compressés
description: Sous-types de média compressés
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows Media Format SDK, types de médias
- ASF (Advanced Systems Format), types de média
- ASF (format des systèmes avancés), types de média
- Windows Media Format SDK, sous-types de média compressés
- ASF (Advanced Systems Format), sous-types de média compressés
- ASF (format des systèmes avancés), sous-types de média compressés
- types de média, sous-types de média compressés
- sous-types de média compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f231c9c8ff666c11d3fb3bf101dc3b43c1cd2ff90ca3a28ca1af0113fe8fccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548089"
---
# <a name="compressed-media-subtypes"></a>Sous-types de média compressés

Le tableau suivant répertorie les sous-types de médias compressés. Ces types sont utilisés pour identifier des flux compressés dans un fichier. Quand vous configurez un flux vidéo ou audio, vous utilisez généralement ces types.



| Sous-type de média compressé          | Description                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Fichier audio encodé avec le codec Sipro Labs ACELP. Ce fichier audio est généralement des données vocales. (N’est plus pris en charge pour l’encodage.)                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ mp43              | Vidéo encodée par le codec Microsoft MPEG 4 version 3. ce codec n’est plus pris en charge par le kit de développement logiciel (SDK) de Format multimédia Windows. si ce codec est déjà installé sur un ordinateur, l’installation du kit de développement logiciel (SDK) Windows Media Format ou du package de redistribution sur un ordinateur ne supprimera pas ce codec. |
| WMMEDIASUBTYPE \_ fichiers MP4 à              | Vidéo encodée à l’aide du codec ISO MPEG 4 version 1.                                                                                                                                                                                                                                         |
| \_Vidéo WMMEDIASUBTYPE MPEG2 \_      | Les spécifications vidéo encodées en MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | vidéo encodée avec le codec d’écran de média Windows version 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | vidéo encodée avec le codec d’écran Windows Media Video 9.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | vidéo encodée avec le codec d’Image Windows Media Video 9 pour transformer les bitmaps et les données de déformation en un flux vidéo.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | vidéo encodée avec le codec d’Image Windows Media Video 9 v2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | encodage Audio avec le codec Windows Media Audio 9 Lossless ou le codec Windows Media Audio 9,1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | encodage Audio avec le codec Windows Media Audio version 2. Cette valeur est identique à WMMEDIASUBTYPE \_ WMAudioV7 et WMMEDIASUBTYPE \_ WMAudioV8, car les flux binaires pour ces versions de codec sont compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | encodage Audio avec le codec Windows Media Audio version 7. Cette valeur est identique à WMMEDIASUBTYPE \_ WMAudioV2 et WMMEDIASUBTYPE \_ WMAudioV8, car les flux binaires pour ces versions de codec sont compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | fichier Audio encodé avec le codec Windows Media Audio 8, le codec Windows Media Audio 9 ou le codec Windows Media Audio 9,1. Cette valeur est identique à WMMEDIASUBTYPE \_ WMAudioV2 et WMMEDIASUBTYPE \_ WMAudioV7, car les flux binaires pour ces versions de codec sont compatibles.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | fichier Audio encodé avec le codec Windows Media Audio 9 Professional ou le codec Windows Media Audio 9,1 Professional.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Vidéo encodée avec le codec ISO MPEG4 v 1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | encodage Audio avec le codec vocal Windows Media Audio 9.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | vidéo encodée à l’aide du codec Windows Media Video version 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | encodage vidéo à l’aide du codec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | encodage vidéo à l’aide du codec Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | fichier vidéo encodé à l’aide de la version du codec de profil avancé Windows Media Video 9 fourni avec le kit de développement logiciel (SDK) Windows Media Format 9 Series.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | fichier vidéo encodé à l’aide de la version du codec de profil avancé Windows Media Video 9 fourni avec le kit de développement logiciel (SDK) Windows Media Format 11. Ce sous-type identifie un flux binaire conforme à la norme SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs de type de média**](media-type-identifiers.md)
</dt> <dt>

[**Types de médias**](media-types.md)
</dt> <dt>

[**Sous-types de médias non compressés**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




