---
title: Gestion des événements dans une page Web affichée par Firefox
description: Gestion des événements dans une page Web affichée par Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- Contrôle ActiveX du lecteur Windows Media, gestion des événements
- Windows Media Player Mobile contrôle ActiveX, gestion des événements
- Contrôle ActiveX, gestion des événements
- incorporation, pages Web
- Incorporation de pages Web, gestion des événements
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Windows Media Player Mobile, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Windows Media Player Mobile contrôle ActiveX, Firefox
- Contrôle ActiveX, Firefox
- Firefox, gestion des événements
- Incorporation de pages Web, Firefox
- événements, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311686"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Gestion des événements dans une page Web affichée par Firefox

Lorsque vous incorporez le contrôle du lecteur Windows Media dans une page Web, vous pouvez écrire un script qui gère les événements. Pour obtenir la liste des événements déclenchés par le contrôle du lecteur, consultez l' [objet Player](player-object.md).

Si le type MIME associé à un contrôle de lecteur incorporé est application/x-ms-WMP, vous pouvez écrire des gestionnaires d’événements qui ont le format suivant :


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



où *EventName* est le nom d’un événement du lecteur Windows Media, et *params* est une liste des paramètres de l’événement. Par exemple, le code suivant a un gestionnaire pour l’événement [PlayStateChange](player-player-playstatechange.md) .


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



où *EventName* est le nom d’un événement du lecteur Windows Media, et *params* est une liste des paramètres de l’événement. Par exemple, le code suivant a un gestionnaire pour l’événement **PlayStateChange** .


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

[**Utilisation du contrôle du lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




