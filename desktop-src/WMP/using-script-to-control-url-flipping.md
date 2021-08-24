---
title: Utilisation d’un script pour contrôler le basculement d’URL
description: Utilisation d’un script pour contrôler le basculement d’URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Lecteur Windows Media, présentations basées sur le Web
- modèle objet Lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Lecteur Windows Media Présentations mobiles, basées sur le Web
- contrôle de ActiveX Lecteur Windows Media, présentations basées sur le Web
- Lecteur Windows Media contrôle Mobile ActiveX, présentations basées sur le Web
- contrôle de ActiveX, présentations basées sur le Web
- Lecteur Windows Media, retournement d’URL
- Lecteur Windows Media modèle objet, retournement d’URL
- modèle objet, basculement d’URL
- Lecteur Windows Media Mobile, basculement d’URL
- contrôle de ActiveX Lecteur Windows Media, retournement d’URL
- Lecteur Windows Media contrôle de ActiveX Mobile, basculement d’URL
- contrôle ActiveX, retournement d’URL
- Présentations basées sur le Web, retournement d’URL
- création de présentations basées sur le Web, retournement d’URL
- Retournement d’URL
- Lecteur Windows Media, diffusion multimédia riche
- Lecteur Windows Media modèle objet, diffusion multimédia riche
- modèle objet, diffusion multimédia riche
- Lecteur Windows Media Mobile, diffusion multimédia riche
- contrôle de ActiveX Lecteur Windows Media, diffusion multimédia riche
- Lecteur Windows Media contrôle de ActiveX Mobile, diffusion multimédia riche
- contrôle de ActiveX, diffusion multimédia riche
- Présentations basées sur le Web, diffusion multimédia riche
- création de présentations basées sur le Web, diffusion multimédia riche
- diffusion multimédia enrichie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9470bf2b812d36bceb6159ab089e3b08c49bc84515320872b125ed6519568141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507129"
---
# <a name="using-script-to-control-url-flipping"></a>Utilisation d’un script pour contrôler le basculement d’URL

lorsqu’un utilisateur se connecte à un flux multimédia riche alors que le flux est déjà en cours, il est possible que la page web en continu s’affiche avant que tous les éléments soient arrivés et mis en cache si Lecteur Windows Media appelle automatiquement l’URL. Dans ce cas, l’utilisateur voit une page Web vide ou incomplète jusqu’à ce que le jeu de données suivant arrive dans le cache.

vous pouvez éviter d’afficher une page web vide ou incomplète en appelant l’URL à l’aide d’un script au lieu de laisser Lecteur Windows Media le faire automatiquement. De cette façon, vous pouvez ignorer la première inversion de l’URL, puis appeler les URL suivantes à l’aide du code de script.

> [!Note]  
> cette section part du principe que vous diffusez en continu du code html à l’aide du kit de développement logiciel (SDK) de la série Windows Media encoder 9 et que vous avez défini le flux html sur repeat.

 

Tout d’abord, vous devez créer une page Web de jeu de frames pour contenir le frame avec le lecteur incorporé et le frame qui affiche le HTML de diffusion en continu. Chacun de ces deux frames affiche une page Web distincte. vous allez donc créer un total de trois pages Web. L’exemple de code suivant illustre la page Web du jeu de cadres :


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



L’exemple de page Web précédent incorpore deux frames. La première image s’affiche dans la moitié gauche de la fenêtre du navigateur et affiche la page Web nommée incorporer \_player.htm. L’exemple de code suivant crée cette page Web :


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



Le deuxième Frame dans le jeu de frames s’affiche dans la moitié droite de la fenêtre du navigateur et affiche une page Web nommée « blank.htm ». L’exemple de code suivant crée cette page Web :


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Lorsque la page du jeu de cadres est chargée dans le navigateur, le frame de gauche montre le lecteur incorporé et le cadre de droite affiche le texte « chargement en cours... ». pour informer l’utilisateur que des données supplémentaires sont à venir. Lorsque la première commande de script d’URL arrive à partir du flux HTML, le gestionnaire d’événements modifie simplement la valeur de l’indicateur **booléen** . Lorsque chaque commande de script d’URL suivante arrive à partir du flux HTML, le script du gestionnaire d’événements charge la nouvelle URL dans le frame nommé « content » et la page Web complète s’affiche dans le frame situé dans la moitié droite de la fenêtre du navigateur.

pour plus d’informations sur la diffusion en continu de code HTML à l’aide de Windows media, consultez le kit de développement logiciel Windows media encoder

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Diffusion multimédia enrichie**](rich-media-streaming.md)
</dt> <dt>

[**Retournement d’URL**](url-flipping.md)
</dt> </dl>

 

 




