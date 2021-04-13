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
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="b5f14-128">Gestion des événements dans une page Web affichée par Firefox</span><span class="sxs-lookup"><span data-stu-id="b5f14-128">Handling Events in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="b5f14-129">Lorsque vous incorporez le contrôle du lecteur Windows Media dans une page Web, vous pouvez écrire un script qui gère les événements.</span><span class="sxs-lookup"><span data-stu-id="b5f14-129">When you embed the Windows Media Player control in a webpage, you can write script that handles events.</span></span> <span data-ttu-id="b5f14-130">Pour obtenir la liste des événements déclenchés par le contrôle du lecteur, consultez l' [objet Player](player-object.md).</span><span class="sxs-lookup"><span data-stu-id="b5f14-130">For a list of events raised by the Player control, see [Player Object](player-object.md).</span></span>

<span data-ttu-id="b5f14-131">Si le type MIME associé à un contrôle de lecteur incorporé est application/x-ms-WMP, vous pouvez écrire des gestionnaires d’événements qui ont le format suivant :</span><span class="sxs-lookup"><span data-stu-id="b5f14-131">If the mime type associated with an embedded Player control is application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



<span data-ttu-id="b5f14-132">où *EventName* est le nom d’un événement du lecteur Windows Media, et *params* est une liste des paramètres de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b5f14-132">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="b5f14-133">Par exemple, le code suivant a un gestionnaire pour l’événement [PlayStateChange](player-player-playstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="b5f14-133">For example, the following code has a handler for the [PlayStateChange](player-player-playstatechange.md) event.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



<span data-ttu-id="b5f14-134">Si vous avez plusieurs instances du contrôle Player sur une page Web et si vous utilisez le format indiqué dans l’exemple précédent, chaque gestionnaire d’événements est lié à une instance spécifique du contrôle Player.</span><span class="sxs-lookup"><span data-stu-id="b5f14-134">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to a specific instance of the Player control.</span></span> <span data-ttu-id="b5f14-135">Dans l’exemple précédent, le gestionnaire d’événements est appelé uniquement lorsque l’état de lecture change pour le contrôle ayant l’ID = « Player ».</span><span class="sxs-lookup"><span data-stu-id="b5f14-135">In the preceeding example, the event handler is called only when the play state changes for the control that has id="Player".</span></span>

<span data-ttu-id="b5f14-136">Si le type MIME associé à un contrôle de lecteur incorporé n’est pas application/x-ms-WMP, vous pouvez écrire des gestionnaires d’événements au format suivant :</span><span class="sxs-lookup"><span data-stu-id="b5f14-136">If the mime type associated with an embedded Player control is not application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



<span data-ttu-id="b5f14-137">où *EventName* est le nom d’un événement du lecteur Windows Media, et *params* est une liste des paramètres de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b5f14-137">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="b5f14-138">Par exemple, le code suivant a un gestionnaire pour l’événement **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="b5f14-138">For example, the following code has a handler for the **PlayStateChange** event.</span></span>


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



<span data-ttu-id="b5f14-139">Si vous avez plusieurs instances du contrôle Player sur une page Web et si vous utilisez le format indiqué dans l’exemple précédent, chaque gestionnaire d’événements est lié à toutes les instances du contrôle du lecteur et le gestionnaire d’événements est appelé lorsque l’état de lecture change pour n’importe quel contrôle de lecteur sur la page.</span><span class="sxs-lookup"><span data-stu-id="b5f14-139">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to all instances of the Player control and the event handler is called when the play state changes for any Player control on the page.</span></span>

> [!Note]  
> <span data-ttu-id="b5f14-140">Si le type MIME n’est pas application/x-ms-WMP, l’événement **DoubleClick** est envoyé en tant que OnDSDblClickEvt (et non OnDSDoubleClickEvt) pour la compatibilité avec la version 6,4 du contrôle du lecteur.</span><span class="sxs-lookup"><span data-stu-id="b5f14-140">If the mime type is not application/x-ms-wmp, the **DoubleClick** event is sent as OnDSDblClickEvt (not OnDSDoubleClickEvt) for compatibility with version 6.4 of the Player control.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5f14-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5f14-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f14-142">**Utilisation du contrôle du lecteur Windows Media avec Firefox**</span><span class="sxs-lookup"><span data-stu-id="b5f14-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




