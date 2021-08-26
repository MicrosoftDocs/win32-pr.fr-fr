---
title: mappage des flux RSS aux propriétés du Gestionnaire de périphériques de médias Windows
description: mappage des flux RSS aux propriétés du Gestionnaire de périphériques de médias Windows
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Gestionnaire de périphériques de média, flux RSS
- Gestionnaire de périphériques, flux RSS
- Guide de programmation, flux RSS
- applications de bureau, flux RSS
- création d’applications Windows Media Gestionnaire de périphériques, flux RSS
- Flux RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355515217db31740603d5c6323ef8455da4b29ee80bec508897d2d4df5d59bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031679"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>mappage des flux RSS aux propriétés du Gestionnaire de périphériques de médias Windows

Lecteur Windows Media 11 fournit une fonctionnalité d’agrégation RSS qui permet aux utilisateurs de stocker du contenu obtenu à partir de podcasts sur leurs ordinateurs. Cette rubrique décrit les éléments XML trouvés dans un flux RSS. en outre, il mappe ces éléments RSS à Windows propriétés de Gestionnaire de périphériques de média.

Les éléments d’un flux RSS possèdent la hiérarchie et les attributs suivants :


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



le tableau suivant répertorie les éléments de canal dans un flux RSS et les propriétés de Gestionnaire de périphériques de média Windows correspondantes.



| Élément Channel | Statut         | propriété de Gestionnaire de périphériques de média Windows correspondante   |
|-----------------|----------------|-------------------------------------------------------|
| catégorie        | Facultatif       | [\_wszWMDMGenre g](metadata-constants.md)             |
| cloud           | Non applicable | Non applicable                                        |
| copyright       | Facultatif       | [\_wszWMDMProviderCopyright g](metadata-constants.md) |
| description     | Obligatoire       | [\_wszWMDMDescription g](metadata-constants.md)       |
| docs            | Non applicable | Non applicable                                        |
| générateur       | Non applicable | Non applicable                                        |
| langage        | Non applicable | Non applicable                                        |
| lastBuildDate   | Facultatif       | [\_wszWMDMLastModifiedDate g](metadata-constants.md)  |
| link            | Obligatoire       | [\_wszWMDMDestinationURL g](metadata-constants.md)    |
| managingEditor  | Facultatif       | [\_wszWMDMEditor g](metadata-constants.md)            |
| pubDate         | Facultatif       | [\_wszWMDMYear g](metadata-constants.md)              |
| rating          | Non applicable | Non applicable                                        |
| skipDays        | Non applicable | Non applicable                                        |
| skipHours       | Non applicable | Non applicable                                        |
| textInput       | Non applicable | Non applicable                                        |
| title           | Obligatoire       | [\_wszWMDMTitle g](metadata-constants.md)             |
| ttl             | Facultatif       | [\_wszWMDMTimeToLive g](metadata-constants.md)        |
| webMaster       | Facultatif       | [\_wszWMDMWebMaster g](metadata-constants.md)         |



 

Le tableau suivant répertorie les éléments d’image dans un flux RSS et les propriétés WMDM correspondantes.



| Élément Image | Statut   | propriété de Gestionnaire de périphériques de média Windows correspondante |
|---------------|----------|-----------------------------------------------------|
| description   | Facultatif | [\_wszWMDMDescription g](metadata-constants.md)     |
| height        | Facultatif | [\_wszWMDMHeight g](metadata-constants.md)          |
| link          | Facultatif | [\_wszWMDMDestinationURL g](metadata-constants.md)  |
| title         | Facultatif | [\_wszWMDMTitle g](metadata-constants.md)           |
| url           | Facultatif | [\_wszWMDMSourceURL g](metadata-constants.md)       |
| width         | Facultatif | [\_wszWMDMWidth g](metadata-constants.md)           |



 

le tableau suivant répertorie les éléments item d’un flux RSS et les propriétés de Gestionnaire de périphériques de média Windows correspondantes.



| Item, élément | Attribut   | Statut         | propriété de Gestionnaire de périphériques de média Windows correspondante            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| auteur       |             | Facultatif       | [\_wszWMDMAuthor g](metadata-constants.md)                     |
| catégorie     |             | Facultatif       | [\_wszWMDMGenre g](metadata-constants.md)                      |
|              | domaine      | Non applicable | Non applicable                                                 |
| description  |             | Facultatif       | [\_wszWMDMDescription g](metadata-constants.md)                |
| coffret    |             | Facultatif       | Non applicable                                                 |
|              | length      | Obligatoire       | [\_wszWMDMFileSize g](metadata-constants.md)                   |
|              | type        | Obligatoire       | (Le type MIME doit être mappé au type de contenu de la propriété.) |
|              | url         | Obligatoire       | [\_wszWMDMSourceURL g](metadata-constants.md)                  |
| guid         |             | Facultatif       | [\_wszWMDMediaGuid g](metadata-constants.md)                   |
|              | isPermaLink | Non applicable | Non applicable                                                 |
| link         |             | Facultatif       | [\_wszWMDMDestinationURL g](metadata-constants.md)             |
| pubDate      |             | Facultatif       | [\_wszWMDMYear g](metadata-constants.md)                       |
| source       |             | Non applicable | Non applicable                                                 |
| title        |             | Facultatif       | [\_wszWMDMTitle g](metadata-constants.md)                      |



 

