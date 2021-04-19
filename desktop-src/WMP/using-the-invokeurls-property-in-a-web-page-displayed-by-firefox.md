---
title: Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox
description: Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX du lecteur Windows Media, propriété invokeURLs
- Contrôle ActiveX Windows Media Player Mobile, propriété invokeURLs
- incorporation, pages Web
- Incorporation de page Web, propriété invokeURLs
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Contrôle ActiveX, Firefox
- Firefox, propriété invokeURLs
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106531599"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox

Certains fichiers multimédias contiennent des URL incorporées pour lesquelles le lecteur Windows Media affiche des pages Web dans une fenêtre de navigateur Web ou un frame à mesure que le fichier multimédia est lu. Dans Windows Internet Explorer, vous pouvez utiliser la propriété [Settings. invokeURLs](settings-invokeurls.md) pour spécifier si les pages sont affichées pour les URL incorporées, et vous pouvez utiliser la propriété [Settings. defaultFrame](settings-defaultframe.md) pour spécifier un frame pour l’affichage de ces pages.

Dans Firefox, certaines solutions de contournement sont requises pour définir la propriété **invokeURLs** et pour spécifier un frame permettant d’afficher les pages des URL incorporées.

## <a name="setting-the-invokeurls-property"></a>Définition de la propriété invokeURLs

La valeur par défaut de la propriété **Settings. invokeURLs** est true. par conséquent, si vous souhaitez que la valeur soit false, vous devez la définir explicitement. Dans Internet Explorer, vous pouvez affecter à **invokeURLs** la valeur false dans un élément param à l’intérieur de l’élément Object du contrôle Player.

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

Un fichier multimédia peut contenir des URL qui affichent des pages Web dans une fenêtre ou un frame du navigateur lorsque le fichier multimédia est lu. Dans Internet Explorer, vous pouvez utiliser la propriété [Settings. defaultFrame](settings-defaultframe.md) pour spécifier le frame dans lequel ces pages sont affichées. Si vous ne définissez pas la propriété **defaultFrame** , les URL sont affichées dans une fenêtre distincte du navigateur par défaut. Toutefois, le plug-in Firefox ne prend pas en charge la propriété **Settings. defaultFrame** . Pour contourner cette limitation, affectez la valeur false à la propriété **Settings. invokeURLs** et écrivez un gestionnaire d’événements [commande](player-player-scriptcommand.md) qui définit l’emplacement du frame cible. L’exemple suivant, qui fonctionne dans Internet Explorer et Firefox, illustre cette technique. Supposons que la page Web affichée dans l’exemple se trouve dans le frame \[ 0 \] et que vous souhaitiez que la page de l’URL s’affiche dans le cadre \[ 1 \] .


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

[**Utilisation du contrôle du lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




