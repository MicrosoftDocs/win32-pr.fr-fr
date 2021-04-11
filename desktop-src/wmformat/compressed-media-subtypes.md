---
title: Sous-types de média compressés
description: Sous-types de média compressés
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows Media Format SDK, types de média
- ASF (Advanced Systems Format), types de média
- ASF (format des systèmes avancés), types de média
- Windows Media Format SDK, sous-types de média compressés
- ASF (Advanced Systems Format), sous-types de média compressés
- ASF (format des systèmes avancés), sous-types de média compressés
- types de média, sous-types de média compressés
- sous-types de média compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d92d192d04257f0375a618dda05aa97fd3f344b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100645"
---
# <a name="compressed-media-subtypes"></a>Sous-types de média compressés

Le tableau suivant répertorie les sous-types de médias compressés. Ces types sont utilisés pour identifier des flux compressés dans un fichier. Quand vous configurez un flux vidéo ou audio, vous utilisez généralement ces types.



| Sous-type de média compressé          | Description                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Fichier audio encodé avec le codec Sipro Labs ACELP. Ce fichier audio est généralement des données vocales. (N’est plus pris en charge pour l’encodage.)                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ mp43              | Vidéo encodée par le codec Microsoft MPEG 4 version 3. Ce codec n’est plus pris en charge par le kit de développement logiciel (SDK) du format Windows Media. Si ce codec est déjà installé sur un ordinateur, l’installation du kit de développement logiciel (SDK) Windows Media format ou du package de redistribution sur un ordinateur ne supprimera pas ce codec. |
| WMMEDIASUBTYPE \_ fichiers MP4 à              | Vidéo encodée à l’aide du codec ISO MPEG 4 version 1.                                                                                                                                                                                                                                         |
| \_Vidéo WMMEDIASUBTYPE MPEG2 \_      | Les spécifications vidéo encodées en MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Vidéo encodée avec le codec Windows Media Screen version 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Vidéo encodée avec le codec d’écran Windows Media Video 9.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Vidéo encodée avec le codec d’image Windows Media Video 9 pour transformer les bitmaps et les données de déformation en un flux vidéo.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Vidéo encodée avec le codec d’image Windows Media Video 9 v2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Encodage audio avec le codec Windows Media Audio 9 Lossless ou le codec Windows Media Audio 9,1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Encodage audio avec le codec Windows Media Audio version 2. Cette valeur est identique à WMMEDIASUBTYPE \_ WMAudioV7 et WMMEDIASUBTYPE \_ WMAudioV8, car les flux binaires pour ces versions de codec sont compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Encodage audio avec le codec Windows Media Audio version 7. Cette valeur est identique à WMMEDIASUBTYPE \_ WMAudioV2 et WMMEDIASUBTYPE \_ WMAudioV8, car les flux binaires pour ces versions de codec sont compatibles.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Fichier audio encodé avec le codec Windows Media Audio 8, le codec Windows Media Audio 9 ou le codec Windows Media Audio 9,1. Cette valeur est identique à WMMEDIASUBTYPE \_ WMAudioV2 et WMMEDIASUBTYPE \_ WMAudioV7, car les flux binaires pour ces versions de codec sont compatibles.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Fichier audio encodé avec le codec Windows Media Audio 9 Professional ou le codec Windows Media Audio Professional 9,1.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Vidéo encodée avec le codec ISO MPEG4 v 1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Encodage audio avec le codec vocal Windows Media Audio 9.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Vidéo encodée à l’aide du codec Windows Media Video version 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | Encodage vidéo à l’aide du codec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | Encodage vidéo à l’aide du codec Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Fichier vidéo encodé à l’aide de la version du codec de profil avancé Windows Media Video 9 fourni avec le kit de développement logiciel (SDK) Windows Media Format 9 Series.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | Fichier vidéo encodé à l’aide de la version du codec de profil avancé Windows Media Video 9 fourni avec le kit de développement logiciel (SDK) Windows Media format 11. Ce sous-type identifie un flux binaire conforme à la norme SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs de type de média**](media-type-identifiers.md)
</dt> <dt>

[**Types de médias**](media-types.md)
</dt> <dt>

[**Sous-types de médias non compressés**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




