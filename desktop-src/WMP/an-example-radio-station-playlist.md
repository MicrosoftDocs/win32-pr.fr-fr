---
title: Exemple de sélection de station de radio
description: Exemple de sélection de station de radio
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Sélections de métafichiers Windows Media, exemples de sélection
- sélections, exemples de sélection
- sélections de métafichiers, exemples de sélection
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemple de code
- sélections, exemple de code
- sélections de métafichiers, exemple de code
- Sélections de métafichiers Windows Media, exemple de sélection de station de radio
- sélections, exemple de sélection de station de radio
- sélections de métafichiers, exemple de sélection de station de radio
- Windows Media Player, exemples de sélection
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemple de sélection de station de radio
- exemples de sélection
- exemples de sélections
- exemples de sélections
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379820"
---
# <a name="an-example-radio-station-playlist"></a>Exemple de sélection de station de radio

L’exemple de code suivant montre comment créer une sélection pour analyser trois stations de radio Rock. La société fictive Adventure Works radio figure sur la sélection et sur tous les flux individuels de la playlist. Lorsque vous écrivez votre code, remplacez toutes les URL et tous les noms de fichiers par des noms de fichiers valides accessibles à votre lecteur Windows Media.

Une sélection est créée pour chacune des stations. Une quatrième playlist balaie les trois premières. Les sélections sont créées pour référencer des publications générées de manière dynamique et avoir la personnalisation radio d’Adventure Works.

L’une des sélections représentant une station de radio peut se présenter comme suit.


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



La sélection peut ensuite être constituée de références à des sélections individuelles.

Exemple de code


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



Dans cet exemple, une publicité est suivie de 30 secondes de chacune des trois stations référencées, l’une après l’autre. Ce cycle se répète indéfiniment, car l’attribut **Count** de l’élément **REPEAT** n’est pas défini.

-   Les exemples de sociétés, organisations, produits, personnes et événements utilisés dans les exemples sont fictifs. Toute ressemblance avec des noms ou des événements réels est purement fortuite et involontaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Exemples de sélections**](example-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




