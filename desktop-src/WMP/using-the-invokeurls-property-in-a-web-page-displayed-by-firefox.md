---
title: Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox
description: Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- Lecteur Windows Media ActiveX contrôle, pages Web
- Lecteur Windows Media contrôle de ActiveX Mobile, pages Web
- Lecteur Windows Media ActiveX contrôle, propriété invokeURLs
- Lecteur Windows Media contrôle Mobile ActiveX, propriété invokeURLs
- incorporation, pages Web
- Incorporation de page Web, propriété invokeURLs
- Lecteur Windows Media, Firefox
- modèle objet Lecteur Windows Media, Firefox
- modèle objet, Firefox
- Lecteur Windows Media ActiveX contrôle, Firefox
- contrôle ActiveX, Firefox
- Firefox, propriété invokeURLs
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2487ebba1ff5664537dbaf0b0abad02a98acecf3c5985f1c09ffe9f8bbb743c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117108"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox

certains fichiers multimédias contiennent des url incorporées pour lesquelles Lecteur Windows Media affiche des pages web dans une fenêtre de navigateur Web ou un frame à mesure que le fichier multimédia est lu. dans Windows Internet Explorer, vous pouvez utiliser la propriété [Paramètres. invokeURLs](settings-invokeurls.md) pour spécifier si les pages sont affichées pour les url incorporées, et vous pouvez utiliser la propriété [Paramètres. defaultFrame](settings-defaultframe.md) pour spécifier un frame pour l’affichage de ces pages.

Dans Firefox, certaines solutions de contournement sont requises pour définir la propriété **invokeURLs** et pour spécifier un frame permettant d’afficher les pages des URL incorporées.

## <a name="setting-the-invokeurls-property"></a>Définition de la propriété invokeURLs

la valeur par défaut de la propriété **Paramètres. invokeURLs** est true. par conséquent, si vous souhaitez que la valeur soit false, vous devez la définir explicitement. Dans Internet Explorer, vous pouvez affecter à **invokeURLs** la valeur false dans un élément param à l’intérieur de l’élément Object du contrôle Player.

Le plug-in Firefox ne prend pas en charge la définition de la propriété **invokeURLs** dans un élément param.

Vous pouvez contourner cette limitation en définissant la propriété **invokeURLs** dans le script. Le code suivant montre comment définir la propriété **invokeURLs** sur false dans une page Web qui peut être affichée par Internet Explorer et Firefox.


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a>Affichage des pages Web dans un frame

Un fichier multimédia peut contenir des URL qui affichent des pages Web dans une fenêtre ou un frame du navigateur lorsque le fichier multimédia est lu. dans Internet Explorer, vous pouvez utiliser la propriété [Paramètres. defaultFrame](settings-defaultframe.md) pour spécifier le frame dans lequel ces pages sont affichées. Si vous ne définissez pas la propriété **defaultFrame** , les URL sont affichées dans une fenêtre distincte du navigateur par défaut. toutefois, le plug-in Firefox ne prend pas en charge la propriété **Paramètres. defaultFrame** . pour contourner cette limitation, affectez la valeur false à la propriété **Paramètres. invokeURLs** et écrivez un gestionnaire d’événements [commande](player-player-scriptcommand.md) qui définit l’emplacement du frame cible. L’exemple suivant, qui fonctionne dans Internet Explorer et Firefox, illustre cette technique. Supposons que la page Web affichée dans l’exemple se trouve dans le frame \[ 0 \] et que vous souhaitiez que la page de l’URL s’affiche dans le cadre \[ 1 \] .


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du contrôle Lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




