---
description: '\_type de contenu wpd \_ \_ \_ diffusion multimédia'
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4454053400c783b53437dd025e5adc8e845ea08c1b95b8d9b1fd358f39e326f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083313"
---
# <a name="wpd_content_type_media_cast"></a>\_type de contenu wpd \_ \_ \_ diffusion multimédia

Objet qui décrit son type en tant que \_ \_ type de contenu wpd \_ . le \_ cast de média représente une collection de contenu associé.

Un objet Mediacast peut être considéré comme un objet conteneur qui regroupe du contenu associé, de la même façon qu’une sélection de musique. Souvent, un objet Mediacast est utilisé pour regrouper le contenu multimédia qui a été publié en ligne. Par exemple, un canal RSS peut être représenté sous la forme d’un objet Mediacast dont les références d’objet pointent vers les objets de contenu qui représentent chaque élément dans le canal.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété             |  Obligatoire ou facultatif         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire.                                                             |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire.                                                             |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                             |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire.                                                             |
| [\_format d’objet wpd \_](object-properties.md)                                                        | Obligatoire.                                                             |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                           | Obligatoire.                                                             |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet est masqué.                                     |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                    | Obligatoire si l’objet est un objet système (représente un fichier système). |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet a au moins une ressource.                     |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                              | Obligatoire si l’objet représente un fichier.                             |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                       | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil. |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet a des références à d’autres objets.               |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Facultatif.                                                             |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Facultatif.                                                             |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                  | Obligatoire si l’objet est protégé par la technologie DRM.                |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                           | Facultatif.                                                             |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                         | Recommandé.                                                          |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                         | Facultatif.                                                             |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                     | Recommandé si l’objet est référencé par un autre objet.            |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)     | Facultatif.                                                             |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Facultatif.                                                             |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                               | Obligatoire si l’objet peut être supprimé.                                |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                | Obligatoire si l’objet ne peut pas être supprimé.                             |
| [\_Copyright du support wpd \_](media-properties.md)                                                     | Facultatif.                                                             |
| [\_ \_ classification parentale des médias wpd \_](media-properties.md)                                        | Facultatif.                                                             |
| [\_méta- \_ \_ genre de média wpd](media-properties.md)                                                  | Facultatif.                                                             |
| [\_sous- \_ \_ titre du média wpd](media-properties.md)                                                    | Facultatif.                                                             |
| [\_Date de \_ publication du support wpd \_](media-properties.md)                                              | Recommandé.                                                          |
| [\_titre du support wpd \_](media-properties.md)                                                             | Recommandé.                                                          |
| [\_propriétaire du média wpd \_](media-properties.md)                                                             | Recommandé.                                                          |
| [\_éditeur de \_ gestion du média wpd \_](media-properties.md)                                        | Recommandé.                                                          |
| [\_webmaster multimédia \_ wpd](media-properties.md)                                                     | Recommandé.                                                          |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                                                  | Recommandé.                                                          |
| [\_URL de \_ destination du support wpd \_](media-properties.md)                                        | Recommandé.                                                          |
| [\_Description du support wpd \_](media-properties.md)                                                 | Facultatif.                                                             |
| [\_genre de média wpd \_](media-properties.md)                                                             | Facultatif.                                                             |
| [signet de l' \_ objet multimédia wpd \_ \_](media-properties.md)                                        | Recommandé                                                           |
| [\_Date de \_ dernière \_ génération du média \_ wpd](media-properties.md)                                       | Recommandé.                                                          |
| [\_ \_ durée \_ de vie des \_ médias wpd](media-properties.md)                                             | Facultatif.                                                             |
| [\_sous- \_ \_ Description du média wpd](object-properties.md)                                                                 | Facultatif.                                                             |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                               | Obligatoire ou facultatif | Description                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md)      | Facultatif.            | Contient les données du fichier Mediacast. Par exemple, si ce Mediacast représente un canal RSS, il peut s’agir du document RSS. |
| [**\_miniature des ressources wpd \_**](wpd-resource-thumbnail.md)  | Facultatif.            | Contient la miniature représentant ce Mediacast.                                                                         |
| [**image de l' \_ album des ressources wpd \_ \_**](wpd-resource-album-art.md) | Facultatif.            | Contient l’illustration pour ce Mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Mappage des éléments RSS et des propriétés Mediacast

Un canal RSS peut être représenté sous la forme d’un objet Mediacast dont les références pointent vers des objets de contenu représentant chaque élément d’un canal donné.

Les éléments d’un flux RSS possèdent la hiérarchie et les attributs suivants.


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



Le tableau suivant répertorie les éléments de canal dans un flux RSS et les \_ \_ Propriétés de \_ diffusion multimédia du type de contenu wpd correspondant \_ .



| Élément Channel | Spécification du flux RSS | Propriété Mediacast correspondante      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| catégorie            | Facultatif.                | [\_genre de média wpd \_](media-properties.md)                       |
| cloud               | Non applicable.          | Non applicable.                                                                 |
| copyright           | Facultatif.                | [\_Copyright du support wpd \_](media-properties.md)               |
| description         | Obligatoire.                | [\_Description du support wpd \_](media-properties.md)           |
| docs                | Non applicable.          | Non applicable.                                                                 |
| générateur           | Non applicable.          | Non applicable.                                                                 |
| langage            | Non applicable.          | Non applicable.                                                                 |
| lastBuildDate       | Facultatif.                | [\_Date de \_ dernière \_ génération du média \_ wpd](media-properties.md) |
| link                | Obligatoire.                | [\_URL de \_ destination du support wpd \_](media-properties.md)  |
| managingEditor      | Facultatif.                | [\_éditeur de \_ gestion du média wpd \_](media-properties.md)  |
| pubDate             | Facultatif.                | [\_Date de \_ publication du support wpd \_](media-properties.md)        |
| rating              | Non applicable.          | Non applicable.                                                                 |
| skipDays            | Non applicable.          | Non applicable.                                                                 |
| skipHours           | Non applicable.          | Non applicable.                                                                 |
| textInput           | Non applicable.          | Non applicable.                                                                 |
| title               | Obligatoire.                | [nom de l' \_ objet wpd \_](object-properties.md)                      |
| ttl                 | Facultatif.                | [\_ \_ durée \_ de vie des \_ médias wpd](media-properties.md)       |
| webMaster           | Facultatif.                | [\_webmaster multimédia \_ wpd](media-properties.md)               |



 

Le tableau suivant répertorie les éléments d’image dans un flux RSS et les \_ \_ Propriétés de \_ diffusion multimédia du type de contenu wpd correspondant \_ .



| Élément Image | Spécification du flux RSS | Propriété Mediacast                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| description       | Facultatif.                | [\_Description du support wpd \_](media-properties.md)          |
| height            | Facultatif.                | [\_hauteur du média wpd \_](media-properties.md)                    |
| link              | Facultatif.                | [\_URL de \_ destination du support wpd \_](media-properties.md) |
| title             | Facultatif.                | [nom de l' \_ objet wpd \_](object-properties.md)                     |
| url               | Facultatif.                | [URL de la \_ source du média wpd \_ \_](media-properties.md)           |
| width             | Facultatif.                | [\_largeur du média wpd \_](media-properties.md)                      |



 

Le tableau suivant répertorie les éléments Item d’un flux RSS et les \_ Propriétés de \_ diffusion multimédia du type de contenu wpd correspondant \_ \_ .



| Item, élément | Attribut | Spécification du flux RSS | Propriété Mediacast  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| auteur           |               | Facultatif.                | [\_artiste multimédia \_ wpd](media-properties.md)                    |
| catégorie         |               | Facultatif.                | [\_genre de média wpd \_](media-properties.md)                      |
|                  | domaine        | Non applicable.          | Non applicable.                                                                |
| description      |               | Facultatif.                | [\_Description du support wpd \_](media-properties.md)          |
| coffret        |               | Facultatif.                |                                                                                |
|                  | url           | Obligatoire.                | [URL de la \_ source du média wpd \_ \_](media-properties.md)           |
|                  | length        | Obligatoire.                | [taille de l' \_ objet wpd \_](object-properties.md)                     |
|                  | Type          | Obligatoire.                | (Le type MIME doit être mappé au type de contenu de la propriété.)                 |
| guid             |               | Facultatif.                | [\_GUID du média wpd \_](media-properties.md)                        |
|                  | isPermaLink   | Non applicable.          | Non applicable.                                                                |
| link             |               | Facultatif.                | [\_URL de \_ destination du support wpd \_](media-properties.md) |
| pubDate          |               | Facultatif.                | [\_Date de \_ publication du support wpd \_](media-properties.md)       |
| source           |               | Non applicable.          | Non applicable.                                                                |
| title            |               | Facultatif.                | [nom de l' \_ objet wpd \_](object-properties.md)                     |



 

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
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Mappage d’éléments de canal RSS à des valeurs de propriété WPD

Le tableau suivant décrit comment les valeurs des éléments de canal RSS de l’exemple précédent sont mappées à des propriétés WPD particulières.



| WPD, propriété | Valeur |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [\_Copyright du support wpd \_](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. Tous droits réservés.                                        |
| [\_Description du support wpd \_](media-properties.md)                        | Peter Bankov, PDG de Lucerne Publishing, examine les dernières tendances des publications en ligne. |
| [\_URL de \_ destination du support wpd \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [\_genre de média wpd \_](media-properties.md)                                    | Actualités                                                                                          |
| [\_Date de \_ dernière \_ génération du média \_ wpd](media-properties.md)              | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_éditeur de \_ gestion du média wpd \_](media-properties.md)               | someone@example.com                                                                           |
| [\_Date de \_ publication du support wpd \_](media-properties.md)                     | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_ \_ durée \_ de vie des \_ médias wpd](media-properties.md)                    | 240                                                                                           |
| [\_titre du support wpd \_](media-properties.md)                                    | La publication numérique                                                                       |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [\_webmaster multimédia \_ wpd](media-properties.md)                            | someone@example.com                                                                           |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                  | \_type de contenu wpd \_ \_ \_ diffusion multimédia                                                               |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                  | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                | Vendredi 9 juin 2006 14:00:28 EDT                                                                 |
| [\_format d’objet wpd \_](object-properties.md)                               | FORMAT d’objet WPD- \_ \_ \_ Cast abstrait de \_ média \_                                                    |
| [\_ID d’objet wpd \_](object-properties.md)                                       | Valeur dépendante de la session.                                                                      |
| [nom de l' \_ objet wpd \_](object-properties.md)                                   | La publication numérique                                                                       |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)     | La publication numérique                                                                       |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                        | MyPodcasts (un dossier de podcast fictif sur l’appareil). Supposons « 0A0 » pour cet exemple.        |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md) | Valeur indépendante de la session. (Supposons « 0A1 » pour cet exemple.)                                   |
| [\_références d’objets wpd \_](object-properties.md)                       | 0A2 pour N éléments<br/>                                                                   |
| [taille de l' \_ objet wpd \_](object-properties.md)                                   | 13 790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Mappage d’éléments d’image RSS à des valeurs de propriété WPD

Le tableau suivant décrit comment les valeurs des éléments d’image RSS de l’exemple précédent sont mappées à des propriétés WPD particulières.



| WPD, propriété               |                         Valeur                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [\_Description du support wpd \_](media-properties.md)                                                   | Logo Lucerne                                        |
| [\_URL de \_ destination du support wpd \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [\_hauteur du média wpd \_](media-properties.md)                                                             | 300                                                 |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_largeur du média wpd \_](media-properties.md)                                                               | 300                                                 |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                              | Lucerne Publishing                                  |
| [l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé](attributes.md)                               | VARIANTE \_ true                                       |
| [l' \_ attribut de ressource wpd \_ \_ peut \_ lire](attributes.md)                                   | VARIANTE \_ true                                       |
| [\_format d' \_ attribut de ressource wpd \_](resource-attribute-properties.md)                     | \_ \_ gif format d’objet wpd \_                            |
| [\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd](attributes.md) | 1 024                                                |
| [\_ \_ \_ taille totale de l’attribut de ressource wpd \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Mappage d’éléments d’élément RSS à des valeurs de propriété WPD

Le tableau suivant décrit comment les valeurs des éléments de l’élément RSS de l’exemple précédent sont mappées à des propriétés WPD particulières.



| WPD, propriété  | Valeur                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [\_titre du support wpd \_](media-properties.md)                                    | La publication numérique                                                                                                          |
| [\_durée du média wpd \_](media-properties.md)                              | 10329011                                                                                                                         |
| [\_artiste multimédia \_ wpd](media-properties.md)                                  | Lucerne                                                                                                                          |
| [\_Description du support wpd \_](media-properties.md)                        | Les publications en ligne évoluent rapidement. Le PDG d’une maison de publication examine les tendances des 5 dernières années et leurs implications. |
| [\_URL de \_ destination du support wpd \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_genre de média wpd \_](media-properties.md)                                    | Actualités                                                                                                                             |
| [\_GUID du média wpd \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_Date de \_ publication du support wpd \_](media-properties.md)                     | Case, 1er juin 2006 14:00:28 EDT                                                                                                   |
| [URL de la \_ source du média wpd \_ \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)            | 0A1                                                                                                                              |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                  | \_image de \_ média du type de contenu wpd \_ \_                                                                                                 |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                | Case, 1er juin 2006 14:00:28 EDT                                                                                                   |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                  | Case, 1er juin 2006 14:00:28 EDT                                                                                                   |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                | Case, 1er juin 2006 14:00:28 EDT                                                                                                   |
| [\_format d’objet wpd \_](object-properties.md)                               | FORMAT de l' \_ objet wpd \_ \_ mp3                                                                                                         |
| [\_ID d’objet wpd \_](object-properties.md)                                       | Dépendant de la session. (Supposons « 0A2 » pour cet exemple.)                                                                              |
| [nom de l' \_ objet wpd \_](object-properties.md)                                   | La publication numérique                                                                                                          |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md) | Indépendant de la session.                                                                                                             |
| [taille de l' \_ objet wpd \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 




