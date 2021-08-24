---
title: Utilisation d’un script dans une page Web affichée par Firefox
description: Utilisation d’un script dans une page Web affichée par Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Lecteur Windows Media ActiveX contrôle, exemple de script
- Lecteur Windows Media contrôle Mobile ActiveX, exemple de script
- contrôle de ActiveX, exemple de script
- incorporation, pages Web
- Incorporation de page Web, exemple de script
- Lecteur Windows Media, Firefox
- modèle objet Lecteur Windows Media, Firefox
- modèle objet, Firefox
- Lecteur Windows Media Mobile, Firefox
- Lecteur Windows Media ActiveX contrôle, Firefox
- Lecteur Windows Media contrôle de ActiveX Mobile, Firefox
- contrôle ActiveX, Firefox
- Firefox, exemple de script
- Incorporation de pages Web, Firefox
- exemple de script pour l’incorporation de pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450b03f7adefca1a887fb31207f0a3280e1925c9d3e1f1066df370d87f0a7779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762059"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Utilisation d’un script dans une page Web affichée par Firefox

Un script sur une page Web peut utiliser le modèle objet de lecteur pour contrôler le lecteur lorsque l’utilisateur interagit avec la page. Par exemple, l’élément d’entrée suivant contient un script qui définit le volume du lecteur.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



la plupart des objets du modèle objet Lecteur Windows Media sont pris en charge par Internet Explorer et par le plug-in Firefox. Toutefois, certains objets ne sont pas pris en charge par le plug-in Firefox. Le tableau suivant répertorie tous les objets du modèle objet de lecteur et indique les objets pris en charge par le plug-in Firefox.



| Object                                              | Prise en charge de Firefox |
|-----------------------------------------------------|-----------------|
| [-](cdrom-object.md)                           | non              |
| [CdromCollection](cdromcollection-object.md)       | non              |
| [ClosedCaption](closedcaption-object.md)           | oui             |
| [Contrôles](controls-object.md)                     | non              |
| [DVD](dvd-object.md)                               | non              |
| [Error](error-object.md)                           | oui             |
| [ErrorItem](erroritem-object.md)                   | oui             |
| [Média](media-object.md)                           | oui             |
| [MediaCollection](mediacollection-object.md)       | non              |
| [MetadataPicture](metadatapicture-object.md)       | non              |
| [MetadataText](metadatatext-object.md)             | non              |
| [Réseau](network-object.md)                       | oui             |
| [Lecteur](player-object.md)                         | oui             |
| [PlayerApplication](playerapplication-object.md)   | non              |
| [Sélection](playlist-object.md)                     | oui             |
| [PlaylistArray](playlistarray-object.md)           | non              |
| [PlaylistCollection](playlistcollection-object.md) | non              |
| [Requête](query-object.md)                           | non              |
| [Paramètres](settings-object.md)                     | oui             |
| [StringCollection](stringcollection-object.md)     | non              |



 

Le plug-in Firefox prend en charge l’objet **Player** , mais certaines propriétés de l’objet **Player** renvoient la **valeur null** dans un navigateur Firefox. Par exemple, la propriété [cdromCollection](player-cdromcollection.md) de l’objet **Player** retourne la **valeur null** , car le plug-in Firefox ne prend pas en charge l’objet **cdrom** . De même, les propriétés [DVD](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)et [playlistCollection](player-playlistcollection.md) de l’objet **Player** renvoient la **valeur null** dans un navigateur Firefox.

La propriété **Player. pluginVersionInfo** est prise en charge par le plug-in Firefox, mais pas par Internet Explorer. Cette propriété retourne la version du plug-in Firefox.

Le plug-in Firefox prend en charge l’objet **Media** , y compris la propriété [getItemInfoByType](media-getiteminfobytype.md) . Toutefois, dans un navigateur Firefox, la propriété **getItemInfoByType** ne prend pas en charge les types de retour **MetadataText** et **MetadataPicture** .

le plug-in Firefox prend en charge l’objet [Paramètres](settings-object.md) , à l’exception de la méthode [setMode](settings-setmode.md) et de la propriété [requestMediaAccessRights](settings-requestmediaaccessrights.md) . Dans un navigateur Firefox, la propriété **requestMediaAccessRight** retourne toujours false.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du contrôle Lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




