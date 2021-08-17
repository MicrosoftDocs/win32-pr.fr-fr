---
title: Gestion des événements dans une page Web affichée par Firefox
description: Gestion des événements dans une page Web affichée par Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- contrôle de ActiveX Lecteur Windows Media, gestion des événements
- Lecteur Windows Media contrôle Mobile ActiveX, gestion des événements
- contrôle de ActiveX, gestion des événements
- incorporation, pages Web
- Incorporation de pages Web, gestion des événements
- Lecteur Windows Media, Firefox
- modèle objet Lecteur Windows Media, Firefox
- modèle objet, Firefox
- Lecteur Windows Media Mobile, Firefox
- Lecteur Windows Media ActiveX contrôle, Firefox
- Lecteur Windows Media contrôle de ActiveX Mobile, Firefox
- contrôle ActiveX, Firefox
- Firefox, gestion des événements
- Incorporation de pages Web, Firefox
- événements, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748414"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Gestion des événements dans une page Web affichée par Firefox

lorsque vous incorporez le contrôle Lecteur Windows Media dans une page web, vous pouvez écrire un script qui gère les événements. Pour obtenir la liste des événements déclenchés par le contrôle du lecteur, consultez l' [objet Player](player-object.md).

Si le type MIME associé à un contrôle de lecteur incorporé est application/x-ms-WMP, vous pouvez écrire des gestionnaires d’événements qui ont le format suivant :


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



où *EventName* est le nom d’un événement Lecteur Windows Media, et *params* est une liste des paramètres de l’événement. Par exemple, le code suivant a un gestionnaire pour l’événement [PlayStateChange](player-player-playstatechange.md) .


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Si vous avez plusieurs instances du contrôle Player sur une page Web et si vous utilisez le format indiqué dans l’exemple précédent, chaque gestionnaire d’événements est lié à une instance spécifique du contrôle Player. Dans l’exemple précédent, le gestionnaire d’événements est appelé uniquement lorsque l’état de lecture change pour le contrôle ayant l’ID = « Player ».

Si le type MIME associé à un contrôle de lecteur incorporé n’est pas application/x-ms-WMP, vous pouvez écrire des gestionnaires d’événements au format suivant :


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



où *EventName* est le nom d’un événement Lecteur Windows Media, et *params* est une liste des paramètres de l’événement. Par exemple, le code suivant a un gestionnaire pour l’événement **PlayStateChange** .


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



Si vous avez plusieurs instances du contrôle Player sur une page Web et si vous utilisez le format indiqué dans l’exemple précédent, chaque gestionnaire d’événements est lié à toutes les instances du contrôle du lecteur et le gestionnaire d’événements est appelé lorsque l’état de lecture change pour n’importe quel contrôle de lecteur sur la page.

> [!Note]  
> Si le type MIME n’est pas application/x-ms-WMP, l’événement **DoubleClick** est envoyé en tant que OnDSDblClickEvt (et non OnDSDoubleClickEvt) pour la compatibilité avec la version 6,4 du contrôle du lecteur.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du contrôle Lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




