---
title: Retournement d’URL
description: Retournement d’URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player, présentations basées sur le Web
- Modèle objet du lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Windows Media Player Mobile, présentations basées sur le Web
- Contrôle ActiveX du lecteur Windows Media, présentations basées sur le Web
- Windows Media Player Mobile contrôle ActiveX, présentations basées sur le Web
- Contrôle ActiveX, présentations basées sur le Web
- Lecteur Windows Media, basculement d’URL
- Windows Media Player Object Model, retournement d’URL
- modèle objet, basculement d’URL
- Windows Media Player Mobile, basculement d’URL
- Contrôle ActiveX du lecteur Windows Media, retournement d’URL
- Windows Media Player Mobile Control, basculement d’URL
- Contrôle ActiveX, basculement d’URL
- Présentations basées sur le Web, retournement d’URL
- création de présentations basées sur le Web, retournement d’URL
- Retournement d’URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "103676014"
---
# <a name="url-flipping"></a>Retournement d’URL

L’utilisation de pages Web pour les diaporamas s’appelle le basculement d’URL et est gérée automatiquement par le lecteur Windows Media lorsqu’il rencontre des commandes de script d’URL incorporées dans le flux de médias numériques qu’il lit. Vous pouvez spécifier un frame cible pour vos pages dans chaque commande de script, ou vous pouvez le spécifier en définissant la propriété **Settings. defaultFrame** . Vous pouvez définir cette propriété dans le code de script ou à l’aide d’un élément PARAM au sein de l’élément OBJECT qui incorpore le contrôle du lecteur Windows Media.

Vous êtes libre de gérer les commandes de script d’URL dans votre code JScript tout comme vous le feriez pour gérer des commandes de script personnalisées. Si vous souhaitez que le contrôle du lecteur Windows Media ignore les commandes de script d’URL afin que vous puissiez les gérer entièrement par vous-même, définissez les *paramètres*. propriété **invokeURLs** la valeur false dans le code de script ou à l’aide d’un élément param comme décrit précédemment.

L’exemple suivant illustre un jeu de frames standard pour le basculement d’URL. Tout d’abord, créez une page décrivant le jeu de frames :


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Ensuite, créez le fichier player.html référencé dans le jeu de frames à l’aide du code suivant (le fichier Video. wmv est supposé exister dans le même répertoire que les fichiers HTML) :


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



Si vos pages Web sont suffisamment petites pour être chargées rapidement, cette configuration peut suffire à vos besoins. Si, en revanche, vos pages Web sont complexes, le streaming multimédia enrichi peut être plus efficace en fonction de la vitesse de connexion de votre public.

> [!Note]  
> Le retournement d’URL ne fonctionne pas correctement avec les pages affichées dans Netscape Navigator. Au lieu d’apparaître dans le frame spécifié par **defaultFrame**, chaque commande de script d’URL reçue dans le navigateur affiche l’URL dans une nouvelle fenêtre de navigateur.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de présentations Web-Based**](creating-web-based-presentations.md)
</dt> <dt>

[**Utilisation d’un script pour contrôler le basculement d’URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




