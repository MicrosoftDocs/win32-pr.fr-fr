---
title: Incorporation du contrôle Player dans une page Web affichée par Firefox
description: Incorporation du contrôle Player dans une page Web affichée par Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media ActiveX contrôle, pages Web
- Lecteur Windows Media contrôle de ActiveX Mobile, pages Web
- contrôle ActiveX, pages Web
- Lecteur Windows Media, Firefox
- modèle objet Lecteur Windows Media, Firefox
- modèle objet, Firefox
- Lecteur Windows Media Mobile, Firefox
- Lecteur Windows Media ActiveX contrôle, Firefox
- Lecteur Windows Media contrôle de ActiveX Mobile, Firefox
- contrôle ActiveX, Firefox
- Firefox, à propos de l’incorporation de pages Web
- incorporation, pages Web
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c1db799df78cb6c62516798f4bbd196c093f02225386f0c1009bfa11d9a668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578586"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Incorporation du contrôle Player dans une page Web affichée par Firefox

pour incorporer le contrôle Lecteur Windows Media dans une page web qui peut être affichée par un navigateur Firefox, créez un élément objet ou un élément embed dont l’attribut **type** est l’un des types mime suivants :

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



Les exemples précédents fonctionnent dans Firefox, mais pas dans Internet Explorer. pour incorporer le contrôle du lecteur dans une page web qui peut être affichée par Internet Explorer, vous devez créer un élément objet dont l’attribut **classid** a pour valeur l’ID de classe du contrôle Lecteur Windows Media.

l’exemple suivant montre comment incorporer le contrôle Lecteur Windows Media dans une page web qui peut être affichée correctement à la fois par Internet Explorer et Firefox. Le script sur la page détecte le type de navigateur et génère la balise d’objet appropriée.


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

[**utilisation du contrôle Lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




