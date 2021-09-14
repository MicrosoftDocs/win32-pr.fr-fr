---
title: Retournement d’URL
description: Retournement d’URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403780"
---
# <a name="url-flipping"></a>Retournement d’URL

l’utilisation de pages web pour les diaporamas s’appelle le basculement d’url et est gérée automatiquement par Lecteur Windows Media lorsqu’il rencontre des commandes de script d’url incorporées dans le flux de média numérique qu’il lit. vous pouvez spécifier un frame cible pour vos pages dans chaque commande de script, ou vous pouvez le spécifier en définissant la propriété **Paramètres. defaultFrame** . vous pouvez définir cette propriété dans le code de script ou à l’aide d’un élément PARAM au sein de l’élément OBJECT qui incorpore le contrôle Lecteur Windows Media.

vous êtes libre de gérer les commandes de script d’URL dans votre code JScript comme vous le feriez pour gérer des commandes de script personnalisées. si vous souhaitez que le contrôle Lecteur Windows Media ignore les commandes de script d’URL afin que vous puissiez les gérer entièrement par vous-même, définissez le *Paramètres*. propriété **invokeURLs** la valeur false dans le code de script ou à l’aide d’un élément param comme décrit précédemment.

L’exemple suivant illustre un jeu de frames standard pour le basculement d’URL. Tout d’abord, créez une page décrivant le jeu de frames :


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Ensuite, créez le fichier player.html référencé dans le jeu de frames en utilisant le code suivant (le fichier Video. wmv est supposé exister dans le même répertoire que les fichiers HTML) :


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

 

 




