---
title: Personnalisation de la distribution des médias
description: Personnalisation de la distribution des médias
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Sélections de métafichiers multimédias, personnalisation de la distribution de médias
- sélections, personnalisation de la distribution des médias
- sélections de métafichiers, personnalisation de la distribution de médias
- Windows Sélections de métafichiers multimédia, personnalisation de la remise de médias
- sélections, personnalisation de la distribution des médias
- sélections de métafichiers, personnalisation de la remise de médias
- personnalisation de la livraison des médias
- personnalisation de la distribution des médias
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9483f4fc7a068c6f6456a5d170b4be73a9ba31ef85294f9a6939181dff00c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996009"
---
# <a name="personalizing-media-delivery"></a>Personnalisation de la distribution des médias

contrairement à la communication unidirectionnelle qui diffuse du contenu identique à un public de masse, Windows Media Technologies vous fournit les outils nécessaires à l’utilisation de données démographiques pour individualiser des diffusions. Avec Internet, une communication bidirectionnelle à grande échelle est facilement disponible. Cet échange d’informations dynamique permet aux fournisseurs de contenu de connaître leur public et de répondre aux présentations personnalisées.

L’exemple suivant, qui utilise une société fictive, illustre la manière dont la distribution de contenu de diffusion en continu peut être personnalisée. Cette discussion part du principe que vous êtes familiarisé avec les pages de Active Server (fichiers ASP ou. asp) et à la définition des variables.

News Network est une organisation d’actualités de diffusion fictive qui a développé ses opérations pour inclure un site Web. La principale fonctionnalité du site est une section dans laquelle les utilisateurs peuvent créer leurs propres newscasts personnalisées. Au lieu d’afficher un Newscast traditionnel destiné à un public de masse, un utilisateur voit un programme complet qui contient uniquement des sujets d’intérêt personnel. La séquence suivante décrit une expérience utilisateur typique.

1.  Un nouvel utilisateur accède au site et clique sur **créer votre Newscast personnel**.
2.  Un formulaire de préférences s’ouvre. Sur ce formulaire, l’utilisateur répond à des questions concernant les préférences personnelles, telles que les articles d’actualité préférés, les articles les plus préférés, les hobbies et la méthode habituelle de réception d’actualités quotidiennes.
3.  L’utilisateur envoie ces informations, et quelques secondes plus tard, affichent un Newscast personnel complet de 15 minutes, contenant le contenu du programme, les transitions et les commerciaux. la sélection de chaque élément multimédia, y compris les commerciaux, est basée sur le profil utilisateur et s’effectue automatiquement avec Windows composants media Technologies et les outils Internet prêts à l’emploi.

La liste suivante décrit comment les différents outils interagissent pour créer un Newscast personnalisé.

1.  Le formulaire de préférence que l’utilisateur remplit est une page de Active Server (ASP) (Choices. asp). Les données obtenues à partir de la forme de préférence sont analysées par deux composants serveur. un composant utilise les informations pour interroger une base de données Microsoft SQL Server de nouvelles histoires. L’autre composant est un serveur AD qui utilise un ensemble complexe de règles basées sur les exigences contractuelles et démographiques pour planifier des publicités appropriées à l’utilisateur à ce moment-là.
2.  Les deux bases de données retournent différentes parties d’une sélection. La base de données News Story retourne un ensemble d’entrées d’histoires appropriées, et le serveur Active Directory renvoie un ensemble d’entrées commerciales appropriées.
3.  Une deuxième page ASP (PlayShow. asp) reçoit les entrées de la base de données d’actualités et d’AD Server, et les combine avec les entrées standard afficher ouvrir, fermer et transition. Toutes les entrées sont ensuite présentées en fonction du modèle fourni par PlayShow. asp, et la page ASP renvoie une sélection à l’utilisateur.
4.  le contrôle de Lecteur Windows Media incorporé sur l’ordinateur de l’utilisateur lit la sélection du début à la fin, et l’utilisateur voit un newscast personnalisé.

L’exemple suivant est une partie d’un fichier de sélection qu’un utilisateur peut recevoir. Des bannières Active Directory, des liens MOREINFO et des RÉSUMÉs ont été ajoutés.


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   Les exemples de sociétés, organisations, produits, personnes et événements utilisés dans les exemples sont fictifs. Toute ressemblance avec des noms ou des événements réels est purement fortuite et involontaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




