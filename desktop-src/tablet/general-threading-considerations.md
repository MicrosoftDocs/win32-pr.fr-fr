---
description: Vue d’ensemble des considérations générales sur les threads.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Considérations générales sur les threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092573"
---
# <a name="general-threading-considerations"></a>Considérations générales sur les threads

Voici quelques considérations générales sur les threads lors du développement pour Tablet PC.

-   [Threads d’application et non-application](#application-and-non-application-threads)
-   [Considérations relatives aux performances](#performance-considerations)
    -   [Gestionnaires d’événements](#event-handlers)
    -   [AutoRedraw, propriété](#autoredraw-property)
    -   [Propriété DynamicRendering](#dynamicrendering-property)
-   [Considérations sur les threads d’événements](#event-threading-considerations)
    -   [Événements d’objets InkCollector et InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [Événements de collection d’objets manuscrits et de traits](#ink-object-and-strokes-collection-events)
    -   [Événements de reconnaissance](#recognition-events)
    -   [Événements du panneau de saisie PEN](#pen-input-panel-events)
-   [Rubriques connexes](#related-topics)

## <a name="application-and-non-application-threads"></a>Threads d’application et non-application

Tous les événements d’entrée manuscrite sont générés sur un thread d’entrée de haute priorité distinct. Cela permet à l’encre de circuler sans heurts même lorsqu’une application s’exécute lentement. Toutefois, les gestionnaires d’événements peuvent ralentir ou bloquer le rendu de l’encre.

Tous les événements de reconnaissance générés par les appels de méthode de reconnaissance en arrière-plan sont gérés sur un thread de reconnaissance de l’arrière-plan de priorité normale distinct.

Tous les événements de souris sont générés sur le thread d’interface utilisateur principal de l’application.

## <a name="performance-considerations"></a>Considérations relatives aux performances

### <a name="event-handlers"></a>Gestionnaires d'événements

L’interface de programmation d’applications (API) de Tablet PC Platform a un modèle interactif pour les événements plutôt qu’un modèle de notification. Veillez à ce que le code dans les gestionnaires d’événements soit bref pour réduire le temps de blocage du rendu de l’encre. La collecte d’encre par le Tablet PC n’est pas bloquée, mais votre application ne reçoit pas l’encre pendant que votre application est bloquée.

### <a name="autoredraw-property"></a>AutoRedraw, propriété

Lorsque votre application effectue un rendu personnalisé ou lorsque votre application est sensible à la peinture de problèmes, vous pouvez gérer vous-même le redessin et définir la propriété [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) sur **false** pour l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control.md) . Utilisez les événements du tableau suivant pour gérer le redessin.



| Objet ou contrôle                                            | Événement                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Dessin<br/> | les événements control. [invalidate](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) et control [. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) du contrôle sous-jacent.<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Dessin<br/>     | les événements control. [invalidate](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) et control [. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) du contrôle sous-jacent.<br/>                                 |
| [InkPicture](inkpicture-control.md) Régulation<br/>      | contrôle hérité du contrôle [InkPicture](inkpicture-control.md) . les événements [invalidés](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) et [control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/> |



 

### <a name="dynamicrendering-property"></a>Propriété DynamicRendering

Lorsque votre application effectue un rendu personnalisé ou lorsque vous souhaitez obtenir des informations, mais pas l’encre, vous pouvez gérer vous-même l’encre et désactiver le rendu de l’encre en temps réel en affectant à la propriété [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) la **valeur false** pour l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control.md) .

## <a name="event-threading-considerations"></a>Considérations sur les threads d’événements

Les événements de l’API de la plateforme Tablet PC sont déclenchés sur différents threads.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Événements d’objets InkCollector et InkOverlay

La plupart des événements d’objets [**InkCollector**](inkcollector-class.md) et [**InkOverlay**](inkoverlay-class.md) sont déclenchés sur le thread d’encre. Seuls les événements de souris pour ces objets sont déclenchés sur le thread d’interface utilisateur. Par exemple, pour l’objet **InkCollector** , l’événement [**MouseDown**](inkcollector-mousedown.md) est déclenché sur le thread d’interface utilisateur, et l’événement [**CursorDown**](inkcollector-cursordown.md) est déclenché sur le thread Ink.

### <a name="ink-object-and-strokes-collection-events"></a>Événements de collection d’objets manuscrits et de traits

L’objet [**Ink**](inkdisp-class.md) et les événements de collection [**Stroke**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) peuvent provenir du thread Ink ou du thread d’interface utilisateur. Lorsque votre application manipule l’objet **Ink** ou la collection **Strokes** , l’événement est généré dans le thread d’interface utilisateur. Lorsque l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) met à jour la collection d’objets ou de **traits** **manuscrits** , l’événement est généré dans le thread Ink.

Les contrôles [InkPicture](inkpicture-control-reference.md) et [InkEdit](inkedit-control-reference.md) fonctionnent dans un thread cloisonné (STA, Single-Threaded Apartment). Quand le contrôle InkPicture ou InkEdit met à jour la collection d’objets ou de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) d' [**encre**](inkdisp-class.md) , l’événement est déclenché sur le thread d’interface utilisateur.

### <a name="recognition-events"></a>Événements de reconnaissance

Les événements de reconnaissance sont déclenchés sur le thread d’interface utilisateur ou le thread de reconnaissance en arrière-plan.

-   La méthode [**recogniz**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) du contrôle [InkEdit](inkedit-control-reference.md) déclenche l’événement [reconnaissance](/previous-versions/ms836436(v=msdn.10)) (bibliothèque managée uniquement) ou [**RecognitionResult**](inkedit-recognitionresult.md) (Automation uniquement) sur le thread d’interface utilisateur.
-   Les méthodes [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) et [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) déclenchent les événements de [**reconnaissance**](inkrecognizercontext-recognition.md) et de [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) sur le thread de reconnaissance en arrière-plan.

### <a name="pen-input-panel-events"></a>Événements du panneau de saisie PEN

Les événements [**PenInputPanel**](peninputpanel-class.md) sont déclenchés sur le thread dans lequel l’objet **PenInputPanel** est créé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink. InkCollector. DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft. Ink. InkCollector. AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

