---
title: Utilisation d’un script dans une page Web affichée par Firefox
description: Utilisation d’un script dans une page Web affichée par Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Contrôle ActiveX du lecteur Windows Media, exemple de script
- Contrôle ActiveX mobile pour Windows Media Player, exemple de script
- Contrôle ActiveX, exemple de script
- incorporation, pages Web
- Incorporation de page Web, exemple de script
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Windows Media Player Mobile, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Windows Media Player Mobile contrôle ActiveX, Firefox
- Contrôle ActiveX, Firefox
- Firefox, exemple de script
- Incorporation de pages Web, Firefox
- exemple de script pour l’incorporation de pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106510849"
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



La plupart des objets du modèle objet du lecteur Windows Media sont pris en charge par Internet Explorer et par le plug-in Firefox. Toutefois, certains objets ne sont pas pris en charge par le plug-in Firefox. Le tableau suivant répertorie tous les objets du modèle objet de lecteur et indique les objets pris en charge par le plug-in Firefox.



| Object                                              | Prise en charge de Firefox |
|-----------------------------------------------------|-----------------|
| [-](cdrom-object.md)                           | non              |
| [CdromCollection](cdromcollection-object.md)       | non              |
| [ClosedCaption](closedcaption-object.md)           | Oui             |
| [Contrôles](controls-object.md)                     | non              |
| [DVD](dvd-object.md)                               | non              |
| [Error](error-object.md)                           | Oui             |
| [ErrorItem](erroritem-object.md)                   | Oui             |
| [Média](media-object.md)                           | Oui             |
| [MediaCollection](mediacollection-object.md)       | non              |
| [MetadataPicture](metadatapicture-object.md)       | non              |
| [MetadataText](metadatatext-object.md)             | non              |
| [Réseau](network-object.md)                       | Oui             |
| [Lecteur](player-object.md)                         | Oui             |
| [PlayerApplication](playerapplication-object.md)   | non              |
| [Playlist](playlist-object.md)                     | Oui             |
| [PlaylistArray](playlistarray-object.md)           | non              |
| [PlaylistCollection](playlistcollection-object.md) | non              |
| [Requête](query-object.md)                           | non              |
| [Paramètres](settings-object.md)                     | Oui             |
| [StringCollection](stringcollection-object.md)     | non              |



 

Le plug-in Firefox prend en charge l’objet **Player** , mais certaines propriétés de l’objet **Player** renvoient la **valeur null** dans un navigateur Firefox. Par exemple, la propriété [cdromCollection](player-cdromcollection.md) de l’objet **Player** retourne la **valeur null** , car le plug-in Firefox ne prend pas en charge l’objet **cdrom** . De même, les propriétés [DVD](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)et [playlistCollection](player-playlistcollection.md) de l’objet **Player** renvoient la **valeur null** dans un navigateur Firefox.

La propriété **Player. pluginVersionInfo** est prise en charge par le plug-in Firefox, mais pas par Internet Explorer. Cette propriété retourne la version du plug-in Firefox.

Le plug-in Firefox prend en charge l’objet **Media** , y compris la propriété [getItemInfoByType](media-getiteminfobytype.md) . Toutefois, dans un navigateur Firefox, la propriété **getItemInfoByType** ne prend pas en charge les types de retour **MetadataText** et **MetadataPicture** .

Le plug-in Firefox prend en charge l’objet [Settings](settings-object.md) , à l’exception de la méthode [setMode](settings-setmode.md) et de la propriété [requestMediaAccessRights](settings-requestmediaaccessrights.md) . Dans un navigateur Firefox, la propriété **requestMediaAccessRight** retourne toujours false.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du contrôle du lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




