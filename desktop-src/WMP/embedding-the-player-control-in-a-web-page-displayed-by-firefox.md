---
title: Incorporation du contrôle Player dans une page Web affichée par Firefox
description: Incorporation du contrôle Player dans une page Web affichée par Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Windows Media Player Mobile, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Windows Media Player Mobile contrôle ActiveX, Firefox
- Contrôle ActiveX, Firefox
- Firefox, à propos de l’incorporation de pages Web
- incorporation, pages Web
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106510445"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Incorporation du contrôle Player dans une page Web affichée par Firefox

Pour incorporer le contrôle du lecteur Windows Media dans une page Web qui peut être affichée par un navigateur Firefox, créez un élément objet ou un élément EMBED dont l’attribut **type** est l’un des types MIME suivants :

-   application/x-ms-WMP
-   application/ASX
-   vidéo/x-ms-asf-plug-in
-   application/x-Mplayer2
-   vidéo/x-ms-asf
-   vidéo/x-ms-WM
-   audio/x-ms-WMA
-   audio/x-ms-Wax
-   vidéo/x-ms-WMV
-   vidéo/x-ms-wvx

Le type MIME par défaut est application/x-ms-WMP.

Les exemples suivants montrent comment incorporer le contrôle Player à l’aide d’un élément OBJECT ou d’un élément EMBED.


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



Les exemples précédents fonctionnent dans Firefox, mais pas dans Internet Explorer. Pour incorporer le contrôle du lecteur dans une page Web qui peut être affichée par Internet Explorer, vous devez créer un élément objet dont l’attribut **ClassID** a pour valeur l’ID de classe du contrôle du lecteur Windows Media.

L’exemple suivant montre comment incorporer le contrôle du lecteur Windows Media dans une page Web qui peut être affichée correctement à la fois par Internet Explorer et Firefox. Le script sur la page détecte le type de navigateur et génère la balise d’objet appropriée.


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du contrôle du lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