Exemple

L’exemple suivant montre un flux RSS complet pour un podcast fictif fourni par le PDG d’une société de publication.


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



mappage d’éléments de canal RSS à des valeurs de propriété de Windows Media Gestionnaire de périphériques

le tableau suivant décrit la façon dont les valeurs des éléments de canal RSS de l’exemple précédent sont mappées à des propriétés de Gestionnaire de périphériques de média Windows spécifiques.



| Windows Propriété Media Gestionnaire de périphériques                    | Valeur                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [\_wszWMDMAuthorDate g](metadata-constants.md)           | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_wszWMDMDESCRIPTION g](metadata-constants.md)          | Peter Bankov, PDG de Lucerne Publishing, examine les dernières tendances des publications en ligne. |
| [\_URL wszWMDMDESTINATION \_ g](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [\_wszWMDMEDITOR g](metadata-constants.md)               | someone@example.com                                                                           |
| [\_wszWMDMFileCreationDate g](metadata-constants.md)     | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_wszWMDMFileName g](metadata-constants.md)             | La publication numérique                                                                       |
| [\_wszWMDMFileSize g](metadata-constants.md)             | 13 790                                                                                        |
| [\_wszWMDMFormatCode g](metadata-constants.md)           | WMDM \_ FORMATCODE \_ Media \_ cast                                                                 |
| [\_wszWMDMGENRE g](metadata-constants.md)                | Actualités                                                                                          |
| [\_wszWMDMLAST \_ Date de modification \_ du g](metadata-constants.md) | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_wszWMDMLastModifiedDate g](metadata-constants.md)     | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_wszWMDMProviderCopyright g](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. Tous droits réservés.                                        |
| [\_wszWMDMTimeToLive g](metadata-constants.md)           | 240                                                                                           |
| [\_wszWMDMTitle g](metadata-constants.md)                | La publication numérique                                                                       |
| [\_wszWMDMWEBMASTER g](metadata-constants.md)            | someone@example.com                                                                           |
| [\_wszWMDMYear g](metadata-constants.md)                 | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |



 

mappage d’éléments d’Image RSS à des valeurs de propriété de Windows Media Gestionnaire de périphériques

le tableau suivant décrit la façon dont les valeurs des éléments d’Image RSS de l’exemple précédent sont mappées à des propriétés de Gestionnaire de périphériques de média Windows spécifiques.



| Windows Propriété Media Gestionnaire de périphériques                | Valeur                                            |
|------------------------------------------------------|--------------------------------------------------|
| [\_wszWMDMAlbumCoverFormat g](metadata-constants.md) | \_ \_ gif format d’objet wpd \_                         |
| [\_wszWMDMAlbumCoverSize g](metadata-constants.md)   | 512                                              |
| [\_wszWMDMDescription g](metadata-constants.md)      | Logo Lucerne                                     |
| [\_wszWMDMDestinationURL g](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [\_wszWMDMHeight g](metadata-constants.md)           | 300                                              |
| [\_wszWMDMSourceURL g](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [\_wszWMDMTitle g](metadata-constants.md)            | Lucerne Publishing                               |
| [\_wszWMDMWidth g](metadata-constants.md)            | 300                                              |



 

mappage d’éléments d’élément RSS à des valeurs de propriété Media Gestionnaire de périphériques Windows

le tableau suivant décrit la façon dont les valeurs des éléments de l’élément RSS de l’exemple précédent sont mappées à des propriétés Windows Media Gestionnaire de périphériques spécifiques.



| Windows Propriété Media Gestionnaire de périphériques                | Valeur                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [\_wszWMDMAuthor g](metadata-constants.md)           | Lucerne                                                                                                                             |
| [\_wszWMDMAuthorDate g](metadata-constants.md)       | Case, 1er juin 2006 14:00:28 EDT                                                                                                      |
| [\_wszWMDMDescription g](metadata-constants.md)      | Les publications en ligne évoluent rapidement. Le PDG d’une maison de publication examine les tendances des cinq dernières années et leurs implications. |
| [\_wszWMDMDestinationURL g](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [\_wszWMDMDuration g](metadata-constants.md)         | 120325445                                                                                                                           |
| [\_wszWMDMFileCreationDate g](metadata-constants.md) | Case, 1er juin 2006 14:00:28 EDT                                                                                                      |
| [\_wszWMDMFileSize g](metadata-constants.md)         | 10329011                                                                                                                            |
| [\_wszWMDMFormatCode g](metadata-constants.md)       | \_Mp3 WMDM FORMATCODE \_                                                                                                               |
| [\_wszWMDMGenre g](metadata-constants.md)            | Actualités                                                                                                                                |
| [\_wszWMDMLastModifiedDate g](metadata-constants.md) | Case, 1er juin 2006 14:00:28 EDT                                                                                                      |
| [\_wszWMDMMediaGuid g](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [\_wszWMDMSourceURL g](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [\_wszWMDMTitle g](metadata-constants.md)            | La publication numérique                                                                                                             |
| [\_wszWMDMYear g](metadata-constants.md)             | Case, 1er juin 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes de métadonnées**](metadata-constants.md)
</dt> </dl>

 

 




