---
title: Prise en charge des balises ID3
description: Prise en charge des balises ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, balises ID3
- Balises ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fd65ffadb952e9370af609e336c08fc07c9b96f50d09d95c78492bef2163db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703024"
---
# <a name="id3-tag-support"></a>Prise en charge des balises ID3

Le tableau suivant répertorie tous les attributs qui correspondent aux balises ID3. Si vous souhaitez utiliser les balises ID3 comme attributs au lieu d’utiliser les noms d’attributs standard, ajoutez le préfixe « ID3/ » au nom de la balise. Par exemple, « ID3/TPE2 » est l’équivalent de l' **auteur**.



| Attribut                      | ID3v1. x | ID3v 2.2 | ID3v 2.3/v 2.4 |
|--------------------------------|---------|---------|--------------|
| **Author**                     | Peinture  | TP1     | TPE1         |
| **Copyright**                  |         | TCR     | TCOP         |
| **CopyrightURL**               |         | WCP     | WCOP         |
| **Description**                | Commentaire | COM     | COMM         |
| **Durée**                   |         | TLE     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **Titre**                      | Titre   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | Album   | A     | TALB         |
| **WM/ArtistSortOrder**         |         |         | TSOP         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/binaire**                  |         | LOCAL     | GEOB         |
| **WM/comments**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/conducteur**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | 10MINUTES     | TENC         |
| **WM/EncodingSettings**        |         | TSS     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | Coût total de possession     | TCON         |
| **WM/InitialKey**              |         |         | TKEY         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/langage**                |         | BOÎTIER     | TLAN         |
| **Synchronisation des WM et des paroles \_**    |         | DES SLT     | SYLT         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/humeur**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | ASSURANCES     | TOTAL         |
| **WM/OriginalArtist**          |         | RÉFÉRENCES     | PARTIE supérieure         |
| **WM/OriginalFilename**        |         | TOF     | TOFN         |
| **WM/OriginalLyricist**        |         | ÉCART     | TOLY         |
| **WM/OriginalReleaseYear**     |         | TOR     | TORY         |
| **WM/PartOfSet**               |         | TPA     | TPOS         |
| **WM/image**                 |         | PIC     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/Publisher**               |         | TPB     | TPUB         |
| **WM/RadioStationName**        |         | LETTRAGE     | TRSN         |
| **WM/RadioStationOwner**       |         | TRO     | TRSO         |
| **WM/SetSubTitle**             |         |         | TSST         |
| **WM/sous-titre**                |         | TT3     | TIT3         |
| **WM/texte**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Suivre   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | UFI     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/Writer**                  |         | TXT     | TEXT         |
| **WM/Year**                    | Year    | TYE     | TYER         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> </dl>

 

 




