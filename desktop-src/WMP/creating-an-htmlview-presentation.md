---
title: Création d’une présentation HTMLView
description: Création d’une présentation HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Sélections de métafichiers Windows Media, présentations HTMLView
- sélections, présentations HTMLView
- sélections de métafichiers, présentations HTMLView
- Sélections de métafichiers Windows Media, création de présentations HTMLView
- sélections, création de présentations HTMLView
- sélections de métafichiers, création de présentations HTMLView
- création de présentations HTMLView
- Windows Media Player, création de présentations HTMLView
- Windows Media Player, présentations HTMLView
- HTMLView, création de présentations
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380097"
---
# <a name="creating-an-htmlview-presentation"></a>Création d’une présentation HTMLView

Pour créer une présentation HTMLView de base, vous avez besoin d’au moins trois éléments :

-   **Contenu multimédia numérique.** Il s’agit d’un ou plusieurs fichiers audio ou vidéo que le lecteur Windows Media lit.
-   **Une page Web.** Il s’agit du contenu Web qui s’affiche dans la fonctionnalité de **lecture** en cours de l’interface utilisateur du lecteur.
-   **Métafichier Windows Media.** Il s’agit de la sélection de métafichiers qui indique au lecteur Windows Media de combiner le contenu multimédia numérique avec la page Web.

Un fichier. asx est un fichier texte qui fournit des informations sur un flux de fichier et sa présentation. En fonction de la syntaxe Extensible Markup Language (XML), les fichiers. asx peuvent contenir divers éléments, chacun identifié par une balise avec des attributs associés. L’élément **param** permet d’associer un paramètre personnalisé à une entrée particulière dans une sélection de métafichier ou dans le métafichier entier. L’un des noms de paramètres prédéfinis disponibles pour votre utilisation est « HTMLView ». Il s’agit du paramètre qui permet d’afficher la page Web spécifiée par la valeur de l’URL dans le lecteur Windows Media.

L’exemple de code suivant montre un fichier. asx qui combine un fichier multimédia numérique unique à une seule page Web :


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Lorsque le lecteur Windows Media ouvre le fichier. asx dans l’exemple précédent, il lit le fichier audio à partir du fichier nommé Content1. WMA et ouvre la page Web nommée htmlview.htm dans la fonctionnalité de **lecture** en cours du lecteur en mode plein. L’utilisateur peut suspendre, Rechercher et arrêter le contenu audio à l’aide des commandes du lecteur Windows Media.

Vous pouvez facilement modifier la page Web affichée pour chaque élément de contenu en associant un élément **param** à chaque entrée, comme le montre l’exemple de code suivant :


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



Dans l’exemple précédent, le lecteur Windows Media affiche d’abord la page Web htmlview1.htm lors de la lecture du fichier audio numérique Content1. WMA. Lorsque le joueur ouvre l’entrée suivante dans la playlist, Content2. WMA, la page Web affichée dans **lecture** passe à htmlview2.htm. De cette façon, vous pouvez spécifier la page Web que l’utilisateur voit pour chaque morceau de contenu multimédia numérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Affichage des pages Web dans le lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Élément PARAM**](param-element.md)
</dt> </dl>

 

 




